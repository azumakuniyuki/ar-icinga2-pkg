Ansible Role: icinga2(pkg)
================================================================================
Install Icinga2 and nagios plugins from a package at CentOS 7 and build icinga2
as an Agent-Less monitoring environment.

- Install icinga2 and Nagios Plugins
- Deploy files into /etc/icinga2

Requirements
--------------------------------------------------------------------------------
No requirements.

Role Variables
--------------------------------------------------------------------------------
These variables are defined in defaults/main.yml file for being removed and
installed packages on each supported platform.

```yaml
icinga2:
  enabled: true
  started: true
  contact:
    useragent: hostmaster@example.com
  nodes:
    - name: 127.0.0.1
      file: 
        - app
        - commands
        - downtimes
        - groups
        - hosts
        - services
        - users
```

Dependencies
--------------------------------------------------------------------------------
None

Example Playbook
--------------------------------------------------------------------------------
```yaml
- hosts: servers
  roles:
    - { role: azumakuniyuki.ar-icinga2-pkg }
```

License
--------------------------------------------------------------------------------
BSD

Author Information
--------------------------------------------------------------------------------
[azumakuniyuki](http://nyaan.jp)

