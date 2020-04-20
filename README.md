# Ansible Playbook Redmine

Ansible playbook + Vagrantfile for provisioning [Redmine](https://www.redmine.org/) app to a CentOS server. The playbook installs Ruby, mySQL, Redmine, Nginx and Unicorn.

## Requires

* Ansible 2.9.6 or later

If you want to run the provisioning on VM:
* Vagrant 1.8.6 or later
* VirtualBox 5.1.6 or later

## Getting started

```
vagrant up
```

This will start the VM, and run the provisioning playbook (on the first VM startup).
Visit https://192.168.33.13 and you should see the Redmine home page.


```
ansible-playbook -i hosts playbook.yml -C
```

This will dry-run the playbook and won't affect the existing VM.

## Configuration

update `group_vars/all.yml` at your convenience.

## What's installed

- CentOS7
- Nginx, Unicorn latest
- Ruby 2.5
- mySQL 5.7
- Redmine 4.1.1
