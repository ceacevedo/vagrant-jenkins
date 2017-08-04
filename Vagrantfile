# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  
  # uncomment for faster performance
  #config.vm.provider "virtualbox" do |vb|
  #  vb.cpus = "2"
  #  vb.memory = "4096"
  #end
  
  config.vm.define :jenkins do |jenkins|
	  jenkins.vm.network "forwarded_port", guest: 80, host: 9005
	  jenkins.vm.provision :shell, :path => "provision.sh"	  
  end
  
end
