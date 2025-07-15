# Ansible Playbook Pack (v1)

Welcome to the Ansible Arsenal. This pack includes ready-to-use, real-world playbooks for Linux DevOps automation.

Each playbook is modular and comes with default variables and a sample inventory to get you started.

## What's Included
- Ansible install script (bash script)
- Join Ubuntu to Active Directory
- Install CrowdStrike Falcon Sensor
- Create local or domain-bound users (conditionally)
- Secure your server (UFW, CIS)
  
## Requirements
- Ansible 2.9+
- Ubuntu 22.04 - 24.04 servers
- SSH access and sudo privileges

## Getting Started
1. Create/update your inventory file
2. Adjust variables in `group_vars/.yml`

## Usage
If using within a role use the post_config.yaml script to run the required playbooks sequentially...

```
---
- name: Post-Install Config
  hosts: all
  become: yes
  roles:
   - sudoers
   - cis_hardening
   - ufw
   - chronyd
   - tenable
```

`ansible-playbook -i <inventory_file> post_config.yaml`
