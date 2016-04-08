# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "sinergi/centos-65-x64"
  config.vm.network :private_network, ip: "192.168.200.10"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  config.vm.provision "ansible" do |ansible|
  	ansible.playbook = "build/ansible/playbook.yml"
  	ansible.inventory_path = "build/ansible/inventory"
  	ansible.host_key_checking = "false"
  	ansible.limit = "all"
  end

  config.vm.synced_folder ".", "/vagrant", mount_options:["dmode=775", "fmode=775"]
end
