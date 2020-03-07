# oshiropantsu-vagrant

This is a vagrant environment for oshiropantsu project

## Private IP

You can change the private IP of the vm by changing line 34 of `Vagrantfile`:
```
  config.vm.network "private_network", ip: "192.168.33.101"
```

## Prerequisites

You need to install Virtual box and vagrant on your computer to make vagrant box work
* [Virtual Box](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

## Boot of vm

Inside the folder containing the `Vagrantfile`:
```
vagrant up
```

It will need some time to download the base box.

## SSH into the vm

Inside the folder containing the `Vagrantfile`:
```
vagrant ssh
```

Furthermore, the information required for ssh is as below:
```
Hostname: 192.168.33.101 (The private ip that you set above)
Port: 22
Username: vagrant
Password: vagrant
```
Private key file is located at `.vagrant\machines\default\virtualbox\private_key` which is the same directory containing the `Vagrantfile`.

## Shut down of vm

Inside the folder containing the `Vagrantfile`:
```
vagrant halt
```

## Installation of docker config

After ssh into the vm, you can directly use git to pull the docker config from [here](https://github.com/wcqiter/oshiropantsu-docker)
```
git clone https://github.com/wcqiter/oshiropantsu-docker oshiropantsu-docker
```

Then you can follow the [guide](https://github.com/wcqiter/oshiropantsu-docker/blob/master/README.md) in docker config to proceed.
