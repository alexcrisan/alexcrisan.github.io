---
layout: post
title:      "Sinatra Portfolio Project"
date:       2018-04-07 01:22:13 +0000
permalink:  sinatra_portfolio_project
---


This project was very useful in bringing together all the things I learned about Sinatra, ActiveRecord, MVC, and CRUD. I created a Beat Store application which allows Users to create Beats. Each beat can have one or more associated Tags. Tags and Beats share a many-to-many relationship, while Beats belong_to Users and a User has_many beats. 

There are three controllers, including the application_controller, beats_controller, and users_controller. The beats- and users_controller inherit from the application_controller. The users_controller takes care of registering new users and logging existing users into the application. Once logged in, the beats_controller handles the creation, editing, and deletion of beats (in addition to the creation and association of tags). I didn't create a separate tag_controller because I wanted to consolidate the creation and editing of beats into single routes.

There are 4 models: user, beat, tag, and beat_tag. The beat model has two methods; one that slugifies a beat name, and one that allows a user to find a beat by slug. The views are all contained within beats and users folders. 

I used 'rack-flash' to alert users during critical points in the program for things such as problems with registration/login, invalid entries, etc. Users' passwords are encrypted and authenticated with the "bcrypt" gem. 

Overall I feel this project tested my skills and knowledge. I solidified my understanding of concepts such as the user authentication, rack-flash, and multi-level hash params. 
