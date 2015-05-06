---
layout: post
title: "Day Seven - May 6th"
date: 2015-05-06 23:23
author: Admin
categories:
- blog
- web-design
- Week 2
img: battleships.jpg
thumb: thumb01.jpg
---

###<b>Battleships Continued...</b>

Its fairly late so will keep this even shorter than usual.
All in all, good day and am definitely ramping up the hours I put in.
Last full day on Battleships tomorrow and hopefully, with a basic working version, can get a full 2 player game up and running by end of tomorrow.

****

What I Learnt

* EDUF works - focused on simplifying the steps within each user story and feature test and ensured always made helpful progress rather than trying to solve the entire problem in one go
* Working with Arrays - never cease to learn that there is even more you can do to an array/ data structure in ruby, particularly now operating with a multi-dimensional grid
* Injecting Objects [KEY] - building on the key understanding of last week (using methods as object interfaces and chaining together to pass evaluated statements between obejcts) was able to work in an example today of pushing one such object into a grid and explored ways that you could directly call and manipulate that object within a data structure

****

What was difficult

* Dependency Injection - only touched on this in passing, need a better grasp of use cases, pros and cons etc
* Ensuring single responsibility/ avoiding spaghetti code - first implementation of battleships was very long winded, with EDUF still feel slightly vulnerable to very hacky solutions. Keen to learn more about how to improve design and build leaner programmes.

****

What's the plan tomorrow

* Finish the last couple of Battleships user stories and experiment with Game logic object and start thinking about UI

****

Code of the day...

Today's needs another co-creditor (Thanks Daryl) >> this is how we figured out to keep our ships where they should be - on the board and not on top of anything else.

	if ship.direction == "V"
    for x in 0..ship.size-1
      if row+x > 9 || col > 9
        grid[row+x-1][col] = nil
        fail 'Out of bounds'
      end
      if grid[row+x][col].nil? == false
        grid[row+x-1][col] = nil
        fail 'Already a ship'
      end
      grid[row+x][col] = ship
    end
  end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
