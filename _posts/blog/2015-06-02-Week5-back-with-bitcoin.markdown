---
layout: post
title: "Week 5 (and start of 6) - June 2nd"
date: 2015-05-24 17:15
author: Admin
categories:
- blog
- web-design
- Week 5
img: bitcoin-piggy-bank-2.jpg
thumb: thumb01.jpg
---

###<b>Back with Bitcoin</b>

So I have fallen off the blogging bandwagon a bit in recent weeks and given ongoing intensity am going to try and stick to a weekly (maybe bi-weekly) blog update to the end of the course rather than stick to my early pace of daily updates.

The combination of picking up a new language (Javascript) and starting to take on larger, wider-ranging topics (my basic Bitcoin donation web app) has reduced the time to dedicate to this blog.

Also the more I learn about web development the more I realise I want to entirely re-do my own portfolio/ blog site so that has somewhat lowered my enthusiasm for militantly maintaining this particular spot.

That said, I shall continue albeit at a slightly reduced rate but hopefully, with more complete, weekly reflections!

****

What I Learnt

* Week 5 was all about learning Javascript - I really enjoyed focusing more on the front-end and experimenting with jQuery, particularly as I started to exploring calling APIs using AJAX
* This week I have started ramping up my own ambition to learn more about the technical implementation of cryptocurrencies (particularly Bitcoin as the largest in operation) and the underlying distributed blockhain technology

****

What was difficult

* Testing the front-end has been far more challenging than early adventures with Rspec and Capybara for Ruby. Have only scratched the surface with Jasmine for Javascript
* Exploring a emerging technology like Bitcoin with no structured guidance has been intimidating but I feel much more equipped to do so than 6 weeks previously

****

What's the plan tomorrow

* Keep pushing on with my Bitcoin application - have got a basic interaction with the API working and tested (albeit through a live transfer from someone else's Bitcoin wallet...thanks Rodney)

****

Code of the day...

Building the Ruby server-side interaction with the Blockchain.info API to serve up a randomly generated input address that could receive Bitcoins to my account

    @resp = Blockchain::receive('12X6MREyoTDg6gGYf9BLZ26PaDCKA6xfmD', 'https://peaceful-sea-2336.herokuapp.com/')
    @input_address = @resp.input_address

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
