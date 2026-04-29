<!-- This was created with Claude Code -->

shadowman_inventory_collection
==============================

An Ansible role for shadowman inventory collection.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **inventory_source_name**: Variable used in: Update a single inventory source
  - Default: `RHV Inventory`

* **inventory_name**: Variable used in: Update a single inventory source
  - Default: `RHV Inventory`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_inventory_collection
      vars:
        inventory_source_name: <value>
        inventory_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
