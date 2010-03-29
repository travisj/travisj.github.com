---
title: Custom domains with Wordpress MU
layout: post
---

I have been hosting blogs for my family members for a long time and recently decided to switch over to [Wordpress MU](http://mu.wordpress.org). Wordpress MU allows you to maintain one Wordpress installation (one code base, one database, etc) and give multiple users their own blog. It works by allowing you to either choose a subdomain or first level directory for each user's blog. I wanted to give my family the ablity to have their own domains for a blog - not just be on a subdomain.

I was able to do this by creating (or rather modifying) a special Wordpress MU file call sunrise.php. If a sunrise file is placed in the wp-content folder, it is processed. In it you can override the blog id that WP will use. 

With that in mind, [my sunrise.php](http://github.com/travisj/Sunrise) file examines the full URL of the request to determine if it matches any of the custom domains in a special custom domain table.

So if you are adventurous, try to follow my basic instructions for the project and set up custom domains for your blogs too. I will be doing more work on this and will keep the project up to date as I learn more about it. 

Let me know how it goes.
