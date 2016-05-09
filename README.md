# Ubuntu 14.04 cluster via Vagrant

This repo provides a template Vagrantfile to create a Ubuntu 14.04 cluster using the VirtualBox software hypervisor.
After setup is complete you will have three Ubuntu virtual machines running on your local machine. Please be aware that the standard memory per instance is set to 3072 MB, and the number of cpus to 2.
That means by default you'll need a machine capable to free up to 6 cpu cores and 9216 MB memory.

## Streamlined setup

1) Install dependencies

* [VirtualBox][virtualbox] 4.3.10 or greater.
* [Vagrant][vagrant] 1.6 or greater.

2) Clone this project and get it running!

```
git clone https://github.com/mesoshq/vagrant-cluster-ubuntu/
cd vagrant-cluster-ubuntu
```

3) Startup and SSH

The VirtualBox provider is the default Vagrant provider. Use this if you are unsure.

```
vagrant up
vagrant ssh ubuntu-01
```

**Description:**

`vagrant up` triggers Vagrant to download the `ubuntu/trusty64` box (if necessary) and (re)launch the instances

`vagrant ssh <hostname>` connects you to the virtual machine. The hostnames are ubuntu-01 to ubuntu-05, the IPs are from 172.17.10.101 to 172.17.10.105.

Configuration is stored in the directory so you can always return to this machine by executing vagrant ssh from the directory where the Vagrantfile was located.

[virtualbox]: https://www.virtualbox.org/
[vagrant]: https://www.vagrantup.com/downloads.html
