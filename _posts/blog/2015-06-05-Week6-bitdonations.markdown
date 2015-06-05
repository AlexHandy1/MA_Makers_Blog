---
layout: post
title: "Week 6 - June 5th"
date: 2015-06-05 18:00
author: Admin
categories:
- blog
- web-design
- Week 6
img: bitcoin-piggy-bank-2.jpg
thumb: thumb01.jpg
---

###<b>BitDonations</b>

Its the end of lab-week, a sort of reading week that marks the halfway point of the Makers course. There is no structured learning objectives and you are left to your own devices.
I decided to have a go at building my own mini-project that combined two areas of interest - emerging market entrepreneurship (particularly in East Africa) and cryptocurrencies based around Blockchain technologies.
The result was a prototype for a very basic platform that could facilitate direct P2P donations between donors and young entrepreneurs - think Kiva for micro-donations but with Bitcoin.
I have written more about tech and use cases on my Github so if interested check that out below.
![Github README](https://github.com/AlexHandy1/BitDonations-labweek)

****

What I Learnt

* Seemingly complex and intimidating technologies (e.g. Bitcoin, Blockchain) can be broken down into practical steps where you can make tangible progress - helpfully in the case of Bitcoins it has been developed enough that abstraction has been extended to the point of Ruby gems and easy to call APIs
* Having a better understanding of the tools and frameworks for more advanced front-end layouts is key - very hard to add professional styling right at the end without the right structure, tags etc

****

What was difficult

* Developing a really slick, professional looking front-end still feels a stretch and is an area I know I need to improve, hopefully the more mistakes I make here the better my end-products will end up

****

What's the plan tomorrow

* Want to ramp-up my understanding of Javascript and its accompanying frameworks e.g. Angular, Node etc so will get started on that over the weekend

****

Code of the day...

The Bitcoin transaction flow

  ```
    #ACCESS PREVIOUSLY GENERATED ENTREPRENEUR BLOCKCHAIN WALLET FROM DATABASE
    @entrepreneur = Entrepreneur.get(@ent_id)


    #ACCESS DONOR WALLET FROM API AND SEND STATED BITCOIN TO ENTREPRENEUR
    @donor_wallet = Blockchain::Wallet.new(@donor_wallet_id, @donor_wallet_password)
    @payment = @donor_wallet.send(@entrepreneur.wallet_address, @satoshis, from_address: @donor_address)

    #STORE TRANSACTION IN DATABASE
    @transaction = Transaction.create(amount: @satoshis, entrepreneur_id: @ent_id, donor_id: current_donor.id)

  ```
****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
