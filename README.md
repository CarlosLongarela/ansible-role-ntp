Ansible Role: Ntp
=========

[![Build Status](https://travis-ci.org/CarlosLongarela/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/CarlosLongarela/ansible-role-ntp)

Ntp install and basic configuration. This role is util for a empty xenial ubuntu basic configuration.

Requirements
------------

None.

Role Variables
--------------

    ntp_daemon: ntp
    ntp_enabled: true
    ntp_timezone: Europe/Madrid

    ntp_manage_config: true
    ntp_servers:
    - 0.ubuntu.pool.ntp.org iburst
    - 1.ubuntu.pool.ntp.org iburst
    - 2.ubuntu.pool.ntp.org iburst
    - 3.ubuntu.pool.ntp.org iburst

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers

      gather_facts: no
      become: true

      vars:
        ntp_timezone: Europe/Dublin

      roles:
         - { role: CarlosLongarela.ntp }

License
-------

GPLv2

Author Information
------------------

This role was created in 2017, May by [Carlos Longarela](mailto:carlos@longarela.eu), from [Taberna WordPress](https://tabernawp.com/).
