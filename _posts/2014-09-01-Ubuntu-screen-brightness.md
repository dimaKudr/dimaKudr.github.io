---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, brightness]
---
{% include JB/setup %}

On my Asus Zenbook laptop by default screen brightness is set to maximum every time I start Ubuntu or just open the lid. This script sets initial screen brightness to minimum value on the before mentioned ocasions. This is more convenient to me.

Put this .conf file to `/etc/init/` folder

{% gist dimaKudr/c3c3c803beb03f085871 %}
