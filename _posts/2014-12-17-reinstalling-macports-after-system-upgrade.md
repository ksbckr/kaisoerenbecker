---
layout: post
title: Reinstalling macports after system upgrade
categories: osx
disqus: true
---

I recently switched my work Macbook and just wanted a clean install, which kept me from reinstalling from TimeMachine Backup. So as usual, I had the problem that after configuring the base system I needed to install macports. After some searching I came across the ability to dump a list of installed ports and reinstall them after an OS upgrade or reinstall.
To backup your list of installed ports simply execute the following command:  
`port -qv installed`  
The easiest way is to save them directly to a file:  
`port -qv installed < myports.txt`  
After that you just uninstall all ports and do a cleanup:  
{% highlight python %}
sudo port -f uninstall installed
sudo port clean all
{% endhighlight %}
To restore your ports, macports provides a script that takes your list of installed ports as a parameter. You can directly grab it from [macports svn][restore] or from terminal with curl and run it:  

{% highlight python %}
curl -O https://svn.macports.org/repository/macports/contrib/restore_ports/restore_ports.tcl
chmod +x restore_ports.tcl
sudo ./restore_ports.tcl myports.txt
{% endhighlight %}
The complete guide can be found [here][guide].

[restore]: http://web.archive.org/web/20141217145451/https://svn.macports.org/repository/macports/contrib/restore_ports/restore_ports.tcl
[guide]: http://web.archive.org/web/20141217145451/https://trac.macports.org/wiki/Migration#Updatemacports.conf