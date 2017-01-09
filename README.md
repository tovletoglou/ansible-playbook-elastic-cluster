# Ansible playbook for Elasticsearch cluster

This is an Ansible playbook to setup a Vagrant, multi VM system.

For more information about the Vagrant machines see [vagrant-multi-vm](https://github.com/tovletoglou/vagrant-elastic).

## Requirements

Tested on CentOS 7

## Get started

1. Clone this project

  ```
  git clone https://github.com/tovletoglou/ansible-playbook-elastic-cluster.git
  ```

2. Run the playbook `playbook_ansible.yml`. It will get all the roles and put them in `roles/ansible-role-name`.

  ```
  ansible-playbook -i hosts_vagrant playbook_ansible.yml
  ```

3. Run the playbook `playbook_vagrant` to initialize the servers.

  ```
  ansible-playbook -i hosts_vagrant playbook_vagrant.yml
  ```

4. Run the playbook `playbook_scrapy` to setup the scrapy servers.

  ```
  ansible-playbook -i hosts_vagrant playbook_scrapy.yml
  ```

5. Run the playbook `playbook_elastic` to setup Aegir.

  ```
  ansible-playbook -i hosts_vagrant playbook_elastic.yml
  ```

## Extra info

### git_check_status.sh

The `git_check_status.sh` is a bash script used to check the `git status` for the roles (as sub-projects)
