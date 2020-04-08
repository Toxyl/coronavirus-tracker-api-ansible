# Ansible Playbook "Coronavirus Tracker API Node"
An Ansible playbook to deploy a server running the Coronavirus Tracker API (see https://github.com/ExpDev07/coronavirus-tracker-api)

## Requirements
Ansible won't work without Python installed on the target host, please install it before running this playbook.
Also, this playbook has been made for and tested with Ubuntu 18.04.3 x64 hosts but should, at least in theory, work for any Debian based host. 

## How to run
Make sure you have your **public** SSH key added to `roles/apinode/files/ssh` and update the `accounts` variable in `roles/apinode/vars/main.yml` accordingly.
Also make sure to adjust `hosts.ini` to match your SSH config (usually in `$HOME/.ssh/config`).

Now run `ansible-playbook -C -l api main.yml` and confirm that everything looks ok, then run `ansible-playbook -l api main.yml` to start the deployment process.
