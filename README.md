# vagrant-almalinux

## What is Vagrant?

Using VirtualBox is a good start to learn virtualization. However, it takes time to choose and download an image, configure the virtual machine in the graphical view... That's why I strongly suggest Vagrant, an efficient solution to create virtual machine IN your shell!

> Vagrant isolates dependencies and their configuration within a single disposable, consistent environment, without sacrificing any of your existing tools. To learn more about the benefits of Vagrant, read the "Why Vagrant?" introduction page.
The getting started tutorials use Vagrant with VirtualBox, since it is free and available on every major platform. Vagrant can work with many other providers.

More details on the official Vagrant [website](https://developer.hashicorp.com/vagrant/tutorials/getting-started/getting-started-index).

## Installation of a AlmaLinux 8 virtual machine

To have the support of the [KVM](https://www.linux-kvm.org/page/Main_Page) for developping LXC containers in this virtual machine, I've choosen the [libvirt provider](https://github.com/vagrant-libvirt/vagrant-libvirt) instead of VirtualBox (by default).

You can execute the following commands to install Vagrant on an Ubuntu dist:
```
sudo apt install virtualbox
sudo apt install vagrant
```
Then, you have to install the libvirt provider:
```
vagrant plugin install vagrant-libvirt
```
Finally you can launch the virtual machine thanks to the Vagrantfile:
```
vagrant up --provider=libvirt
vagrant ssh
```

Of course, you can customize the Vagrantfile for what features you want!
