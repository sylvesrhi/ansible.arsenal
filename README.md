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
1. Update your inventory
2. Adjust variables in `group_vars/all.yml`
3. Run your playbook:  
   ```bash
   ansible-playbook -i inventory playbooks/join_domain.yml
