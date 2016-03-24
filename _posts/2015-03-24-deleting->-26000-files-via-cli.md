---
layout: post
title: Deleting > 26000 files via CLI
categories: bash
disqus: true
---

I came across a problem today, were I wanted to delete about 49000 files in a folder with a specific file name.
First thing I tried was `rm -f *foo.xml` but permanently got the error  
`-bash: /bin/rm: Argument list too long`.
In short, the problem is that the command exceeds `getconf ARG_MAX`, which is set to 262144 on my machine (depends on your linux kernel).  
So how to workaround this problem? Just use a simple for loop in bash:  
`for f in *foo.xml; do rm "$f"; done`  
Optionally you could create a bash function that accepts a filename as an argument.
Further Information can be found here.