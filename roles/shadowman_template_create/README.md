<!-- This was created with Claude Code -->

shadowman_template_create
=========================

An Ansible role for shadowman template create.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **datacenter**: Data payload
  - Default: `Default`

* **cluster**: Cluster name or identifier
  - Default: `Default`

* **template**: Variable used in: VM Create for Template
  - Default: `{{ operating_system }}_ShadowMan`

* **vm_memory**: Memory configuration or limit
  - Default: `4GiB`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_template_create
      vars:
        datacenter: <value>
        cluster: <value>
        template: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
