# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box ="ubuntu/trusty64"
    
  #Provision con shell propia
#  config.vm.define :jenkins do |jenkins|
#	  jenkins.vm.network "forwarded_port", guest: 80, host: 9005
#	  jenkins.vm.provision :shell, :path => "provision.sh"	  
#  end
  
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  
  config.vm.provider "virtualbox" do |vb|
     vb.name = "git-jenkins-pof"
     vb.memory = "2048"
     vb.cpus = 2
  end
  
  #Provision con docker e imagen oficial de jenkins
  config.vm.provision "docker" do |d|
    d.run "jenkins/jenkins:lts",
      args: "--name jenkins -p '8000:8000' -p '5000:5000' --network=host"
  end
  
end
