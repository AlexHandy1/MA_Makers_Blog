---
layout: post
title: "Day Ten - May 11th"
date: 2015-05-11 23:00
author: Admin
categories:
- blog
- web-design
- Week 3
img: sheep.jpg
thumb: thumb01.jpg
---

###<b>Things Breaking</b>

Today has been one of those slightly frustrating days where you spend a lot of time and energy almost getting stuff to work but then not quite crossing the line.
We've moved on from basic command line interface ruby programmes to learning about pushing stuff online, specifically using Sinatra and some of the other ruby testing frameworks (Cucumber, Capybara).
Ambitiously, I have also tried to get Heroku working. That keeps breaking too.
Exciting to move onto the internet but day 1 of something v. new has brought back a lot of frustrations - e.g. took me about 2 hours to get a stupid sheep counting page to work.

****

What I Learnt

* Sinatra routes - you can control blocks of code to be passed between different HTTP method calls using /app and /view based files, essentially the VC and an MVC framework e.g. GET and POST and pass user inputs between these using params
* Sinatra sessions - are a way to control state and store user data in cookies during a stated session, will be interesting to apply to battleships game

****

What was difficult

* Cucumber and capybara tests - experiencing some test framework fatigue after rspec and even basic implementations in tutorial seemed a bit contrived
* Scaling up Sinatra and ERB logic - do not yet find the logic of passing data between routes intuitive and struggling to see how can transpose some of the more complex ruby logic to ERB

****

What's the plan tomorrow

* Get stuck into the Battleships web-challenge and start making some tangible progress there

****

Code of the day...

My barely functional sheep picture Sinatra app I suppose.

    <div>
      <%if @sheep_answer %>
          You think there are <%= @sheep_answer %>
      <%else%>
        <form action = "/hi" >
          My name is <%= @name %>
          Can you tell how many sheep there are?
          Is it <%= @sheep%>
        <input type = "text" name = "sheep">
        <input type = "submit">
      <%end%>
      </form>
     <img src='https://download.unsplash.com/photo-1423766111988-c47a5ff6ed06'>
    </div>

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
