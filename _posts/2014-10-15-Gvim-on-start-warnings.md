---
layout: post
category : Vim
tagline: Vim configuration
tags : [vim, bash]
---
{% include JB/setup %}

On Gvim start it prints to console several warnings:
`(gvim:4054): GLib-GObject-WARNING **: Attempt to add property GnomeProgram::sm-connect after class was initialised
(gvim:4054): GLib-GObject-WARNING **: Attempt to add property GnomeProgram::show-crash-dialog after class was initialised
(gvim:4054): GLib-GObject-WARNING **: Attempt to add property GnomeProgram::display after class was initialised
(gvim:4054): GLib-GObject-WARNING **: Attempt to add property GnomeProgram::default-icon after class was initialised`

In order to remove them, just add the following to .bashrc file: `alias gvim="gvim 2>/dev/null"`