---
layout: post
category : Ubuntu
tagline: Ubuntu configuration
tags : [Ubuntu, Java]
---
{% include JB/setup %}

Unfortunately defaul Ubuntu package repositories contain OpenJDK only. In order to install Oracle JDK you need to add custom repo first:
`sudo add-apt-repository ppa:webupd8team/java`
`sudo apt-get update`

And then install Java 8 or 7:
`sudo apt-get install oracle-java8-installer`
`sudo apt-get install oracle-java7-installer`

The installer provides Oracle Java bundle (which includes Java JDK, JRE and the Java browser plugin). Once installed, running `java -version` in a terminal should output valid Java version.
