---
title: CSS Sprites
layout: post
---

When I first tried out Compass I was drawn to the project because it turned the art of creating CSS into something I could really understand as a programmer. I like being able to write functions that reduce the amount of code I have to write. After writing just a few lines of SASS, I figured that generating sprites should be a function of SASS. You should be able to add the image as if it were a standalone image and when the SASS file is processed all the images in the file should get turned into a sprite. All the offsets should be calculated for you. I was dreaming.

After doing a little searching around github, I found a project that looks to be really close to what I wanted. [Sprite](http://github.com/gistinc/sprite) takes a config file and generates a sprite for you. It then creates the CSS or SASS mixin for you! I am looking forward to trying this project out.

Anyone know of a better way to incorporate sprites into your development? While this sounds easy, I am not going to stop looking until I find an even easier sprite method.

*Update 02/25/2010*: I am not as experienced installing ruby gems as I would have hoped. I am stalled on playing with this project as I try to get RMagick installed. I think the problem is with my install of ImageMagick, but need to keep investigating. I have install ImageMagick from both source and binary and it makes no difference. I am hoping to get some time this weekend to really dig into it and get something working.
