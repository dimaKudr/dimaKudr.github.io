---
layout: post
category : Vim
tagline: Vim Plugins
tags : [Ubuntu, Vim, Plugins]
---
{% include JB/setup %}

Airline uses several special glyphs to get the arrow effect and some custom symbols for developers.
This requires that you have a patched font on your system. Your terminal emulator must also support
patched fonts for Airline to work properly.

Gnome Terminal 3.6.2 that is default terminal in Ubuntu 14.04 supports patched fonts.
So the only task is to put fonts in the appropriate folder.

## Get patched fonts
Download the font of your choice from [powerline-fonts](https://github.com/Lokaltog/powerline-fonts).

## Install patched fonts

* Move the patched fonts to `~/.fonts`

* Update font cache `fc-cache -vf ~/.fonts/`

* Select patched font in your terminal profile. This will fix fonts for console Vim.

* Select patched font in your GVim settings.
