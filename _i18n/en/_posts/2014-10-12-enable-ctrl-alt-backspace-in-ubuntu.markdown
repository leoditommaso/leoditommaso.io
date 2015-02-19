---
title:  "Enable Ctrl+Alt+Backspace in Ubuntu"
date:   '2014-10-12 01:41:21 -03:00'
summary: I always liked the Ctrl+Alt+Backspace combination to kill the desktop
  environment in Linux, for different reasons, because the graphical interface
categories: ubuntu
tags: os ubuntu tricks
---

I always liked the Ctrl+Alt+Backspace combination to kill the desktop
environment in Linux, for different reasons: because the graphical interface
just freezes or maybe because I reconfigured the desktop environment and it is a
fast way to restart the X server. But since 10.04, Ubuntu has disabled this key 
combination. Luckily for us (or may I say for me perhaps), enabling it again is
really simple.

With the text editor of your choice, open the file */etc/default/keyboard* and
change the following option.

{% highlight bash %}
XKBOPTIONS="terminate:ctrl_alt_bksp"
{% endhighlight %}

Enjoy!
