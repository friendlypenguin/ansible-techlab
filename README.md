# Ansible-Techlab

Techlab to learn ansible!

We assume, that each user has three virtual machines available:
- a control host
- two nodes called `node1` and `node2`

## Vagrant Setup
```
control 192.168.122.50
node1 192.168.122.51
node2 192.168.122.52

user: vagrant
password: vagrant
```
With vagrant you can create those vm's on your local machine, make sure vagrant is installed
```
yum install vagrant

# install libvirt provider
vagrant plugin install vagrant-libvirt

# setup vm's
vagrant up

# remove all vms
vagrant destroy -f
```
