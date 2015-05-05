---
layout: post
title: "Day Five - May 1st"
date: 2015-05-01 19:32
author: Admin
categories:
- blog
- web-design
- Week 1
img: airport.jpg
thumb: thumb01.jpg
---

###<b>So the end of the first week is over</b>

Today we had a bit more freedom to do our own thing which was useful - I tried to finish up Boris Bikes and managed to add some Vans and Garages which really helped in better understanding how to chain methods together and move objects around.
Also had a chance for a Q&A session with Evgency (Co-Founder and CEO of Makers Academy) which was interesting - for me personally it is encouraging that start-ups and entrepreneurship is promoted alongside the obvious push to get people into junior dev jobs.
Airport challenge awaits for the weekend but not before a couple of drinks.
Hopefully I have figured out how to write cleaner markdown so this will all look a bit tidier...will fix up first week of old posts when have a bit more time.

****

What I Learnt

* Doubles - how to ensure you have proper encapsulation in your tests by essentially passing placeholder objects to tests
* Manipulating objects - figured out how to effectively define class attributes and methods to ensure can move around and access.
* Establishing variables as class attributes and building methods to act as interfaces definitely came to life today.

****

What was difficult

* Doubles, mocks, stubs and some of the more advanced rspec testing methods still challenging to grasp - just need more working examples
* Level of testing to implement to ensure robust - this will likely become clear as scale of programmes increase

****

What's the plan tomorrow

* Airport challenge - start pushing through some of the weekend work

****

Code of the day...

This one line radically improved my understanding and ability of how to move around objects and their attributes using methods

	expect{ van.collect(docking_station.send_for_repair) }.not_to raise_error

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
