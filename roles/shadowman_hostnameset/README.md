<!-- This was created with Claude Code -->

shadowman_hostnameset
=====================

An Ansible role for shadowman hostnameset.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **vm_names**: Virtual machine name
  - Default: `{{ vm_name.split(',') }}`

* **shadowman_provision_hypervisor**: Variable used in: RHV Hostname
  - Default: `RHV`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_hostnameset
      vars:
        vm_names: <value>
        shadowman_provision_hypervisor: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
