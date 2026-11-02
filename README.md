# ShopEasy — Ansible Configuration Management

## Project Overview

ShopEasy is a simple e-commerce storefront developed to demonstrate DevOps concepts and configuration management using Ansible.

The webpage displays sample products, descriptions, and prices. Ansible automates the installation of Nginx, deployment of the webpage, and startup of the web server.

## Technologies Used

- HTML and CSS
- Ansible
- Nginx
- Linux
- SSH
- AWS EC2

## Project Features

- Simple e-commerce storefront
- Product cards with names and prices
- Responsive webpage layout
- Automated Nginx installation
- Automated webpage deployment
- Automated web service startup

## Deployment Workflow

1. Configure the managed Linux server.
2. Define the managed host in `inventory.ini`.
3. Test connectivity using Ansible.
4. Execute the playbook in `site.yml`.
5. Verify the Nginx service.
6. Access the deployed webpage through a browser.

## Execution Commands

Test connectivity:

    ansible webservers -m ping

Check playbook syntax:

    ansible-playbook site.yml --syntax-check

Execute the playbook:

    ansible-playbook site.yml

Verify Nginx on the managed server:

    sudo systemctl status nginx

Test the HTTP response:

    curl -I http://localhost

## Project Scope

This is a demonstration storefront. It does not implement a real shopping cart backend, user authentication, payment processing, or a product database.

## Security

Private SSH keys, passwords, and cloud credentials must not be committed to the repository.
