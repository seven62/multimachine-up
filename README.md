# Vagrant Multi-machine Setup

> For local development & testing (specifically deployments via Ansible)

spin up vagrant boxes using included Vagrantfile

vagrant validate
vagrant up
vagrant global-status

validate each host: vagrant ssh vm#


### add to inventory

```
[servers]
vm1
vm2
vm3
```


### enable ssh with password

vagrant ssh vm1-3
sudo vi /etc/ssh/sshd_config
change line 65 to PA yes
restart sshd


### add boxes you local hosts file

sudo vim /etc/hosts:

```
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1       localhost
255.255.255.255 broadcasthost
::1             localhost
10.0.15.11      vm1
10.0.15.12      vm2
10.0.15.13      vm3
```


### role structure




### ansible.cfg




### role defaults



### role tasks


### ssh-keygen

ssh-keygen -t rsa -C "local vagrant dev via ansible"
name key appropriately






from project folder:
`ansible all -i inventory.ini -m ping --become -Kk`  



ansible-playbook preconfigure.yml -i inventory.ini -Kk
