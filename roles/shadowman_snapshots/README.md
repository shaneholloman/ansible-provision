<!-- This was created with Claude Code -->

shadowman_snapshots
===================

An Ansible role for shadowman snapshots.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **datacenter**: Data payload
  - Default: `Default`

* **vm_names**: Virtual machine name
  - Default: `{{ vm_name.split(',') }}`

* **cluster**: Cluster name or identifier
  - Default: `Default`

* **extra_var**: Variable value
  - Default: `{'vm_name': '{{ vm_name }}'}`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_snapshots
      vars:
        datacenter: <value>
        vm_names: <value>
        cluster: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
