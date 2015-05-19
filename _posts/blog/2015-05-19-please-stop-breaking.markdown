---
layout: post
title: "Day Fifteen (+ Sixteen) - May 19th"
date: 2015-05-19 19:25
author: Admin
categories:
- blog
- web-design
- Week 4
img: tired-rex.jpg
thumb: thumb01.jpg
---

###<b>Things breaking again</b>

Its database week - this plus issues with the blog have led to a new record in things breaking and not quite getting to a nice, clean production point.
The blog issue (this is now seemingly spread across 2 repositories...) is a particular bind and may lead to a significant rework of approach...

****

What I Learnt

* Postgresql, SQL, Datamapper and the added ability to persist state from form submissions
* Capybara web testing syntax - this is slowly becoming more intuitive

****

What was difficult

* Getting Heroku working with a database - still failing 2hrs+ in

****

What's the plan tomorrow

* Refactor basic bookmark program and start having a database that can react to live input online + add some prettification

****

Code of the day...

Helpers are clever

    helpers do
      def current_user
       @current_user ||= User.get(session[:user_id]) if session[:user_id]
      end
    end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
