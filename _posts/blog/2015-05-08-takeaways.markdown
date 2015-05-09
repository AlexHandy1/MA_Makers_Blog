---
layout: post
title: "Day Nine - May 8th"
date: 2015-05-08 23:57
author: Admin
categories:
- blog
- web-design
- Week 2
img: takeaway.jpg
thumb: thumb01.jpg
---

###<b>Takeways, Injecting and the Weekend...</b>

So its actually Saturday night - with all the challenges etc, yesterday got away from me a bit so am consolidating today.
Excitingly, we are starting to get into the realms of the internet and connecting to actual things rather than working away to get our internal tests to pass.
Whilst far from groundbreaking, it is surprising just quite how rewarding it is when you manage to write a small script which uses an API to send text messages to yourself (and others) over the internet straight from your command line.
Big workload for the weekend challenges still lies ahead though - hence why I am hacking away at this now...

****

What I Learnt

* APIs are not intimidating, add a huge amount of functionality to what you are doing and are fun to use
* Starting with designing your UI upfront (even if just a set of IRB commands) and developing your object and domain structure accordingly is very helpful in mapping out an object orientated programme

****

What was difficult

* Getting to grips with the more complex applications of the inject method and combining with yield and out of method block calls >> still feels far too trial and error
* Building a scalable data structure for the Takeaway challenge - have a working prototype but interesting to explore how you would structure if this was a programme processes higher volumes and concurrent orders

****

What's the plan tomorrow

* I want to have a go at building a new, more sophisticated version of the Takeaway challenge using some of the more advanced techniques that were shared in Ben's version of battleships and also look ahead to next weeks objectives

****

Code of the day...

Definitely the Twilio API call.

    @client.account.messages.create(:body => "Thank you! Your order was placed and will be delivered before #{(Time.now+hour_in_secs).asctime}")

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
