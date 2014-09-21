---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, VirtualBox, Networking]
---
{% include JB/setup %}

##Goal:
* The Host should be able to connect to the Guest (the virtual machine)
* The Guest should be able to access the outside world (intranet / internet)
* Use fixed IP address, no problems with DHCP at all.

##At Host

* Add Host-Only network adapter in Virtual Box preferences

![virt-box-settings.png]({{ site.url }}/assets/images/virt-box-settings.png)

* Check sub-network in adapter settings

![virt-box-adapter-settings.png]({{ site.url }}/assets/images/virt-box-adapter-settings.png)

* Select Host-Only adapter in virtual machine settings

![vm-adapter-settings.png]({{ site.url }}/assets/images/vm-adapter-settings.png)

##At Virtual Machine

* Edit its interfaces settings

    cd /etc/network/
    sudo vim interfaces

* Change eth0 to use static IP

    iface eth0 inet static

* Add following lines:

    address 192.168.56.4
    netmask 255.255.255.0
    gateway 192.168.56.1
    dns-nameservers 192.168.1.1

Now you should be able to connect from Host to Guest and vice versa using ssh.
