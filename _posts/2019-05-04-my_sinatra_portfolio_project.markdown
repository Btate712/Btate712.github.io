---
layout: post
title:      "My Sinatra Portfolio Project"
date:       2019-05-04 19:43:11 +0000
permalink:  my_sinatra_portfolio_project
---


For my Sinatra Portfolio Project, I built a web app that is designed for businesses to use.  Within the app, users can create tasks to be assigned to other users (or themselves).  In a business environment, a worker can't typically assign work to their boss, so the app needs to know who works for who and needs to ensure tasks can only be assigned to subordinates.  This supervisor/subordinate relationship creates a need to have a belongs to/has many relationship between users and other users.  Here's the basic layout of my models:

User:
* belongs to a supervisor
* has many subordinates
* has many owned tasks
* has many created tasks
* has many notes

Task:
* belongs to a creator
* belongs to an owner
* has many notes

Note:
* belongs to a task
* belongs to a user

For my controllers, I've used RESTful routes with a few modifications and/or additions.  For example, what would normally be my `/tasks/index` route is actually `tasks/users/:slug` because it doesn't make sense for a user to view all tasks, only the tasks that they've either created or that they own.  Another deviation from standard RESTful routes is that, in addition to a `/tasks/:id/edit` route (in which only the task creator can edit the task`, there's a `/tasks/complete/` route (in which only the task owner can mark the task as complete).

My views are currently not very visually appealing.  I need to add CSS. 

A walkthrough of my project can be found at [https://youtu.be/MSD3AUBIMQA](http://)
