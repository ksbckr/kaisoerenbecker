---
layout: post
title: Display whitespaces in Sublime Text
categories: app
disqus: true
---

Sublime Text is my main editor and I’m using it all day long. The flexibility and extendability is what I like most. Sometimes there is just one thing you want to change about your editor and keep searching through the prefs all day long. With Sublime Text this is quite handy, because all the settings are kept in a json config.
To enable whitespaces being displayed all the time (not only when selected), just paste `"draw_white_space": "all"`  
into `Sublime Text -> Preferences -> Settings - User` after the opening `{`.  
The file contents should look like  
{% highlight bash%}
{
    ...
    "draw_white_space": "all"
    ...
}
{% endhighlight %}