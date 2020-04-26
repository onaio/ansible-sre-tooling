Ansible SRE Tooling [![Build Status](https://github.com/onaio/ansible-sre-tooling/workflows/CI/badge.svg)](https://github.com/onaio/ansible-sre-tooling/actions?query=workflow%3ACI)
=========

Installs the [SRE Tooling](https://github.com/onaio/sre-tooling) application and optionally services to augment the application.

Role Variables
--------------

* `sre_tooling_enabled_services`: A list of services to augment the SRE Tooling application. Supported values are:
  1. `infra-index-update`: Installs a systemd timer that updates the index of the host (and optionally the hostname) within a group of cloud resources.


Example Playbook
----------------

Here's an example of how to run the role in a playbook:

```yml
- hosts: servers
  roles:
    - role: onaio.sre-tooling
      vars:
        sre_tooling_enabled_services:
          - infra-index-update
```

License
-------

Apache 2
