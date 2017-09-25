# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
#  config.vm.box = "ubuntu-trusty64-1"
  config.ssh.username = "vagrant"
	config.vm.network :forwarded_port, guest: 80, host: 8080, id: 'web'
	config.vm.provision :ansible do |ansible|
    ansible.playbook = "apt.yml"
  end
end
