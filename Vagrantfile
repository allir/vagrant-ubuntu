# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  config.vm.define "ubuntu" 
  config.vm.hostname = "ubuntu"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu"
    vb.cpus = 2
    vb.memory = 2048
    vb.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
  end

  config.vm.provision "environment-file", type: "file", source: "ubuntu.env", destination: "/tmp/ubuntu.sh"
  config.vm.provision "setup-environment", type: "shell", inline: "mv /tmp/ubuntu.sh /etc/profile.d/"

  config.vm.provision "setup", type: "shell", inline: $setup

end

$setup = <<SCRIPT
set -euo pipefail
export DEBIAN_FRONTEND=noninteractive
apt-get -qq update
apt-get install -y \
  linux-tools-common \
  build-essential \
  dstat \
  ngrep \
  tldr
SCRIPT
