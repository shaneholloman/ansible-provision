<!-- This was created with Claude Code -->

shadowman_soft_delete
=====================

An Ansible role for shadowman soft delete.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **vm_names**: Variable used in: Loop to soft delete all hosts
  - Default: `{{ vm_name.split(',') }}`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_soft_delete
      vars:
        vm_names: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
