---
layout: post
title: "Day Thirteen - May 14th"
date: 2015-05-14 19:42
author: Admin
categories:
- blog
- web-design
- Week 3
img: Battleship-1.jpg
thumb: thumb01.jpg
---

###<b>Is this the end of Battleships?</b>

After almost two weeks of various manifestations of battleships we are now approaching the end.
Personally, I have found new and imaginative ways to destroy this game and have ended up with something that only vaguely resembles the original classic.
That said, it works, is online and looks vaguely presentable so I suppose that is some sort of achievement.

****

What I Learnt

* Cookies - a lot of today has been spent experimenting with sessions and using them to store information on alternative players that can call opposing methods in the underlying battleships programme
* REST - GETS and PUSH are actually just language conventions for request patterns, not functional methods
* CSS - rediscovering how to use CSS and found out that can create a master layout.erb view in Sinatra that can then yield to underlying, nested layouts (the rest of your .erb files) and carry in template bootstrap CSS files

****

What was difficult

* Yeah, Cucumber testing again, did persist in getting the tests to pass but it has proved challenging all week
* Transfer of turns using sessions and maintaining state

****

What's the plan tomorrow

* Get the weekend challenge and go from there...

****

Code of the day...

The way we ended up managing individual turns

    elsif @@turn != @player
      redirect to '/game/fire?error=wrongturn'

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
