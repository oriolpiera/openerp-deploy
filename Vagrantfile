# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  os = "bento/ubuntu-16.04"
  net_ip = "192.168.50"

  config.vm.define :erpserver, primary: true do |erpserver_config|
    erpserver_config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 2
        vb.name = "erpserver"
    end
      erpserver_config.vm.box = "#{os}"
      erpserver_config.vm.host_name = 'erpserver.local'
      erpserver_config.vm.network "private_network", ip: "#{net_ip}.10"
    end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "erpdeploy.yml"
  end

end
