# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.define "ubuntu" 
  config.vm.hostname = "ubuntu"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu"
    vb.cpus = 2
    vb.memory = 2048
  end

end
