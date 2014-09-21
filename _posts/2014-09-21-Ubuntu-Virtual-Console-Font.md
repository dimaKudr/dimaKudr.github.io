---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, Console, font]
---
{% include JB/setup %}

On my laptop default Virtual Console font (`Ctrl + Alt + F[1-6]`) is too small to be convenient for me. I have tried several solutions but none of them was working for all virtual consoles in persistent way. Until I have found this one. It works like a charm on Ubuntu 14.04.

So you just should run in one of virtual consoles:

    sudo dpkg-reconfigure console-setup

It will ask you couple questons. As for me TerminusBold font of 24x12 size looks pretty good. And that's it.
