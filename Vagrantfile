# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.provision "shell", path: "provision/ubuntu.sh"

  config.vm.define "octopress" do |box|
    box.vm.network "private_network", ip: "192.168.33.10"
    box.vm.provision "shell", path: "provision/git.sh"
    box.vm.provision "shell", path: "provision/rvm.sh"
    box.vm.provision "shell", path: "provision/heroku.sh"
  end

end
