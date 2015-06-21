---
layout: post
title: "Week 8 - June 21st"
date: 2015-06-21 23:25
author: Admin
categories:
- blog
- web-design
- Week 8
img: ruby-on-rails-history.jpg
thumb: thumb01.jpg
---

###<b>Back to Ruby</b>

Just about keeping to the weekly blog posts albeit that its approaching midnight on the Sunday before Week 9...

Week 8 saw a return to Ruby and focused on learning the Ruby on Rails framework.

Its clear Rails is very powerful and there is a lot of 'magic' under the hood which allows you to build scalable (to a point) web apps very quickly.

Whilst I enjoyed getting back to Ruby, Rails is essentially an idiosyncratic language with its own set of syntax.  In hindsight, I'd have preferred to have spent more time exploring the full power of the framework rather than feeling like I have only touched the tip of the iceberg.

And with that marks the end of any formalised teaching/ learning as we move into the projects for the next 3 weeks.
I'm actually looking forward to this as solving real project based issues is the best way to learn as I am finding out as I keep trying to learn Swift for IoS.

That said I still have a degree of trepidation around what we'll actually be able to pull together and build based on what we know so far and time constraints.

The aim of a mobile focused IOS app written in Swift for a final project still remains just about on the table...

****

What I Learnt

* Rails, Active Record, not to fight the Rails framework and its reliance on correct pluralizations
* How you can expose multiple routes/ resources as APIs very easily through Rails

****

What was difficult

* Again, struggling slightly with how superficial some of my knowledge feels when introduced to a new framework. Hoping to bed in both Rails and Javascript full stack frameworks in coming week.

****

What's the plan next week

* Two projects including the Makerthon >> I have a couple of smaller ideas I'll put into the mix but will be interesting to see what we end up doing

****

Code of the week...

I'm still fascinated by API calls and asynchronous ajax actions so my Instagram dislike button wins this time.

    $('.dislikes-link').on('click', function(event) {
      event.preventDefault();

      var likescount = $('.likes-link').siblings('.likes-count')
      $.ajax({
          url: $('.dislikes-link').attr('href'),
          type: 'DELETE',
          success: function(response) {
              likescount.text(response.new_like_count);
          }
      });
    });

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
