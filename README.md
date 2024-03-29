# DigitalOcean Solr Search Engine deployment with automatic inventory config

[![Lint Ansible playbooks](https://github.com/skorupcia/DigitalOcean_Solr/actions/workflows/ci.yml/badge.svg)](https://github.com/skorupcia/DigitalOcean_Solr/actions/workflows/ci.yml)

## Specifications

macOS: Sonoma 14.2.1

Solr version: 8.6.0

Ubuntu: 23-10-x64

## Instructions

1. Add your machine SSH to DigitalOcean account
2. Update hosts file position

   a) ansible_ssh_private_key_file (path to your public ssh file)
3. Create API token and add to your DigitalOcean project
4. Update vars files to your personal preferences

   a) Update u_token in Connection vars (api_token)

   b) Update u_ssh in Connection vars (ssh fingerprint)

   c) Update hosts_dest with your actual path to the hosts file (you can use pwd)
5. Run droplet.yml playbook to deploy new droplet on DigtalOcean and automatically update hosts inventory file
6. Run solr.yml playbook to install solr engine
7. Connect to your Solr engine with droplet ip and 8983 port (or the one you have applied in config)

## Droplet Delete

If you would like to delete droplet, simply switch state of "Create Digitalocean droplet" from PRESENT to ABSENT and run playbook.
