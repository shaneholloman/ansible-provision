<!-- This was created with Claude Code -->

shadowman_aws_account_clear
===========================

An Ansible role for shadowman aws account clear.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

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
    - role: shadowman_aws_account_clear
      vars:
        _region_: <value>
        vpc_name: <value>
        igw_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
