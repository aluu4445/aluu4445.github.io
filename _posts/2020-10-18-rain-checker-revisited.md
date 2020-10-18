---
layout: post
title:  "Rain Checker Revisited"
date:   2020-10-18 17:19:03 +1000
categories: learning cs
---

As a follow up to the free version of the course, I decided to purchase the [full version of the Flutter course offered by App Brewery](https://www.appbrewery.co/p/flutter-development-bootcamp-with-dart). At only $10 USD, I kind of regret not finishing the complete course earlier - the first half of the course is definitely introductory and the second half tackles much meatier topics. This does however let me look back on my Rain Checker app project and reflect on what I could've approached in a better way from both a design and execution perspective.

## 1. More modular code

I think it's pretty common knowledge that you don't want all your code to be in one file, but this is definitely where my Rain Checker app started. It wasn't clear to me what the best way to split up my code was, or how I was even meant to reference different Dart files from each other. The final result was broken up into a few high level files that revolved around different core functions like 'sending notifications' or 'checking the rain'. When I look back on it, it's more like I split up my code for the sake of not having one really long file, rather than any proper consideration for the benefits of modular code. 

For example, rather than having one file that covers everything related to getting a rain forecast, I'd separate out the user interface components and the components generating a rain forecast.

## 2. A better looking app

One thing that I feel a lot more confident in after completing the course is working with the visual Flutter widgets. The course does a good job of introducing the different widgets available to you and telling you to challenge yourself to create the sample widgets on your own, and there are a lot of chances to do it unprompted for more practice. I shrugged it off as an optional thing that I could add in later if needed but I think it's a pretty important feature in a mobile app and it's not particularly hard to get a basic but good looking app.

I'd spent some time looking for design inspiration and dedicate a few hours to get it looking nice.

## 3. Extra functionality

There a lot of widgets that I didn't even know existed back when I first made the Rain Checker app. Some of them are better ways to write features that I had like ListView and ThemeData, and there are also new things I could add like Animations and Loading indicators. 

I don't think this is too important but I may have designed it in a different way if I knew of all the different tools available to me.

## 4. Cleaner state management

One thing that I spent a lot of time trying to deal with without really knowing what I was dealing with was state management. To make it easier for me, I didn't modularise my code too much so I didn't have to pass data around too often. Now that I know how to do things like pass data through Routes or use the Provider package that's one whole less thing to worry about.

I'd like to spend some time in the future actually refactoring all my code to see how I could simplify it, but I think my time would be better spent starting a new project from scratch first.