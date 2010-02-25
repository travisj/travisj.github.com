---
title: jquery's live() vs. bind()
layout: post
---

Anyone using jquery's event methods know a good way to test performance of the various ways to bind events to an element? I am most interested in testing .live('click', function()...) vs. .bind('click', function()...).

My instinct tells me that there would be massive overhead using live() but a few google searches tell me otherwise. I am not sure if I am reading posts by people who know what they are talking about, but they say that using live() allows you to only bind one event and then let jquery handle the event dispatching. Sounds reasonable, but then it also seems like additional overhead of having the browser fire an event on every single click, for example, and then making jquery figure out if the event matches something you are interested in.
