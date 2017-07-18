Role Name
=========

Very simple `rsyslog` configuration role.  Based on [current rsyslog role in cnx-deploy](https://github.com/Connexions/cnx-deploy/tree/61848081e1083c322dfcf8b7a833057cfc43005c/roles/rsyslog).

Requirements
------------

Ansible > 2, Ubuntu

Role Variables
--------------

`rsyslog_hostname` is needed, and is defaulted to `inventory_hostname` in `defaults/main.yml`.

Dependencies
------------

No dependencies, but `osdeploy.papertrail` and `osdeploy.graylog` will depend on this.

Example Playbook
----------------

```
    - hosts: servers
      roles:
        - role: osdeploy.rsyslog
          rsyslog_hostname: "{{ hostvars[inventory_hostname] }}"
```

License
-------

BSD

Author Information
------------------

[OpenStax](https://github.com/openstax)
