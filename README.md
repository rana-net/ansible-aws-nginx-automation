
# Automated AWS EC2 Web Server Deployment using Ansible

## Overview

This project automates the provisioning and configuration of AWS EC2 web servers using Ansible.

The solution remotely manages Linux instances over SSH, installs and configures Nginx, and deploys a custom web page automatically using Infrastructure as Code (IaC) principles.

## Architecture

```text
+----------------------------------+
| VirtualBox Ubuntu                |
| (Ansible Control Node)           |
+----------------------------------+
                |
                | SSH
                v
+----------------------------------+
| AWS EC2 Instances                |
| (Managed Nodes)                 |
+----------------------------------+
                |
                | Ansible Playbook
                v
+----------------------------------+
| Install & Configure Nginx        |
| Deploy Custom Web Page           |
+----------------------------------+
```
```
## Features

- Automated Nginx installation using Ansible playbooks
- Remote Linux server management via SSH
- AWS EC2 integration
- Infrastructure as Code (IaC)
- Custom webpage deployment
- Multi-host inventory management
- Idempotent configuration management

## Technologies Used

- Ansible
- AWS EC2
- Ubuntu Linux
- Nginx
- YAML
- SSH
- Oracle VirtualBox

## Project Structure

- `inventory.ini` : Managed hosts inventory
- `install_nginx.yml` : Ansible playbook for Nginx deployment

## How to Run

1. Install Ansible on the control node.

```bash
sudo apt update
sudo apt install ansible -y
