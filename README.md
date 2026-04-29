<!-- This was created with Claude Code -->

# Provision Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Provision)


This directory contains Ansible automation for provision management and operations.

## Overview

The Provision automation provides playbooks and roles for managing and configuring
provision infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [determine_vmware_placement](roles/determine_vmware_placement/README.md) | Role for determine vmware placement |
| [generate_vm_names](roles/generate_vm_names/README.md) | Role for generate vm names |
| [shadowman_agentcert](roles/shadowman_agentcert/README.md) | Role for shadowman agentcert |
| [shadowman_aws_account_clear](roles/shadowman_aws_account_clear/README.md) | Role for shadowman aws account clear |
| [shadowman_deprovision](roles/shadowman_deprovision/README.md) | Role for shadowman deprovision |
| [shadowman_hosted_cluster](roles/shadowman_hosted_cluster/README.md) | Role for shadowman hosted cluster |
| [shadowman_hosted_cluster_remove](roles/shadowman_hosted_cluster_remove/README.md) | Role for shadowman hosted cluster remove |
| [shadowman_hostnameset](roles/shadowman_hostnameset/README.md) | Role for shadowman hostnameset |
| [shadowman_inventory_collection](roles/shadowman_inventory_collection/README.md) | Role for shadowman inventory collection |
| [shadowman_provision](roles/shadowman_provision/README.md) | Role for shadowman provision |
| [shadowman_snapshots](roles/shadowman_snapshots/README.md) | Role for shadowman snapshots |
| [shadowman_soft_delete](roles/shadowman_soft_delete/README.md) | Role for shadowman soft delete |
| [shadowman_soft_delete_batch](roles/shadowman_soft_delete_batch/README.md) | Batch Soft Delete hosts no longer in the inventory from the Controller's host metrics. |
| [shadowman_template_create](roles/shadowman_template_create/README.md) | Role for shadowman template create |
| [shadowman_unsubscribe](roles/shadowman_unsubscribe/README.md) | Role for shadowman unsubscribe |
| [shadowman_vmware_convert_to_template](roles/shadowman_vmware_convert_to_template/README.md) | Role for shadowman vmware convert to template |
| [shadowman_vmware_convert_to_vm](roles/shadowman_vmware_convert_to_vm/README.md) | Role for shadowman vmware convert to vm |
| [shadowman_vmware_update_template](roles/shadowman_vmware_update_template/README.md) | Role for shadowman vmware update template |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| aws_clear_role.yml | Playbook for aws clear role | localhost |
| determine_vcenter_params.yml | Playbook for determine vcenter params | localhost |
| generate_vm_names.yml | Playbook for generate vm names | localhost |
| removefromAD.yml | Playbook for removefromAD | {{ vm_name }} |
| removesubs.yml | Playbook for removesubs | {{ vm_name | default('all') }} |
| rhv_hosted_ocp_create.yml | Playbook for rhv hosted ocp create | localhost, just_created |
| rhv_hosted_ocp_remove.yml | Playbook for rhv hosted ocp remove | localhost |
| rhv_template_create.yml | Playbook for rhv template create | localhost |
| rhv_vm_create.yml | Playbook for rhv vm create | localhost, just_created |
| rhv_vm_remove.yml | Playbook for rhv vm remove | {{ vm_name | default('none') }} |
| rhv_vmfortemplate_create.yml | Playbook for rhv vmfortemplate create | localhost |
| shadowman_inventory_sync_collection.yml | Playbook for shadowman inventory sync collection | localhost |
| snapshot_create.yml | Playbook for snapshot create | localhost |
| snapshot_pull_collection.yml | Playbook for snapshot pull collection | localhost |
| snapshot_restore.yml | Playbook for snapshot restore | localhost |
| terraform create_vmware.yml | Playbook for terraform create vmware | localhost, just_created |
| terraform_hostnameset_vmware.yml | Playbook for terraform hostnameset vmware | localhost, just_created |
| terraform_hostnameset_vmware_actions.yml | Playbook for terraform hostnameset vmware actions | localhost, just_created |
| vm_create_role.yml | Playbook for vm create role | localhost, just_created |
| vm_remove_role.yml | Playbook for vm remove role | {{ vm_name | default('none') }} |
| vm_soft_delete.yml | Playbook for vm soft delete | localhost |
| vm_soft_delete_batch.yml | Playbook for vm soft delete batch | localhost |
| vmware_template_update.yml | Playbook for vmware template update | localhost, justcreated, localhost |
| vmware_vm_create.yml | Playbook for vmware vm create | localhost, just_created |
| vmware_vm_remove.yml | Playbook for vmware vm remove | {{ vm_name | default('none') }} |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run aws_clear_role.yml

# Run in stdout mode
ansible-navigator run aws_clear_role.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - shadowman_agentcert
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-Provision/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
