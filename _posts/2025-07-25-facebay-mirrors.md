---
layout: post
title: I Made Something Silly
date: 2025-07-25
description: Facebook marketplace oddities.
---

Hello. The image below should change every time you refresh this page.

<div style="display: flex; justify-content: center;">
    {% include figure.liquid
        loading="eager"
        path="http://79.72.79.205"
        class="img-fluid rounded z-depth-1"
    %}
</div>

A hobby of mine is to search for mirrors on Facebook Marketplace[^1]. It entertains me that people often try to avoid being visible in the photo, but, in the relatively lukewarm heat of the moment, do not have the idea to stand to the side and take a picture of the mirror at an angle. Instead, a substantial minority will rather hilariously reach an arm into the shot to snap the picture. There may be other oddities I have saved to the collection because I have found them entertaining in other ways.

If, by some freak chance, you are in one of these images and you don't like it, please reach out to me at mehmenmike@gmail.com, and I will happily remove it. Please, however take this as a lesson in that anything you put on the internet publicly is indeed public. It is accessible by anyone, and strange people with too much time on their hands may do as they please with the data you upload.

## The Technical Stuff

This website is a static site, compiled from markdown I write offline. It isn't possible for static sites to dynamically change the content they serve, without some silly JavaScript voodoo. You can somewhat circumvent this limitation by creating and hosting a small application that runs a web server. Set it up so whenever it is poked over the internet, it replies with an image. Just like how if you poke google.com, you're given a webpage that has the Google logo, a search bar and 40lbs of tracking scripts. Except much simpler - just send an image back.

Behind the scenes, all my app does is randomly select an image from a directory. It then sends the image as the response to that poke (i.e. HTTP request).

## The Practical Stuff

This will not work one day. I can say with absolute certainty that there will be a day when this will stop working, and the image on this page will not load. Perhaps Oracle Cloud will discontinue its free tier. Or maybe I will accidentally break it myself. Perhaps someone will hack the machine serving the images. I will not be actively maintaining this toy, so if you happen to be here before it breaks, enjoy![^2]

---

[^1]: Other peer-to-peer marketplaces are available.
[^2]: Creating stuff on the internet is always temporary. And before you tell me I'm wrong, because that picture of your wrecked car from 2009 is still on Facebook, think about the coordination it took between thousands of people to keep that image accessible. Software engineers performing migrations safely to ensure data is brought onto newer versions of databases before support is dropped. Compliance teams in charge of making sure the organisation obeys new and evolving law, like GDPR and CCPA. Frontend engineers working so the Facebook website itself (that is, the tip of the iceberg) still functions - even on multiple different browsers, on different platforms. And of course, the mobile app. It's a Ship of Theseus, completely changed and yet still bears same name. Everything, EVERYTHING needs constant maintenance, real or digital.
