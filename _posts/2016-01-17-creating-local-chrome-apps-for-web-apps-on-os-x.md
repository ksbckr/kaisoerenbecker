---
layout: post
title: Creating local Chrome apps for web apps on OS X
categories: app
disqus: true
---

I use a lot of Google services for business and private purposes. Both Inbox and Play Music for example have great web apps which are easy to use. But there is no native desktop application which I would prefer in some ways (independent window, not bound to a specific browser, ..)  
Gladly there is a simple tool to generate a local app out of a web app making use of Google Chrome as a wrapper. The tool is called **createGcApp**, created by [Max Kostow][mk], and can be found on [github][gh].  
When starting the tool, simply enter an app name, insert the URL you wish to bind and select an image as an icon. createGcApp will create a seperate chrome profile, so none of your existing settings will be touched. Starting the created app for the first time, you will be asked for your credentials (if you use it with service that need authentication of course).

[mk]: "http://maxkostow.com/"
[gh]: "https://github.com/maxkostow/createchromeapp"