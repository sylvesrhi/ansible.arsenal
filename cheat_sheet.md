## Ansible Cheat Sheet: Everyday Commands for Sys Admins
1. Check Ansible Version

ansible --version
2. Ping All Hosts in Inventory

ansible all -m ping
3. Run Ad-hoc Command on All Hosts
For example, check uptime:


ansible all -a "uptime"
4. Run a Module (e.g., install a package)
Install httpd on all hosts:


ansible all -m yum -a "name=httpd state=present"
5. Specify User and Become Root

ansible all -m ping -u username --become
6. Run Playbook

ansible-playbook site.yml
7. Check Playbook Syntax

ansible-playbook playbook.yml --syntax-check
8. List All Hosts in Inventory

ansible all --list-hosts
9. Use Inventory File

ansible-playbook -i inventory.ini playbook.yml
10. Dry Run (Check mode)

ansible-playbook playbook.yml --check
11. Show Differences in Change

ansible-playbook playbook.yml --diff
12. Limit to Specific Host or Group

ansible-playbook playbook.yml -l webservers
13. Gather Detailed Facts About a Host

ansible host1 -m setup
14. Tag Management
Run only specific tags:


ansible-playbook playbook.yml --tags "setup"
Skip specific tags:


ansible-playbook playbook.yml --skip-tags "debug"
15. Vault (Encrypt Sensitive Data)
Encrypt a file:


ansible-vault encrypt secrets.yml
Decrypt a file:


ansible-vault decrypt secrets.yml
Edit encrypted file:


ansible-vault edit secrets.yml
Run playbook with vault password prompt:


ansible-playbook playbook.yml --ask-vault-pass
Tips:

Replace all with a specific host or group as needed.

The -m flag specifies the module; -a passes arguments.

Use --become for privilege escalation (sudo).
