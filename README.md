Limits
=========

Role designed to configure limits for services using systemd.

Requirements
------------

* Ansible 2.7+

Role Variables
--------------

    limits_systemd_service:
      - name:
        nofile:
        memlock:
        nproc:

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: servers
      vars:
        limits_systemd_service:
          - name: mysqld
            nofile: 65535
            memlock: 'infinity'
      roles:
         - role: ansible-role-limits

License
-------

Apache

Author Information
------------------

Timothy Vigers <tvigers@serversumo.io>
