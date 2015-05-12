---
layout: post
title: "Day Eleven - May 12th"
date: 2015-05-12 23:22
author: Admin
categories:
- blog
- web-design
- Week 3
img: hello_world.gif
thumb: thumb01.jpg
---

###<b>Hello Internet</b>

So today I built a better relationship with the internet.
After the frustrations of yesterday's nearly efforts today brought more joy - albeit small steps.
Our battleships web-game is slowly taking shape and I have kept playing with the Twilio API through Heroku and learning about how unbelievably quickly you can build and serve something onto the internet for free.

****

What I Learnt

* REST and Routes - the key principles of being RESTful, particularly with the GETS and PUTS constructs are starting to make sense within the Sinatra environment and I am beginning to get data flowing correcly
* Object orientated design - to ensure encapsulation and integrity of key data structures need to build interface methods within your objects rather than just relying on attr_reader and passing around classes

****

What was difficult

* Still having some major testing fatigue with new frameworks >> will address back-end of this week
* Serving pages - there seems to be 50 different ways to skin the cat between shotgun, rackup, foreman start (Heroku) and Heruko itself. Got held up on state/ variable persistence issue caused by shotgun

****

What's the plan tomorrow

* Try and complete a first end-to-end version of Battleships-web. Also want to brush-up my CSS/ HTML skills to make it pretty.

****

Code of the day...

I found the sessions counter on my Twilio app fairly clever. It uses a cookie to track an SMS message conversation between 2 numbers (my Twilio number and phone number in this instance).

    enable :sessions

    get '/' do
      session["counter"] ||= 0
      sms_count = session["counter"]
      if sms_count == 0
        message = "Hello, thanks for the new message."
      else
        message = "Hello, thanks for the message number #{sms_count}"
      end
      twiml = Twilio::TwiML::Response.new do |r|
        r.Message message
      end
      session["counter"] += 1
      twiml.text
    end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
