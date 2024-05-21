# WordPress Blog Deployment on LAMP Stack using Ansible

Welcome to the WordPress Blog Deployment project! This repository contains Ansible playbooks and configurations to set up a WordPress blog on a LAMP (Linux, Apache, MySQL, PHP) stack. Follow the instructions below to deploy your WordPress blog easily and efficiently.

![WordPress Logo](https://wordpress.org/about/logos/)

## Table of Contents

- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
## Prerequisites

Before you begin, ensure you have met the following requirements:

- Ansible installed on your local machine
- A server (or virtual machine) running a Linux distribution (Ubuntu, CentOS, etc.)
- SSH access to the server
- Basic knowledge of Ansible and YAML syntax

## Project Structure

```plaintext
.
├── ansible.cfg
├── hosts
├── playbook.yml
├── roles
│   ├── apache
│   │   └── tasks
│   │       └── main.yml
│   ├── mysql
│   │   └── tasks
│   │       └── main.yml
│   ├── php
│   │   └── tasks
│   │       └── main.yml
└── README.md
```
# Installation

## Clone the repository:
  ```bash
 git clone https://github.com/Bilal80/wordpress-lamp-ansible.git
  cd ansible-wordpress
```

 ## Configure the inventory:
  Update the *hosts* file with your server details.
  ```bash
[demo]
node_private_ip
```
# Usage
## Run the playbook:
Execute the Ansible playbook to deploy the WordPress blog.
  ```bash
ansible-playbook -i hosts playbook.yml
```
Using Ansible Role to deploy the WordPress blog.
  ```bash
ansible-playbook main.yml
```
## Access your blog:
Once the playbook completes, open your web browser and navigate to your server's IP address to complete the WordPress setup through the web interface.
# Customization
Feel free to customize the Ansible roles and tasks according to your needs. Here are some common customizations:
- **Apache Configuration:** Edit **`roles/apache/tasks/main.yml`** to customize Apache settings.
- **PHP Configuration:** Modify **`roles/php/tasks/main.yml`** for PHP-specific configurations.
- **MySQL Configuration:** Adjust database settings in **`roles/mysql/tasks/main.yml.`**

