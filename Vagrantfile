# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "box-cutter/centos67"
  config.vm.network :private_network, ip: "192.168.101.10"

  config.vm.provision :ansible do |ansible|
    ansible.galaxy_role_file = "requirements.yml"
    ansible.galaxy_roles_path = "roles/"
    ansible.playbook = "playbook.yml"
  end
end
