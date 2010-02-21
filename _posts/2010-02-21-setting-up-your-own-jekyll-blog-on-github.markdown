---
title: Setting up your own Jekyll blog on github
layout: post
---

I set this blog up yesterday in a about two hours yesterday. Over half of that was spent reading through documentation on how to get these projects installed and how to use the github hosting service. In the interest of saving someone else some time, I wanted to share how I set everything up.

The first thing that should be noted is that you don't have to set anything up. You can just fork [my project](http://github.com/travisj/travisj.github.com), remove my posts, edit the \_layouts and start adding your own posts. When you push your posts to github, they automatically run the files through [Jekyll](http://wiki.github.com/mojombo/jekyll/) and create your static site. The only reason you need to Install Jekyll is if you want to deploy your site somewhere else or if you want to do a lot of customization to your templates - local development is a lot easier than pushing every single change to github to see how something looks.

I setup the projects in a CentOS VMWare instance because CentOS has some great tools for installing what is needed. If you are on a Mac you could probably also use [Homebrew](http://github.com/mxcl/homebrew) to get stuff setup easily or install from source. I don't trust random snippets of code I find on the web enough to trust them on my actual machine, so sandboxing them in a virtual machine allows me to play around without worry of screwing anything up. 

I first installed Jekyll following [these intstructions](http://wiki.github.com/mojombo/jekyll/install). My OS didn't come with ruby and rubygems so I needed to run a quick 'yum install ruby rubygems ruby-devel python-pygments -y'. Pygments is a python project that adds line numbering if you use certain liquid syntax in your posts. Github renders using pygments by default so I figured I would set it up locally too.

After Jekyll is installed you can start creating your site. The first thing you should do is setup your git repo. 

1. Create a new repo at github named __your_name__.github.com
2. Follow the instructions provided by github to set up your local repo. 
3. In that repo run 'jekyll'
4. Take a look at my [\_config.yml](http://github.com/travisj/travisj.github.com/blob/master/_config.yml) and [.gitignore](http://github.com/travisj/travisj.github.com/blob/master/.gitignore). Neither is needed but help. Jekyll is going to create your site locally, but since github also creates it when you push to them, you don't need to send them the static files. When I first started playing with this stuff, I set up the project to only send github my staticly-generated files. This worked, but since they run everything through Jekyll and this is the "right" way to do things I decided to follow the new setup.
5. Start Jekyll in your root project dir with 'jekyll --server'. Any changes you make to your files will automatically get picked up and deployed to your local site.

Now that you have Jekyll set up, you should start creating and modifying your layouts. I found that looking at [other layouts](http://wiki.github.com/mojombo/jekyll/sites) was the easiest way to set up my own. Layouts are basically HTML with a little bit of liquid templating thrown in. 

When you are ready to start blogging, you create a new file in your \_posts directory named 'yyyy-mm-dd-title-of-your-post.extension' where extension can be .html, .markdown or .textile. You choose how you want your post rendered and Jekyll does the rest. I like [Markdown](http://daringfireball.net/projects/markdown/syntax) because it is so easy to use, but the others would work fine too. 

After you create your first post, you need to commit (git commit -a -m 'my first post') and then push (git push origin master). 

That's all there is to it. Your site is now live at __your_site__.github.com. Please let me know how this worked out.
