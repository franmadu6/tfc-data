# -*- mode: ruby -*-
# vi: set ft=ruby :
 
Vagrant.configure("2") do |config|
  config.vm.define :controller do |controller|
    controller.vm.box = "debian/buster64"
    controller.vm.hostname = "controlador"
    controller.vm.network :public_network,:bridge=>"wlo1",
      use_dhcp_assigned_default_route: true
    controller.nfs.verify_installed = false
    controller.vm.synced_folder '.', '/vagrant', disabled: true
    controller.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
  end
 config.vm.define :worker1 do |worker1|
    worker1.vm.box = "debian/buster64"
    worker1.vm.hostname = "worker1"
    worker1.vm.network :public_network,:bridge=>"wlo1",
      use_dhcp_assigned_default_route: true
    worker1.nfs.verify_installed = false
    worker1.vm.synced_folder '.', '/vagrant', disabled: true
    worker1.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
  end
  config.vm.define :worker2 do |worker2|
    worker2.vm.box = "debian/buster64"
    worker2.vm.hostname = "worker2"
    worker2.vm.network :public_network,:bridge=>"wlo1",
      use_dhcp_assigned_default_route: true
    worker2.nfs.verify_installed = false
    worker2.vm.synced_folder '.', '/vagrant', disabled: true
    worker2.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
  end
end
