# Ansible Tower Demo

Welcome to this small Ansible Tower demo.
This repository instantiates the git repo for a demo project to be created in Tower.

## Install Tower
Download Tower package on your machine:

  wget https://releases.ansible.com/ansible-tower/setup/ansible-tower-setup-latest.tar.gz
  tar -xvf ansible-tower-setup-latest.tar.gz
  cd cd ansible-tower-setup-<tower_version>

For a single node install, edit the inventory file to match the following:

  [tower]
  localhost ansible_connection=local

  [database]

  [all:vars]
  admin_password='ADMIN_PASSWORD_HERE'

  pg_host=''
  pg_port=''

  pg_database='DATABASE_NAME_HERE'
  pg_username='DATABASE_USERNAME_HERE'
  pg_password='DATABASE_PASSWORD_HERE'

Run the installer:

  ./setup.sh
  
Test your setup by visiting https://<TOWER_SERVER_NAME>/
