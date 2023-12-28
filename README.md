# DigitalOcean_Solr
DigitalOcean Solr Search Engine deployment with automatic inventory config

-- Specifications --

macOS: Sonoma 14.2.1

Solr version: 8.6.0

Ubuntu: 23-10-x64

-- INSTRUCTIONS --

1. Add your machine SSH to DigitalOcean account
2. Update hosts file position

   a) ansible_ssh_private_key_file (path to your public ssh file)
4. Create API token and add to your DigitalOcean project
5. Update vars files to your personal preferences

   a) Update u_token in Connection vars (api_token)

   b) Update u_ssh in Connection vars (ssh fingerprint)

   c) Update hosts_dest with your actual path to the hosts file (you can use pwd)
7. Run droplet.yml playbook to deploy new droplet on DigtalOcean and automatically update hosts inventory file
8. Connect to your Solr engine with droplet ip and 8983 port (or the one you have applied in config)

-- Droplet Delete --

If you would like to delete droplet, simply switch state of "Create Digitalocean droplet" from PRESENT to ABSENT.
