# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  #config.vm.synced_folder "nextflow", "/home/vagrant/nextflow"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
      ansible.sudo = true
      ansible.playbook = 'playbook.yml'
      ansible.verbose = false
  end
end
