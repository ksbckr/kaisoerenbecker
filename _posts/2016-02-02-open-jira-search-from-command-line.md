---
layout: post
title: Open JIRA search from command line
categories: bash
disqus: true
---

In addition to my last post, I made a little bash script for opening the search dialog of a custom JIRA instance from command line. The script works on OS X and opens a new tab in your default browser: 

{% highlight bash%}
jira_search() {
   #configure your JIRA url here:
   url='https://my.jira.url'

   url+='/jira/issues/?jql=text~"'
   if [ "$#" == "1" ]; then
      url+="$a"
   else
      url+="$1"
      for a in ${@:2}
      do
         url+=" "
         url+="$a"
      done
   fi
   url+='"'
   open "$url"
} alias sj=jira_search
{% endhighlight %}

Just put this snippet into your bash.rc or in a seperate bash_alias file.
Don’t forget to run
`source .bash_aliases` (or wherever you put it)
to make the function available. 