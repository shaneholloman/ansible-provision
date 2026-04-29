<!-- This was created with Claude Code -->

shadowman_soft_delete_batch
===========================

Batch Soft Delete hosts no longer in the inventory from the Controller's host metrics.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **shadowman_soft_delete_batch_bool**: Removal flag or target
  - Default: `True`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_soft_delete_batch
      vars:
        shadowman_soft_delete_batch_bool: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
