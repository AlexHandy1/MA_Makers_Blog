---
layout: post
title: "Day Two - April 28th"
date: 2015-04-28 19:29
author: Admin
categories:
- blog
- web-design
- Week 1
img: post01.jpg
thumb: thumb01.jpg
---

<b>Lost in loops</b>

Today was the first full day at Makers and the difference in pace was clear.
We got our first set of challenges, first go at pair programming and started with the stand-ups and lecture structure.

****

What I Learnt

	Github pong - figuring out how you can push and pull to github whilst pair programming off your own laptops
	Rspec - covered all the basics in our FizzBuzz challenge
	Loops - kept experimenting with how multiple nested loops work and the output should expect (Wall St challenge)

****

What was difficult

	I lost some momentum in the afternoon after a good morning on the FizzBuzz challenge. Got very stuck in understanding nested loops for the Wall St challenge but thankfully cohort was able to help.
	Struggled with lack of structure in the afternoon - with longer challenges, I expect this may change but if not need to adapt my own structure

****

What's the plan tomorrow

	Start the Boris Bike challenge with a new pair

****

Code of the day...

Building a loop within a loop based on assessing the varying length of the hash we were iterating over was fairly mindbreaking so that wins today

	"(0..length_of_hash-1). each do |m|
		(m+1..length_of_hash-1).each do |n|
			if diff < stocks.values[n] - stocks.values[m]
		 		diff = stocks.values[n] - stocks.values[m]
		 		output = {stocks.keys[m] => stocks.values[m], stocks.keys[n] => stocks.values[n]}
		 	end
		end
   end"

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
