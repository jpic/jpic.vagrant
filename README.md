Role Name
=========

Installs Vagrant + VirtualBox, and 
``virtualbox-ck-host-module-{{ vagrant_ck_march }}`` if set.

Requirements
------------

Currently supports only Arch Linux, welcome PRs !

Role Variables
--------------

- vagrant_ck_march: march to use, ie. haswell, core2, etc ... In case you want the appropriate ``virtualbox-ck-host-module-``.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Basic vagrant setup:

    - hosts: servers
      roles:
      - jpic.vagrant

Or with precompiled modules for your kernel:

    - hosts: servers
      roles:
      - { role: jpic.vagrant, march: core2 }

Recommended for arch linux:

    - hosts: servers
      roles:
      - jpic.march
      - jpic.ck
      - jpic.squid
      - role: jpic.vagrant
        vagrant_http_proxy: http://10.0.2.2:3128

License
-------

BSD
