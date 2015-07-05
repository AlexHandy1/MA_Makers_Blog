---
layout: post
title: "Week 10 - July 5th"
date: 2015-07-05 23:45
author: Admin
categories:
- blog
- web-design
- Week 10
img: video.jpg
thumb: thumb01.jpg
---

###<b>Start of Final Projects</b>

Cutting it very fine again to make my weekly post as getting towards midnight

So Week 10 and final projects have come and gone meaning next week is the last week before full hiring/ job-searching begins.

Sadly, none of the ideas I pitched for final projects made it through to the final shortlist but nonetheless I am pretty pleased with where I have ended up.
My team is building a crowdsourced storytelling video app - similar to Vine but with longer videos and based more about topics/ events rather than individual personalities/ users. We are building a bunch of cool ways to capture and stitch together User Generated Content to better display the visual narrative around events.

Things seem to have gone relatively well so far, we are building up the product iteratively, there are tests and it is even starting to look vaguely presentable across both web and mobile.
Will be interesting to see how much further we can progress the functionality this week given all the extra activities around preparing for final project presentations (e.g. videos etc) and an early feature freeze on the Wednesday.

****

What I Learnt

* Extended Rails Functionality - I have enjoyed getting into more depth with Rails. Specifically, implementing observers to retrieve information from an API before saving an entry to Active Record and using scopes/ helper methods to extend the flexibility of models
* Technical trade-offs - we have leant heavily on the YouTube API to deliver our prototype, a direction I was keen to propose knowing how arduous a lot of the tech around video (e.g. storage, encoding, streaming) can be to set-up even with a combination of readily available third party tools. The trade-off, however, has been an ongoing and increasing limitation around the degree to which we can customise our solution.
* Value of revisiting and driving granularity in task development - we have had a number of helpful sessions as a team this week where we have gone back to our original User Stories/ vision and reworked the specific tasks/ tickets so that we are all clear on what is a must-have, hygiene factor and what features are nice to have

****

What was difficult

* Setting up Google Plus OAuth was inordinately painful - this was partly the product of following a particular online resource very closely. Key lesson here was that when you find yourself getting unexpected errors that you are chasing to lower and lower levels for something that should be relatively straightforward, you should strongly consider revisiting the overall approach rather than continuing to battle to the next granular workaround

****

What's the plan next week

* Finish the final project! - I would also love to try and incorporate some of the uplaoder work I have been building in Swift as have managed to get a working picture file uploader saving to our Rails app database via a post request from a dummy mobile app
* I also have a couple of side-projects I want to continue to progress

****

Code of the week...

I got the best conceptual breakthrough/ AHA moment with my Swift post request code

     func myImageUploadRequest() {
        let request = NSMutableURLRequest(URL: NSURL(string: "http://localhost:3000/videos")!)
            request.HTTPMethod = "POST"

        let param = ["tag" : "Tester"]

        let boundary = generateBoundaryString()

        request.setValue("multipart/form-data; boundary=\(boundary)", forHTTPHeaderField: "Content-Type")

        let imageData = UIImageJPEGRepresentation(MainImg.image, 1)

        if(imageData==nil) { return; }

        request.HTTPBody = createBodyWithParameters(param, filePathKey: "file", imageDataKey: imageData, boundary: boundary)

        let task = NSURLSession.sharedSession().dataTaskWithRequest(request) {
            data, response, error in

            if error != nil {
                println("error=\(error)")
                return
            }

            println("******* response = \(response)")

            let responseString = NSString(data: data, encoding: NSUTF8StringEncoding)
            println("****** response data = \(responseString!)")

            dispatch_async(dispatch_get_main_queue(),{
                self.MainImg.image = nil;
            });
        }
        task.resume()
     }
****
<!--more-->


[hampden]: https://github.com/jekyll/jekyll
