<!-- This was created with Claude Code -->

shadowman_deprovision
=====================

An Ansible role for shadowman deprovision.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **vm_names**: Virtual machine name
  - Default: `{{ vm_name.split(',') }}`

* **datacenter**: Data payload
  - Default: `Default`

* **resource_group**: Group name or identifier
  - Default: `Demo`

* **_region_**: Cloud region or geographical location
  - Default: `us-east-2`

* **vpc_name**: Resource name
  - Default: `Shadowman VPC`

* **igw_name**: Resource name
  - Default: `Shadowman IGW`

* **subnet_name**: Resource name
  - Default: `Shadowman Subnet`

* **_route_table_name_**: Resource name
  - Default: `Shadowman Route Table`

* **_security_group_**: URL or URI endpoint
  - Default: `ShadowmanSG`

* **_key_name_**: Resource name
  - Default: `Shadowmankey`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_deprovision
      vars:
        vm_names: <value>
        datacenter: <value>
        resource_group: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
