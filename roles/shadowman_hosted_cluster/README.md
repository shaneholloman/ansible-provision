<!-- This was created with Claude Code -->

shadowman_hosted_cluster
========================

An Ansible role for shadowman hosted cluster.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **datacenter**: Data payload
  - Default: `Default`

* **cluster**: Variable used in: {{ item }}
  - Default: `Default`

* **template**: Configuration parameter for ca_file task
  - Default: `hypershift-hosted-worker`

* **vm_names**: Virtual machine name
  - Default: `{{ vm_name.split(',') }}`

* **vm_state**: Desired state (present, absent, started, stopped, etc.)
  - Default: `running`

* **shadowman_storage_domain**: shadowman_storage_domain: NFS_Cersei
  - Default: `SSD_Array`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_hosted_cluster
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
