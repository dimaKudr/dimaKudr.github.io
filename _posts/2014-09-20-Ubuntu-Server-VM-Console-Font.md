---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, VirtualBox, Console, font]
---
{% include JB/setup %}

Solution described below is the simplest that I have found. And what is more important it is working for Ubuntu Server 14.04.1 :) Here is the link to [original post](http://jonforums.github.io/general/2012/12/18/ubuntu-console-vm.html)

## Step 1. Update GRUB2

Configure grub2 to use a different display resolution and grow the tiny VirtualBox VM window.
On my laptop setting **GRUB_GFXMODE=1024x768x24** was the perfect size:
<ul>
<li>edit grub settings <code>sudo vim /etc/default/grub</code></li>
<li>set <code>GRUB_GFXMODE=1024x768x24</code></li>
<li>reflect changes to active bootloader <code>sudo update-grub</code></li>
</ul>


## Step 2. Update Initial RAM Disk

<ul>
<li>edit console settings <code>sudo vim /etc/default/console-setup</code></li>
<li>set <code>FONTFACE="TerminusBold"</code></li>
<li>set <code>FONTSIZE="24x12"</code></li>
<li>copy font file archive <code>sudo cp /usr/share/consolefonts/Lat15-TerminusBold24x12.psf.gz /etc/console-setup</code></li>
<li>go to console-setup folder <code>cd /etc/console-setup</code></li>
<li>unpack font file <code>sudo gzip -d Lat15-TerminusBold24x12.psf.gz</code></li>
<li>update init RAM disk <code>sudo update-initramfs -u</code></li>
<li>reboot to see changes <code>sudo reboot</code></li>
</ul>
