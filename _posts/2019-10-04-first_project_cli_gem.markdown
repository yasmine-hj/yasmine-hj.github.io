---
layout: post
title:      "First Project – CLI Gem"
date:       2019-10-04 15:38:44 +0000
permalink:  first_project_cli_gem
---


It was such a satisfying feeling seeing everything I have learnt so far come together and create my very first gem! 

I created an application which extracts a list of the classes available at a gym I was considering joining through scraping the data on their website. It then allows the user to select a gym class they are interested in to find out more information about it.

It was made through creating three key classes: a Scraper class, CLI class and the Gym_Classes class. 

I started of by typing “bundle gem (gem name)” which generated the gem structure for me. The Scraper class was the first class I started creating, which allows you to scrape information off of the desired website using open-uri and nokogiri. I used several different` .gsubs ` to clean the text as it was initially returning several different characters in the middle of the text which I didn’t want to be visible to the user whilst using the application to keep the information clear and concise, such as "â\u0084¢", “\n” and “\r”. 

I created two different class methods in my Scraper class, one which was called “scrape_gym” which scraped the page which contained a list of the different gym classes, and another which was called  ”scrape_individual_gym_class” which would then scrape the url to the specific chosen gym class.

I then created the Gym_Classes class containing an `attr_accessor`, which sets different attributes and allows this class to read and write required information such as :title, :url and :details. I then initialized using the title and the URL. 

The CLI class is what was used to interact with the actual user of the application. This was the most fun to play around with since I got to perfect the way I wanted the software to look like and interact with the user. I used` If, elsif and else` statements, as well as `gets.chomp ` and `puts` to interact with the user and allow the user to respond. It was really interesting to see how you can use this class to add different responses to the users input and customize the use of the application.

The gem can be installed by typing:

`gem install Gym_Classes`

and can be executed by typing:

`ruby bin/GymClasses`

My first interactive database and I can’t wait to create more!

