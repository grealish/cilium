Getting Started with Vagrant
============================

This is a simple Vagrant environment to experiment with Cilium. To get started,
simply run ``vagrant up`` and then log into the VM with ``vagrant ssh``.

For further instructions, please see the `Getting started guide`_.

.. _Getting started guide: https://cilium.readthedocs.io/en/latest/gettingstarted/docker

::

    $ vagrant up
    Bringing machine 'default' up with 'virtualbox' provider...
    [...]
    ==> default: cilium-kvstore is up-to-date
    ==> default: Recreating cilium
    ==> default: Recreating cilium-docker-plugin

    $ vagrant ssh
    Welcome to Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-76-generic x86_64)
    [...]

    vagrant@vagrant:~/cilium/examples/getting-started$ cilium status
    KVStore:                Ok         Consul: 172.19.0.2:8300
    ContainerRuntime:       Ok         docker daemon: OK
    Kubernetes:             Disabled   
    Cilium:                 Ok         OK
    NodeMonitor:            Disabled
    Cilium health daemon:   Ok   
    IPAM:                   IPv4: 3/65535 allocated from 10.15.0.0/16, IPv6: 2/65535 allocated from f00d::a0f:0:0:0/112
    Controller Status:      18/18 healthy
    Proxy Status:           OK, ip 10.15.190.163, port-range 10000-20000
    Cluster health:   1/1 reachable   (2020-02-16T14:07:14Z)