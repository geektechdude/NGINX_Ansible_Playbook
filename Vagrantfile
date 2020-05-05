# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
   config.vm.box = "ubuntu/xenial64"
   
   config.ssh.insert_key = false
   
   config.vm.synced_folder ".","/vagrant", disabled: true

   config.vm.provider:virtualbox do |v|
    v.memory = 2048
    v.linked_clone = true
   end

   config.vm.define "nginx1" do |nginx|
    nginx.vm.hostname = "nginx1.test"
    nginx.vm.network:private_network, ip:"192.168.28.74"
   end

  
end
