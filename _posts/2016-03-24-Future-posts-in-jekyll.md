---
layout: post
title: Scheduling future posts in Jekyll
categories: jekyll
disqus: true
---

One of the handy features ok jekyll is to easily schedule future blog posts. The most conveniant way in my opinion is to give the file a date in the future. Jekyll keeps ignoring articles, that have a higher date than today. To preview the posts in develop mode, you simply add the `--future` flag when running jekyll:
`jekyll serve -w --future`
This will show all posts, even with future dates. That way you can review them in your layout and correct things if you need.  
Another option is to add `published: true/false` to your posts and switch the flag when the post is ready. With `jekyll server -w --unpublished` you can display the posts locally.  

Personally I prefer setting future dates, because I can finish the posts and leave it untouched. For the deployment I can simply pull run jekyll once a day and push the changes to the server.
