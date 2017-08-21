# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 2
  end
  
  config.vm.provision "shell", inline: <<SHELL
    cd /home/vagrant
    yum update -y
SHELL

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "chef_environment.yaml"
  end
end
