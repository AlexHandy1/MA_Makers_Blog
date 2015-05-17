---
layout: post
title: "Day Fourteen (plus w/e) - May 15th"
date: 2015-05-17 20:05
author: Admin
categories:
- blog
- web-design
- Week 3
img: Cam_MA.jpg
thumb: thumb01.jpg
---

###<b>An old school graduation</b>

So I spent this weekend back in Cambridge picking up my masters - slightly archaically, this is something you get as an extra freebie 4 years after you graduate.

Whilst its always entertaining to find an excuse to go back, it did remind me of one of the main reasons I wanted to do Makers which was to have a larger set of skills which I can functionally DO stuff with.

Also slightly panicked myself that I will be having a very different kind of graduation in just 9 weeks time...at least that will be more flannel tees and less white tie.

****

What I Learnt

* Importance of outside in design - now we are into the web and slowly increasingly complexity of our UIs it is important to build your system logic from the front back. Almost got into some difficulty with Rock Paper Scissors here had it been a more complex implementation
* Method refactoring - feel like I'm starting to get a better grasp of slimming down my method functionality and using combinations of methods more intelligently

****

What was difficult

* Cucumber and Capybara have proved very challenging for me this week - it feels like the first topic where my understanding still feels worringly high-level. Did improve my implementation but need to improve this moving into next week

****

What's the plan tomorrow

* Start databases - really looking forward to this as a) feels like another important piece of puzzle and b) I have spent a lot of time in my former career analysing data

****

Code of the day...

The primary game logic for my Rock, Paper, Scissors, Lizard, Spock game. Reduced from +20 lines of code to almost 10.

    def process_turn
      check_round_wins
      return "Game already won" if winner?
      if match?
        "Go again"
      else
        if rock_wins? || scissor_wins? || paper_wins? || lizard_wins? || spock_wins?
          player_1.add_round_win
          "You win"
        else
          player_2.add_round_win
          "Computer wins"
        end
      end
    end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
