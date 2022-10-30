# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.provider "virtualbox" do |vb|
  #   vb.gui = true
    vb.name = "ubuntu-ansible"
    vb.check_guest_additions = false
    vb.memory = "4096"
    vb.cpus = "2"
  end
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  
end