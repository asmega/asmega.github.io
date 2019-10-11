---
layout: post
title: nginx rewrite rules for html extensions
date: 2011-07-05
---

I Just swtiched to [jekyll](http://jekyllrb.com) running in [nginx](http://nginx.net). It's simple and lightning fast.

jekyll makes all output files .html however I wanted these files to be available to people without the explicit need to have .html in the url.

I found the following [rewrite rule](http://snippets.aktagon.com/snippets/411-How-to-remove-html-from-URLs-with-nginx-rewrites) to solve exactly that.

{% highlight nginx %}
location / {
  # break if URI has .html extension
  if ($request_filename ~* ^.+.html$) {
    break;
  }
  # add .html to URI and serve file, directory, or symlink if it exists
  if (-e $request_filename.html) {
    rewrite ^/(.*)$ /$1.html last;
    break;
  }
}
{% endhighlight %}
