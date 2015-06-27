---
layout: post
title: "Week 9 - June 27th"
date: 2015-06-27 12:30
author: Admin
categories:
- blog
- web-design
- Week 9
img: teamwork.jpg
thumb: thumb01.jpg
---

###<b>Makerthon and Makermix</b>

Sat waiting for a haircut opposite the Makers office so felt as good a time as any to try and recap on the week.

Week 9 has all been about learning how to build stuff in teams.
Unsurprisingly, that is a lot harder than it sounds and is worth doing before getting started with the final projects next week.

I think I was actually fairly lucky in that both my team experiences were pretty positive and for both the Makerthon and Makermix we had a working, albeit simple product at the end.

For Makerthon (a 2 day internal hackathon) my team built a clone of Followerwonk but for Instagram which allows you to search and sort Instagram users by topic.  This involved writing a fairly ambitious scraper to gather data through the Instagram API so went on a fun rabbit-hole figuring that one out - think Rodney is probably still abusing my Auth access token right now.

For Makermix (3 days to build a maker pairing app in an unrealistically massive team) I unfortunately had to miss most of the last day but I was pleased that our team managed to wire together a full MEAN JS app which is not bad going when its new to everyone and you are trying to coordinate between a team of almost 10.

As for final projects, still not decided what we'll all be doing yet. I still want to keep pushing on with learning Swift so I will figure out a way to incorporate that.

Only 3 weeks to go...

****

What I Learnt

* Git workflow - had to work through a whole host of merge conflicts but feel like I now have a good grasp of how to set-up and work within a master>develop>feature workflow structure
* Ruby native API calls - rather than using AJAX javascript based API calls as had done previously, for the Instagram clone was forced to use HTTParty and structure an API call that could ultimately scale and automate through a custom rake task
* Connecting MongoDB/ Mongoose all the way through to an angular front end - basically involved structuring your app as its own RESTful API in the Node Express layer and then creating angular factories to request the relevant endpoints

****

What was difficult

* Dividing up work in an effective and holistic way was challenging but I felt like this did improve significantly as week progressed

****

What's the plan next week

* Final projects start...specifics TBD

****

Code of the week...

The relatively hacky instragam API call

  namespace :instagram_api do
    desc "TODO"
    task get_users: :environment do
       @first_call = HTTParty.get('https://api.instagram.com/v1/users/25025320/followed-by?access_token=$ACCESS_TOKEN')
      @data_first = @first_call.parsed_response["data"]

      @data_first.each do |data|

        User.create(instagram_id: data["id"])
        @user = User.find_by(instagram_id: data["id"])
        @second_call = HTTParty.get('https://api.instagram.com/v1/users/' + @user.instagram_id.to_s + '/?access_token=$ACCESS_TOKEN')
        @data_second = @second_call.parsed_response["data"]

          if @data_second != nil

            if @data_second["username"] != nil && @data_second["full_name"] != nil && @data_second["bio"] != nil && @data_second["counts"]["follows"] != nil && @data_second["counts"]["followed_by"] != nil

               @user.update(username: @data_second["username"],full_name: @data_second["full_name"], bio: @data_second["bio"],follows: @data_second["counts"]["follows"], followed_by: @data_second["counts"]["followed_by"])
            end

            if @data_second["profile_picture"] != nil
              @user.update(profile_picture: @data_second["profile_picture"])
            end

          end
        end
    end

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
