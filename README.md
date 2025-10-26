# Server Hardening Automation with Ansible 🛡️

This project automates server hardening using Ansible roles. It helps secure your Ubuntu servers by managing users, SSH, firewall, updates, and auditing.

---

## 📝 Project Purpose

- Automate server hardening tasks using Ansible.
- Ensure security best practices are applied consistently.
- Provide modular, reusable roles for different hardening tasks.

---## 🧱 Folder Structure

server-hardening-ansible/
├── ansible.cfg
├── inventory.ini
├── site.yml
└── roles/
├── users/
│ └── tasks/main.yml
├── ssh/
│ └── tasks/main.yml
├── firewall/
│ └── tasks/main.yml
├── updates/
│ └── tasks/main.yml
└── auditing/
└── tasks/main.yml

yaml
Copy code

---

## 🔐 Roles Overview

- **users** – Create admin users and set password policies.  
- **ssh** – Harden SSH settings, disable root login.  
- **firewall** – Configure UFW to allow only necessary ports.  
- **updates** – Keep system packages up to date.  
- **auditing** – Install and enable `auditd` service.

---

## 🚀 Usage Instructions

1. Clone the repository:
```bash
git clone <YOUR_GITHUB_REPO_URL>
cd server-hardening-ansible
Update your inventory.ini with your server details:

ini
Copy code
[servers]
192.168.56.10 ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
Run the playbook:

bash
Copy code
ansible-playbook site.yml
📌 Requirements
Ansible >= 2.9

Ubuntu/Debian-based server

SSH access with sudo privileges

📝 License
MIT License

vbnet
Copy code

