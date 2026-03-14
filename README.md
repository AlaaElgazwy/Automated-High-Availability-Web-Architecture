# Automated High-Availability Web Architecture 🚀

## Overview
This project demonstrates a robust, automated infrastructure using **Ansible** and **Nginx**. I've built a load-balanced environment on **AWS EC2** that ensures high availability for web services.

## Architecture
- **1x Load Balancer:** Nginx (Round-Robin algorithm).
- **2x Web Servers:** Ubuntu nodes serving dynamic content.
- **Automation:** Fully configured using Ansible playbooks.



## Key Features
- **Infrastructure as Code (IaC):** Automated server hardening, package installation, and user management.
- **High Availability:** Traffic is distributed across multiple nodes to prevent single points of failure.
- **Security:** Configured SSH key-based authentication and specialized Security Groups.

## How to Run
1. Clone the repo.
2. Update `inventory.` with your server IPs.
3. Run the playbooks:
   ```bash
   ansible-playbook -i inventory playbook.yaml
   ansible-playbook -i inventory web_servers.yaml
   ansible-playbook -i inventory load_balancer.yaml
