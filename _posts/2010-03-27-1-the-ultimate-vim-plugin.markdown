---
title: The Ultimate Vim Plugin
layout: posts
---

I switched to Vim from [Textmate](http://macromates.com/) and the hardest feature I had to leave behind was Textmate's Command-T function. When you type Command-T, Textmate indexes all the files in your working directory and allows you to search for the file you want to edit, just by typing a few letters in the filename. The letters don't even have to be next to each other, just in the filename. I used this featrue all the time. For instance, if I wanted to open some_class.php, I could search for 'sc' and most hit enter to edit the file.

Vim obviously doesn't have this feature natively, but last night I came across a plugin project on GitHub that adds it! The project is called [Command-T](http://github.com/wincent/Command-T) and it was pretty easy to install. The only catch I came across was that vim requires ruby support, which I did not have. I had to rebuild vim, which ended up being easier than I expected.

To tell if you already have ruby support:

	vim --version | grep ruby

If you see "+ruby" then you already have ruby support. If you see "-ruby" then you are going to need to rebuild. I had to install ncurses-devel, and figuring that our took some googling, but after that, installation was simple:

	# ./configure --disable-selinux --enable-rubyinterp
	# make
	# make install

Then install the plugin and start enjoying Command-T functionality in Vim. 

A couple notes from my install:

1. I had to add 'syntax on' to my .vimrc. It seems that syntax highlighting was the default in my previous version of vim, but not with my new one.
1. I added 'let mapleader = ","' to my .vimrc. The default leader key is '\', but I saw a few places that people like to remap the leader key to ',' and since that is a much easier keystroke I decided to do the same.

I am still just getting started with this plugin again, but am really enjoying it. If you try out the plugin and find any other great tricks, please share what you find.
