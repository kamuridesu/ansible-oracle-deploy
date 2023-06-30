# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  (1..3).each do |index|
    config.vm.define "vm_#{index}" do |box|
      box.vm.box = "debian/bullseye64"
      box.vm.box_check_update = false
      box.vm.network "private_network", ip: "192.168.56.1#{index}"
      box.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        vb.cpus = "1"
      end
    end
  end
end
