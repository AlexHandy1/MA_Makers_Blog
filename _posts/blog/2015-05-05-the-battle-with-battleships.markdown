---
layout: post
title: "Day Six - May 5th"
date: 2015-05-05 22:52
author: Admin
categories:
- blog
- web-design
- Week 2
img: battleships.jpg
thumb: thumb01.jpg
---

###<b>Start of Week 2...</b>

As if land and air transport based programming challenges were not enough, this week we are taking on the sea with Battleships.
The sea is hard.
Today has been the hardest day for me so far but I suspect I'll be able to copy and paste this a number of times again.

****

What I Learnt

* Composition - introduced to a new method to build objects, relevant for has-a structures rather than inherited is-a structures
* Single Responsibility Principle - need to ensure your objects are doing one thing >> need to fix my Airport weather to adhere to this
* EDUF - Enough Design Upfront - key principle and process to keep practicing

****

What was difficult

* Sticking to BDD/ TDD properly to drive 'emergent' design when you have a very loose understanding of how to solve the problem - always want to look ahead
* Picking the right grid structure - array of arrays, array of hashes, a hash or no grid at all were all plausible at some point today

****

What's the plan tomorrow

* Keep on with Battleships - try an athletic restart of today and push on to getting later user stories done

****

Code of the day...

The alphabet trick (credits to Rodney Cullen) to help structure the grid array without having to stick to my first, overly convoluted internal string naming convention probably saved me hours of pain tomorrow.

	alphabet = ('a'...'z').to_a
  row,col = ship_position.downcase.chars
  coords = alphabet.index(row), col.to_i-1

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
