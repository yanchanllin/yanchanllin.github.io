---
layout: post
title:      "Rails content management system"
date:       2018-07-17 19:12:59 -0400
permalink:  rails_content_management_system
---


     As I just completed my rails project, it seems I have been working on this one for a long time, like two months solving different errors and virtualbox system problems everyday; learning every bit of it. Project might be a slow process, but I think my learning is fast and memorable. The struggles and obstacles will help me in the future eventually, let me become a more skillful person and developer. 

     In this rails application project you can be a user signup and login with your facebook. Then you can start ordering food from this application, create healthy meals you want to add. moreover this app will show all the orders you picked and this company will deliver to you. I realized It is like ubereats company, but at the beginning I had many other ideas like one family restaurant delivery such a application for delivery guy to on track of the orders got to delivery. After working on this app for a while I see a wider customers can use this app, not just restrict on a restaurant. Almost everyone can use it when they eat or order everyday outside, this way this app will be more interesting and useful. Therefore many other people can see it, and can help many society. I also have the idea of if everyone use one delivery app, so it is even more helpful for restaurants to look at their record of source of income and orders customers made.

  Few things I used on this project includes: 
I used ruby on rails framework
three models that include has_many, a belong_to and has_many :through relationship for users,orders and meals 
Included validation for some attributes, such as presence for name
One ActiveRecord scope method I used is what is the most_recent meal user created, when I forget and want to track the meal
A standard user authentication which anyone can signup and login
Here I added a facebook auto login for better to server user
A nested resource with good RESTful URLs, such like in the routes meals/:meal_id/orders/new to: orders#new
Application can correctly display validation errors, ex: “name can’t left blank” to create a meal
   This rails content management system is more complex than sinatra application I made, therefore I used lot time on the rails files. As I  work on this for some time, I realized rails is a more complicated version of sinatra I’m happy I learned a new language. Looking forward to learn more and more everyday coming. 


