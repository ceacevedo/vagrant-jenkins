# Vagrant Jenkins build

Run a Jenkins instance on Ubuntu using vagrant.

## Prerequisites
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

## Installation
Build the vagrant box

```
vagrant up
```

Once your VM has booted and finished provisioning the Jenkins container, ssh into your VM by running:

```
vagrant ssh
```

and then run the next command in order to obtain the password that Jenkins provided to continue the installation on the browser.

```
docker logs jenkins 
```

Copy the password, open your browser and browse:

```
http://localhost:8080
```

Continue with the installation proccess...


