# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # config.vm.box_check_update = false

  # disable default shared folder
  config.vm.synced_folder ".", "/vagrant", disabled: false

  config.vm.define "prometheus" do |vm_config|
      vm_config.vm.hostname = "prometheus"
      vm_config.vm.network :private_network, ip: "192.168.33.11"
  end

  config.vm.provider "virtualbox" do |vb|
      # Customize the amount of memory on the VM:
      vb.memory = "2048"
      vb.linked_clone = true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup-workshop.yml"
    ansible.become = true
    ansible.groups = {
       "training-prometheus" => [ "prometheus" ],
       "vagrant" => [ "prometheus" ],
    }

  end

end
