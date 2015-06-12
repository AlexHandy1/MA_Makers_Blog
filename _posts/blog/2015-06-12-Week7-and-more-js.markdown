---
layout: post
title: "Week 7 - June 12th"
date: 2015-06-12 18:00
author: Admin
categories:
- blog
- web-design
- Week 7
img: funnyjavascript.gif
thumb: thumb01.jpg
---

###<b>And some more Javascript...</b>

This week has been all about getting to grips with more Javascript, good to get back into some more structured learning following lab week and managed to cover the full JS stack from Angular in the front-end through to Node and Mongo DB for the back-end.

I was able to vaguely pull this together in my own small Subreddit search app but am hoping weekend challenge will be another good opportunity to push forward here.

Coming to the end of Week 7 is pretty daunting. We essentially have 1 week left of a formal 'curriculum' with Rails next week and then we are straight into 3 weeks of projects.

Have also started playing with Swift in XCode which has been a fun break as it is a lot more visual form of programming compared to battling away at the command line.


****

What I Learnt

* The key components for building a full stack web app in Javascript >> MongoDB, Node (Express) and Angular JS
* More experience working with APIs - feel more confident having now got ~4-5 APIs functioning with differing tasks

****

What was difficult

* The breadth of information to pick up on Javascript significantly outweights the time we have left within the course to learn. The depth of my knowledge in Javascript and accompanying frameworks still feels light.

****

What's the plan next week

* Do more pairing - as a cohort we haven't been great this week
* Get back into Ruby and Ruby-on-rails

****

Code of the day...

The post route for collecting my Subreddit search data and storing in my API

    app.post('/searchtermsdb', function(req, res) {
      var searchterm = req.query.searchterm;
      var collection = db.get('reddit')

      collection.insert(
        {"searchterm" : searchterm},
        function(err, doc) {
          if(err) {
            console.log('error');
            res.send("There was a problem adding the information to the database.");
          } else {
            res.redirect('/');
          }
        });
     })

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
