# Ansible Windows User Lifecycle Management

Manage Windows local users using Ansible with GitHub as the Source of Truth.

This project demonstrates how to automate the complete lifecycle of Windows local user accounts using Ansible.

Instead of maintaining multiple playbooks for different actions, user information is stored in a GitHub-managed YAML file. Ansible reads the desired state and automatically creates, disables, or removes users from Windows servers.

---

## Architecture

GitHub Repository
        |
        v
    users.yml
        |
        v
Ansible Control Node
        |
        v
Windows Servers (WinRM)

GitHub acts as the Source of Truth.

Ansible enforces the desired state on target Windows systems.

---

## Features

- Create local Windows users
- Disable local users
- Delete local users
- Centralized user management
- Infrastructure as Code (IaC)
- Git-based change tracking
- Idempotent automation
- Scalable across multiple Windows servers

---

## Repository Structure

```text
ansible-windows-user-management/
│
├── inventories/
│   └── hosts.ini
│
├── vars/
│   └── users.yml
│
├── manage_users.yml
│
└── README.md
