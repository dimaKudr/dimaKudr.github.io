---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, VirtualBox, Networking]
---
{% include JB/setup %}

Last time I described how to [configure networking]({{ site.url }}{% post_url 2014-09-21-Ubuntu-VirtualBox-Networking %}) for Ubuntu Server running as a guest OS at VirtualBox.

There is one more thing that should be mentioned. In that configuration **Guest does not have access to the Internet**.

This could be fixed by enabling Internet connection sharing in Host Network settings.

* From the network menu open "Edit Connections..." dialog
* Select your current active Internet connection and click "Edit..."

![connection-settings.png]({{ site.url }}/assets/images/connection-settings.png)

* In the "IPv4 Settings tab", select Method: "Shared to other computers"
* Reconnect, so it gts new IP adresses
* Click on "Connection Information" in the network menu to see new adresses
* Update Guest OS network configuration with Host new arrdesses.


##Note!
Unfortunately there is a bug in Ubuntu that brakes Host's connection to the Internet when you choose sharing mode. It described in details [here](https://bugs.launchpad.net/ubuntu/+source/network-manager/+bug/865001). And [here](https://help.ubuntu.com/community/Internet/ConnectionSharing) is related Ubuntu documentation article. I tried a workaround mentioned in comments to bug. For some reason it did not help.

My workaround is to switch back to NAT in that rare moments when I need Internet at the Guest. It is not convenient, but I did not find anything else yet.
