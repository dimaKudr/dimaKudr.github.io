---
layout: post
category : Ubuntu
tagline: Install IDEA at Ubuntu
tags : [Ubuntu, Java, IDEA]
---
{% include JB/setup %}
Download IntelliJ IDEA CE from `www.jetbrains.com/idea/download/`. Extract ideaIC-XX.Y.Z.tar.gz using:

`tar -zxvf ideaIC-XX.Y.Z.tar.gz`

Become root:

`sudo -i`

Move the extracted folder to `/opt/idea`:

`mv ideaIC-XX.Y.Z /opt/idea`

Create a desktop file and install it:

`gvim idea.desktop`

Copy the following to the idea.desktop file (More info on .desktop files `http://www.nautilus-actions.org/?q=node/377`):

    [Desktop Entry]
    Name=IntelliJ IDEA
    Type=Application
    Exec=idea.sh
    Terminal=false
    Icon=idea
    Comment=Integrated Development Environment
    NoDisplay=false
    Categories=Development;IDE;
    Name[en]=IntelliJ IDEA

Execute the following command to automatically install it in the Unity:

`desktop-file-install idea.desktop`

Create a symlink in `/usr/local/bin` using:

    cd /usr/local/bin
    ln -s /opt/idea/bin/idea.sh

For IDEA icon to be displayed in Dash, IDEA icon can be added as:

`cp /opt/idea/bin/idea.png /usr/share/pixmaps/idea.png`

That's it. Now, you can launch IDEA from Ubuntu Dash.
