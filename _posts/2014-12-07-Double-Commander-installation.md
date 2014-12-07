---
layout: post
category : DoubleCommander
tagline: Double Commande installation
tags : [Double Commander]
---
{% include JB/setup %}

Unfortunately installing Double Commander via Software Center does not work.
Installation looks successful but application does not appear in Dash.

So, to install it manually, do the following:

* add Double Commander repo to apt-get:
`sudo add-apt-repository ppa:alexx2000/doublecmd`

* install Double Commander GTK package
`sudo apt-get install doublecmd-gtk`

* It should be enough, but in my case in DC app keyboard does not work.
 And to solve it I have installed QT package on top of GTK
`sudo apt-get install doublecmd-qt`