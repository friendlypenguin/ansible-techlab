# Ansible-Techlab

Techlab to learn ansible!

We assume, that each user has three virtual machines available:
- a control host
- two nodes called `node1` and `node2`

Unless otherwise specified, your working directory for all labs is `/home/ansible/techlab/`.

Some good advise:

- Always read all the tasks first. Some tasks might not be clear until you get the whole scope of the lab
- Open a terminal that you use only for ansible-doc (see later) and one terminal that you use for ad hoc commands (see later) to check the result of your plays.
- Copypaste all the filenames and other information from the labs to your playbooks. You will do much lesser mistakes.

## Vagrant Setup (Optional)
You can do the labs with any linux servers you'd like. An easy solution would be to use vagrant. For more information about vagrant search the webs. With the vagrant setup provided with this lab you can use three local CentOS virtual machines using kvm. 

WARNING: The following passwords are not secure and intended only to be used with local virtual machines not reachable from outside of the virtualization host.

```
control 192.168.122.50
node1 192.168.122.51
node2 192.168.122.52

user: vagrant
password: vagrant
```
With vagrant you can create those vm's on your local machine, make sure vagrant is installed
```
### Install vagrant on CentOS/RHEL
# yum install vagrant
### Install vagrant on Debian/Ubuntu
# apt install vagrant

### install libvirt provider
# vagrant plugin install vagrant-libvirt

### setup vm's
# vagrant up

### remove all vms
#vagrant destroy -f
```
