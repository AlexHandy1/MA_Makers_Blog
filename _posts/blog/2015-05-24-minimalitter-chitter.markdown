---
layout: post
title: "Day Seventeen through to Day Nineteen - May 24th"
date: 2015-05-24 17:15
author: Admin
categories:
- blog
- web-design
- Week 4
img: Minimalitter-chitter.png
thumb: thumb01.jpg
---

###<b>Minimalitter Chitter</b>

Given the absence of blog entries it is perhaps little surprise that Week 4 was quite a tough week and additionally, that with various breakages, bugs etc (still including this blog) I had briefly lost the enthusiasm to keep hacking away on here on top of everything else.
That said, I have been revitalised by channelling my angst and inner struggle into our weekend challenge of creating a Twitter Clone.

As you can see below in its slightly buggy, clunky but darkly minimalistic glory.

[Minimalitter Chitter](https://minimalitter-chitter-ah.herokuapp.com/)

****

What I Learnt

* How an end-to-end application comes together in the model, view, controller structure - this was quite a cool step particularly with the added persistence layer of databases
* A lot more capybara web testing syntax and examples

****

What was difficult

* More advanced CSS and front-end techniques - I am super keen to make things pretty
* More complex database relations and querying - find Datamapper a little constricting at times

****

What's the plan tomorrow

* Its a bank holiday, but I will be beginning the task of learning a new language - Javascript.

****

Code of the day...

I love a good hidden form for my peeps and replies.

    <div class="col-md-10 col-md-offset-1">
     <% if @peeps %>
      <% @peeps.reverse.each do |peep| %>
      <div class='row'>
        <div class="col-md-11" id='dotted'>
            <div class ="col-md-4" id='test'> <%=peep.message%> </div>
            <div class ="col-md-2"><%=peep.user.name%> </div>
            <div class ="col-md-2">@<%=peep.user.username%> </div>
            <div class ="col-md-2"><%=peep.created_at.strftime('%e %b %Y %H:%M:%S')%> </div>
             <form action='peeps/makereply' method='post'>
                <input type='hidden' name='original_id' value='<%=peep.id%>'>
                <button type='submit' class='btn btn-default' id='button-hack' value='Reply?'>Reply?</button>
              </form>
          </div>
        </div>
          <br>
      <%end%>
     <%end%>
    </div>

****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
