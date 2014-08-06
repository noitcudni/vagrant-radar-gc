# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  Vagrant.require_version ">= 1.4.3"


  config.vm.define :radar do | radar |    
    radar.vm.box = "ubuntu/trusty64"
    
    # Create a private network
    radar.vm.network :private_network, ip: "192.168.1.2"
    radar.vm.hostname = "radar"
    
    #radar.vm.synced_folder  ".", "/vagrant", disabled: true
    
    #VirtualBox provider
    radar.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
      vb.name = "radar"
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      # vb.customize ["modifyvm", :id, "--cpus", "2"]
    end
    
  end
end

