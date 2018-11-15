# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  #use the shell provisioner and a simple bash to setup elastic.
  config.vm.provision :shell, path: "elasticsetup.sh"
  
  #provision box with 4gigs of ram and 4 cpus
    config.vm.provider "virtualbox" do |v|
      v.name = "elastic1"
      v.memory = "4096"
      v.cpus = 4
    end
  #use bionic64 18.04 from Ubuntu, name it, set it to bridged mode.  Needs changed depending on bridge interface
    config.vm.box = "ubuntu/bionic64"
    config.vm.host_name = "elastic1"
    config.vm.network "public_network", bridge: "eno1",
    use_dhcp_assigned_default_route: true
  end