#---
layout: post
category : Vim
tagline: Vim Plugins
tags : [Ubuntu, Vim, Plugins]
---
{% include JB/setup %}

vim-config created by Derek Wyatt was used as a base.
https://github.com/derekwyatt/vim-config

As I just started learning Vim, list of bundles used by Derek looks overwhelming to me. So I removed all of them except vim-scala. And will add some of them back in the future.

Included plugins:
* vim-airline. How to: [install patched fonts](http://dimakudr.github.io/vim/2014/07/16/Vim-Airline-fonts/)
* vim-scala
* vim-gitgutter

Also I have added gvimrc separate config for gVim.

To install it, do the following:
* wipe out your `~/.vimrc` file and `~/.vim` directory (back up if you wish)
* `git clone https://github.com/dimaKudr/vim-configs.git ~/.vim`
* `cd ~/.vim/bundle && ./get`
* `ln ~/.vim/vimrc ~/.vimrc`
* `ln ~/.vim/gvimrc ~/.gvimrc`
*  if you have ~/.gtkrc-2.0 file, hen add there content of just clonned ~/.vim/gtkrc-2.0.
   Otherwise configure a link `ln ~/.vim/gtkrc-2.0 ~/.gtkrc-2.0`.
   This will rid off right and bottom gray bordrs in gVim fullscreen mode.
* start Vim

To update bundles (if necessary):
* `cd ~/.vim && ./update`

Note: Add to .bashrc following lines to enable 256 colors support in Terminal.
```
if [ -n "$DISPLAY" -a "$TERM" == "xterm" ]; then
    export TERM=xterm-256color
fi
```

