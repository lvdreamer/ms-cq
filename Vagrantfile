# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.provider "virtualbox" do |v|
    v.name = "microservice"
    v.memory = 3072
    v.cpus = 2
  end

  config.vm.box_check_update = true

  #Private_network Settings
  config.vm.network "private_network", ip: "192.168.100.2"

  #SSH
  config.ssh.forward_agent = true

  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"

  #Provision scripts
  config.vm.provision "shell", path: "provision.sh"
   
end
