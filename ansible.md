### Installing ansible
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible



### fix the /usr/bin/python: not found error
https://www.toptechskills.com/ansible-tutorials-courses/how-to-fix-usr-bin-python-not-found-error-tutorial/

[all:vars]
ansible_python_interpreter=/usr/bin/python3

### Prepare client for ansible
In new OS distro python 2.7 is not installed we have to figure out a way to fix that

- hosts: all
  gather_facts: False
  become: true

  tasks:
  - name: install python 2
    raw: test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)



### Sending keys to client

ssh-keygen -t rsa -C "name@example.org"
ssh-copy-id user@child1.dev

Vim /etc/ansible/hosts

ansible all -m ping


### Setting up NTP 

https://www.digitalocean.com/community/tutorials/how-to-set-up-timezone-and-ntp-synchronization-on-ubuntu-14-04-quickstart

https://github.com/geerlingguy/ansible-role-ntp (with ansible)

### Setting up percona
### Setting up nginx
https://www.digitalocean.com/community/tutorials/how-to-upgrade-nginx-in-place-without-dropping-client-connections
