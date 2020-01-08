# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-19.10"
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.synced_folder "./", "/polls"
  config.vm.synced_folder "./", "/vagrant"
  config.vm.provision "shell", inline: <<-EOF
    apt-get update
    apt-get --yes upgrade
    apt-get --yes install python3-venv
  EOF
end
