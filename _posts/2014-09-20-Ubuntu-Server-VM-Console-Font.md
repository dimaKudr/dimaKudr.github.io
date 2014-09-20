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
- edit grub settings `sudo vim /etc/default/grub`
- set `GRUB_GFXMODE=1024x768x24`
- reflect changes to active bootloader `sudo update-grub`

## Step 2. Update Initial RAM Disk
- edit console settings 'sudo vim /etc/default/console-setup'
- set 'FONTFACE="TerminusBold"'
- set 'FONTSIZE="24x12"'
- copy font file archive 'sudo cp /usr/share/consolefonts/Lat15-TerminusBold24x12.psf.gz /etc/console-setup'
- go to console-setup folder 'cd /etc/console-setup'
- unpack font file 'sudo gzip -d Lat15-TerminusBold24x12.psf.gz'
- update init RAM disk 'sudo update-initramfs -u'
- reboot to see changes 'sudo reboot'

