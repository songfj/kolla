FROM %%KOLLA_NAMESPACE%%/%%KOLLA_PREFIX%%base
MAINTAINER Kolla Project (https://launchpad.net/kolla)

RUN yum -y install libvirtd libguestfs qemu-system-x86 \
        libvirt-daemon-driver-nwfilter \
        libvirt-daemon-config-nwfilter; yum clean all

VOLUME [ "/sys/fs/cgroup" ]
VOLUME [ "/var/lib/nova" ]

ADD ./start.sh /start.sh

CMD ["/start.sh"]
