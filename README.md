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

To access the Jenkins server

```
http://localhost:9005
```

or, add the following line to the hosts file

```
127.0.0.1   jenkins.local
```

and then run the server with

```
http://jenkins.local:9005
```