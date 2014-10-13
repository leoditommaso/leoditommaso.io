---
layout: post
title:  "The one second webserver"
date:   '2014-10-12 00:13:21 -03:00'
author: "Leandro Di Tommaso"
summary: I've found myself many times in the need to share something quickly
  with a colleague or a friend and ended up copying the files to an USB flash drive,
categories: webserver tricks
---

I've found myself many times in the need to share something quickly with a
colleague or a friend and ended up copying the files to an USB flash drive,
sharing a folder in my computer or even creating and SSH user. Too much for such
simple thing, and Python seems to think the same as it rescue us with just one
single line.

{% highlight python %}
python -m SimpleHTTPServer 4500
{% endhighlight %}

The command above starts a web server with its root being the directory where
it's executed. Perfect, right? The last parameter is the port the webserver will
listen on. It isn't required so you can omit it and the server will use port
8080 by default.

But come on, having to remember such thing is too much work for us, lazy people.
So an alias is the icing on the cake.

{% highlight bash %}
echo "alias web='python -m SimpleHTTPServer 4500'" >> ~/.bash_profile
{% endhighlight %}

That's fantastic! Now when you need to share a file with a friend just execute
the web command in the right directory and voilà. Just remember to open that
port on your firewall...
