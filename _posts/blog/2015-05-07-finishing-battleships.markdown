---
layout: post
title: "Day Eight - May 7th"
date: 2015-05-07 19:09
author: Admin
categories:
- blog
- web-design
- Week 2
img: battleships.jpg
thumb: thumb01.jpg
---

###<b>Finishing Battleships</b>

Mood in the cohort seems pretty low today, this week has been tough as the training wheels have been very abruptly removed and sometimes it isn't linear in terms of how you make progress.
I had a slightly mixed day and ended up doing more solo than pair programming but managed to string together a working battleships programme so can't complain.
Trying to take the opportunities to help others where can and am sure everyone will be feeling more energetic next week.

****

What I Learnt

* The importance of design [AGAIN] - trying to adopt 7 key rules/ questions I constantly review - is it DRY? is it SRP? What are the dependencies? Is it extendable (e.g. how react to change)? Is it abstractable? Is it testable? AND importantly, is it readable? (could I explain it to you if you didn't code)
* Yield - good way to remove dependencies by implicitly calling the block right outside a method e.g. Player.new{Board.new}
* Storing objects more intelligently - the key progress for linking up my battleships was understanding that I could create an opponent by creating an attribute @opponent that could pass the Player class and then call specific methods and interfaces on that

****

What was difficult

* Rspec module testing - still having some difficulty in getting this properly set-up when extracting my element converter module
* Stylistic conciseness and observing all the key design principles - need to keep working on this

****

What's the plan tomorrow

* Start looking into the weekend challenge and then try and extend Battleships where makes sense (e.g. separate Game Engine, UI)

****

Code of the day...

The Player attributes that made all the difference

    class Player
      include Converter
      attr_accessor :my_board, :my_shots_board, :attempts, :opponent

      	def initialize
          @my_board = yield
          @my_shots_board = yield
          @attempts = []
          @opponent = nil
        end

    end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
