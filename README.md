Upgrading Ansible from version 2.4 to 2.14
==========================================

This directory contains example playbooks and roles created such that they work
with Ansible 2.4. They can be used in an exercise of upgrading them to
Ansible 2.14.

Running hosts in Vagrant
------------------------

We tested and used the playbooks against the hosts that can be spun up using
Vagrant.


```shell
vagrant up
    cd /code/
    ansible-playbook -i inventory.yml playbook.yml
    curl -Lk worker-centos
    curl -Lk worker-debian
vagrant destroy -f

# to sync files between local and remote machines after vagrant up, watches for changes
vagrant rsync-auto
```
