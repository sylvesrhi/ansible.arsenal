# Ansible Arsenal — Real-World Linux Automation

Automate the build, configuration, and security hardening of Ubuntu servers using modular, production-ready Ansible playbooks.

This collection is designed for real-life environments — from enterprise IT to homelab clusters — and showcases my approach to scalable automation, compliance, and DevOps consistency.

## ✅ What This Repository Delivers

These playbooks automate common but time-consuming infrastructure tasks:

## 🔐 Security & Compliance

CIS benchmark hardening

SSH lockdown and kernel tuning

UFW firewall baseline

Security agent installs (CrowdStrike, Tenable)

## 🏢 Identity & Access

Join Ubuntu machines to Active Directory

Configure SSSD for domain auth

Create and manage local or domain users

SSH key configuration

## ⚙️ System Configuration

Chrony/NTP setup

Package installation and updates

Hostname, DNS, and environment prep

## 🧩 Orchestration

Modular roles can be run individually or chained together using the included post_config.yaml orchestration playbook.

## 🏁 Quick Start (Demo-Friendly)
`git clone https://github.com/sylvesrhi/ansible.arsenal.git
cd ansible.arsenal`


Review or copy the sample inventory file

Update group_vars or host_vars as needed

Run the main orchestration:

`ansible-playbook -i inventory.sample post_config.yaml`


You can also run any role independently for testing or customization.

# ✅ Real-World Use Cases

These playbooks were built to solve problems like:

Deploying new Linux servers quickly without manual steps

Meeting security/compliance requirements (e.g., CIS)

Standardizing configuration across dev, prod, or lab environments

Accelerating onboarding when working with AD-integrated infrastructure

Automating agent deployment for monitoring and endpoint protection

Example impact:

“Using this structure, a CIS-hardened, domain-joined Linux host can go from vanilla ISO to production-ready in under 15 minutes.”

## 🔧 Requirements

Ansible: v2.9+

Supported OS: Ubuntu 22.04 or 24.04

Access: SSH + sudo privileges

Optional: AD credentials and endpoint agent keys

## 🌟 How This Fits My Portfolio

This repository reflects my experience in:

Infrastructure automation & DevOps practices

Security compliance and system hardening

Enterprise integrations (AD, endpoint agents)

Reusable role design and orchestration

Scalable configuration management

I use this codebase as a foundation for client work, internal tooling, and continuous improvement of my automation skills.
