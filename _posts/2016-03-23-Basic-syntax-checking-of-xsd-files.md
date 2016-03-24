---
layout: post
title: Basic syntax checking of xsd files
categories: xml
disqus: true
---

As I mentioned before, I spend a lot of time working with the cli. And for a lot of tasks, there are nice little helpers build directly into the system (OS X in my case). Today I had to validate an XSD file for documentation purposes. While I use Sublime for editing and creating XML/HTML files, I often prefer cli tools to do smaller tasks. `xmllint` is an often used tool for example and perfect for simple tasks, like validating large XML or XSD files. To validate a XSD file against the w3c standard definition just use the following command:  
`xmllint --noout --dtdvalid http://www.w3.org/2001/XMLSchema.dtd file.xsd`  
If there is no output everything is fine (you can easily verify that by breaking the XML syntax like leaving a tag open).