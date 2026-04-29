<!-- This was created with Claude Code -->

shadowman_provision
===================

An Ansible role for shadowman provision.

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

* **template**: Template name or path
  - Default: `{{ operating_system }}_ShadowMan`

* **vm_memory**: Memory configuration or limit
  - Default: `4GiB`

* **vm_names**: Virtual machine name
  - Default: `{{ vm_name.split(',') }}`

* **vm_template**: Template name or path
  - Default: `71a8e15d-3602-41f7-8e2c-4689863131ef`

* **vm_memory_terraform**: Memory configuration or limit
  - Default: `4096`

* **vm_operating_system_tag**: Resource tags or labels
  - Default: `RHEL`

* **terraform_disk**: Disk or storage configuration
  - Default: `20`

* **terraform_network**: Network configuration
  - Default: `VM Network`

* **cluster_id**: Cluster name or identifier
  - Default: `Cluster01`

* **datastore_id**: Unique identifier
  - Default: `vsanDatastore`

* **folder_id**: Unique identifier
  - Default: `Lab virtual machine`

* **source_vm_id**: Unique identifier
  - Default: `{{ operating_system }}_ShadowMan`

* **operating_system_tag**: Resource tags or labels
  - Default: `RHEL`

* **shadowman_provision_hypervisor**: Variable used in: Azure VM Create
  - Default: `RHV`

* **azure_location**: Configuration parameter for shadowman_provision
  - Default: `eastus`

* **state**: Desired state (present, absent, started, stopped, etc.)
  - Default: `poweredon`

* **publisher**: Configuration parameter for shadowman_provision
  - Default: `RedHat`

* **offer**: Configuration parameter for shadowman_provision
  - Default: `RHEL`

* **version**: Version number or identifier
  - Default: `latest`

* **sku**: Configuration parameter for shadowman_provision
  - Default: `9-lvm-gen2`

* **vm_size**: Size specification
  - Default: `Standard_B2s`

* **resource_group_name**: Resource name
  - Default: `Demo`

* **storage_account_name**: Resource name
  - Default: `demorh`

* **storage_account_type**: Numeric count or quantity
  - Default: `Standard_RAGRS`

* **terraform_state**: Desired state (present, absent, started, stopped, etc.)
  - Default: `absent`

* **terraformmain**: Configuration parameter for shadowman_provision
  - Default: `ansible`

* **shadowman_storage_domain**: shadowman_storage_domain: NFS_Cersei
  - Default: `SSD_Array`

* **_image_id_**: Image identifier or name
  - Default: `ami-05ae892102a574172`

* **image_lookup**: Image identifier or name
  - Default: `RHEL-7.9`

* **_region_**: Cloud region or geographical location
  - Default: `us-east-2`

* **vpc_name**: Resource name
  - Default: `Shadowman VPC`

* **_vpc_cidr_block_**: Virtual Private Cloud identifier
  - Default: `11.0.0.0/16`

* **igw_name**: Resource name
  - Default: `Shadowman IGW`

* **_subnet_cidr_**: Network subnet
  - Default: `11.0.1.0/24`

* **subnet_name**: Resource name
  - Default: `Shadowman Subnet`

* **_route_table_name_**: Resource name
  - Default: `Shadowman Route Table`

* **destination_cidr_block**: Unique identifier
  - Default: `0.0.0.0/0`

* **_security_group_**: URL or URI endpoint
  - Default: `ShadowmanSG`

* **_key_name_**: Resource name
  - Default: `Shadowmankey`

* **_instance_type_**: Type specification
  - Default: `t2.micro`

* **tf_build**: Configuration parameter for shadowman_provision
  - Default: `ansible01`

* **terraform_working_dir**: Directory path
  - Default: `/tmp/srv/`

* **ocp_preference**: Reference identifier
  - Default: `rhel.10`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_provision
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
