---
layout: post
title:      "Final Project"
date:       2020-02-09 14:11:43 +0000
permalink:  final_project
---


For my final Flatiron School portfolio project, I built an app that allows users to study using multiple choice quiz questions. The project uses a Ruby On Rails backend and a React.js frontend.

A key feature of the project is user access, or more specifically user exclusion from areas they don't have access to. Each question in the database belongs to a topic. Users may be given access to the topic via topic_user objects on the backend. Currently, only users with administrator access (a boolean field in the User model - just me for now) can grant a user access to a topic. 

I actually deployed my app for use in a class I'm taking for work and I found that it was tedious to add each user to new topics every time a new topic was created. To alleviate the tedium, I added the ability to add topics to another model called Projects via project_topic objects. Now, rather than adding each user to each new topic, I gave all users access to one topic and I add each topic to the project as it's created.

One major hurdle I ran into while creating the project was maintaining the data in the Redux store. This difficulty came from my lack of understanding of how the Redux store and React Router interact. Any time the browser loads a new page, any data in the Redux store is lost. The way to prevent this loss of data is to ensure that any time a new route is accessed, navigation is via the React Router tools. I found that the easiest tools for me to use were the React Router components "Link" and "Redirect". When these tools are used to access new routes, the browser doesn't actually reload. React Router "tricks" the browser into rendering the new content without actually reloading the page. 

My classmates at work seem to really be enjoying using my app and I've added a few features at their request. I've found it to be a very educational and exciting experience - people are actually using my app and I'm getting real user feedback! Each new feature request presents me with an opportunity to solve a new "problem" and learn how to do something new.
