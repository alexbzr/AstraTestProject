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
end