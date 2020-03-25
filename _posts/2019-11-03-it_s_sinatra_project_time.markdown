---
layout: post
title:      "It’s Sinatra project time!"
date:       2019-11-03 17:07:30 -0500
permalink:  it_s_sinatra_project_time
---



This was my second project at Flatiron School and I’ve learnt so much from it. 

The project requirements were to:

* Build an MVC Sinatra application.
*  Use ActiveRecord with Sinatra.
*  Use multiple models.
*  Use at least one hasmany relationship on a User model and one belongsto relationship on another model.
*  Have user accounts - users must be able to sign up, sign in, and sign out.
*  Validate uniqueness of user login attribute (username or email).
*  Ability to create, read, update and destroy the resource that belongsto user.
*  Ensure that users can edit and delete only their own resources - not resources created by other users.
*  Validate user input so bad data cannot be persisted to the database.

I have always been a bit of a nerd when it comes to studying. I love learning new things and I have always loved taking neat and organised notes to help me remember the things I've learnt and to get everything to stick in my brain. I have always written out physical notes in an actual notebooks with loads of colour coordinated highlighting which is nice and pretty to look at, but ends up being a bit of a waste of space in my room and isn’t so good for the environment, so I thought, since I’m currently studying computer programming online, I should create a web app where I could store all my study notes online in one neat and organised space, and so I did :) 

The user and study notes table is as follows:


**user	                                                     study notes**
:username                                          	:title
:email	                                                  :topic
:password_digest                          	:notes
(password)	                                        :user_id
	
has_many :notes	                            belongs_to :user


This project was pretty eye opening as it showed me that there has really been so much that I’ve learnt so far whilst barely even scratching the surface. It was fun getting creative with the HTML and CSS and playing around with how the web app is displayed. Playing with TUX was also super handy, as well as learning how to use RESTful routes, which map between HTTP verbs (get, post, put, delete, patch) to controller CRUD actions (create, read, update, delete). Building a user signup and login system has been super interesting since this is a feature we use all the time in so many websites and it’s just been great to understand the way it actually works. 

This entire experience so far has been really challenging, rewarding and exciting. I will never get over how satisfying and inspiring it is to just think of an app idea and just go ahead and make it into reality just like that. 

