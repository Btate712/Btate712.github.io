---
layout: post
title:      "Somm - A Rails App For Wine Lovers"
date:       2019-05-31 23:27:07 +0000
permalink:  somm_-_a_rails_app_for_wine_lovers
---


For my rails project, I put together an app that allows users to rate wines and view their own ratings and the ratings other users have submitted.  Although it's outside the scope of the project, I plan to continue working on the project after it is submitted and to add an algorithm that determines which users have similar tastes and to make recommendations to users based on wines that other users with similar tastes have liked.

Getting the project up and running went pretty smoothly.  The hardest part was getting OmniAuth to work.  Building out the MVC components was fairly straightforward.  My models are Users, Reviews, Wines, and Varieties.  Heres how these models relate to one another:

User:
* has many reviews
* hasmany wines through reviews

Review:
* belongs to a user
* belongs to a wine

Wine:
* has many reviews
* has many users through reviews
* belongs to a variety

Varieties:
* has many wines 

I used ActiveRecord validations for things like making sure usernames are unique and making sure each rating (field of a review object) falls between 1 and 5.  Additionally, I added some CSS and a background image to make the app a little visually appealing.  My vision for an actually useful, production version of this app is that people would primarily access the app on their phones while they're at the store or at a restaurant selecting wines.  Because of this vision I've tried to visually style the app in a way that easily lends itself to building responsive layouts for the app.

I can actually see this app being useful to people, so I plan on spending time adding features and improving on it after I complete the Flatiron curriculum.  If nothing else, it'll be fun to build something that I can actually see people using.




