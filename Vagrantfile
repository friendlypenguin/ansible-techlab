# -*- mode: ruby -*-
# vi: set ft=ruby :
# ensure ssh-password login
$script = <<-SCRIPT
sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config
systemctl restart sshd
SCRIPT
Vagrant.configure("2") do |config|
    config.vm.define "control" do |control|
        control.vm.box = "centos/8"
        control.vm.hostname = "control"
        control.vm.network "private_network", ip: "192.168.122.30"
        control.vm.provision "shell",
          inline: $script
    end
    config.vm.define "node1" do |node1|
        node1.vm.box = "centos/8"
        node1.vm.hostname = "node1"
        node1.vm.network "private_network", ip: "192.168.122.31"
        node1.vm.provision "shell",
          inline: $script
    end
    config.vm.define "node2" do |node2|
        node2.vm.box = "centos/8"
        node2.vm.hostname = "node2"
        node2.vm.network "private_network", ip: "192.168.122.32"
        node2.vm.provision "shell",
          inline: $script
    end
end
