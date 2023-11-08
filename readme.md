# Ansible + Laravel Demo

This repository was part of the [Automating Server Setup - a DigitalOcean Workshop Kit](https://www.digitalocean.com/community/meetup_kits/automating-server-setup-with-ansible-a-digitalocean-workshop-kit).

However, that tutorial was outdate and used Ubuntu 18.04 along with outdated Laravel that relied on php 7.4, thus this repository have been modified to work with the following setup:

- Deploy on Ubuntu 22.04 LTS
- Use PHP 8.1
- Laravel 9
- Use git to pull latest changes from GitHub repo containing Laravel 9
- Replace some some roles: php and composer with geerlingguy's php and composer and added geerlingguy.swap to add some swap as a safety net.

## Quick Setup

TL;DR:

Make sure you have [Ansible installed](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-22-04) on your control node, which can be your local machine or a remote server dedicated to running Ansible.
You'll need one Ubuntu 22.04 server to serve as node / host.

1. Clone this repository
2. Set up your inventory file - you can use `hosts` as base - change to your Laravel node VPS's IP address.
3. Adjust values on your `group_vars/all.yml` file
4. Run the `server-setup.yml` playbook to set up the LEMP server
5. Run the `laravel-deploy.yml` playbook to deploy the demo Laravel application
6. Access your server's IP address or hostname to test the setup
