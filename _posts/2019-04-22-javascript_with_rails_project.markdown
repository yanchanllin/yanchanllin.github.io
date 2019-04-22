---
layout: post
title:      "Javascript With Rails Project "
date:       2019-04-22 22:03:06 +0000
permalink:  javascript_with_rails_project
---

 ####            In this project I was required to build a jQuery front end to my previous project, the goal is to add dynamic features to my previous Rails application that are possible only through JavaScript and a JSON API. The purpose of jQuery is to make it much easier to use JavaScript on my website, this is a simpler task than building an entire project; but it challenged me as a first time learner for Javascript. I also learned that to build an application is the best way to learn a new language, it will push you to learn faster from fixing errors and facing new problems.  

  #### The requirements involved rendering a show and index page using jQuery and JSON, creating a resource must use your Rails application to render a form and rendering the response without a page refresh, a has-many relationship in the JSON, must translate JSON responses from your Rails app into JavaScript Model Objects using either ES6 class or constructor syntax. The Model Objects must have at least one method on the prototype, etc.

1. Must render at least one index page (index resource - 'list of things') via JavaScript and an Active Model Serialization JSON Backend.
I choose order index page to work on, I wanted this page to be able to render via JavaScript and an Active Model Serialization JSON Backend. In my orders.js file I made a getOrders function with ajax request and add it to function listenForClick() to make a click on the $('button#orders-data'); and it will show all the orders on index page.

               `function listenForClick() {
          $('button#orders-data').on('click', function (event) {
              event.preventDefault()
             getOrders()
  })`	
2.  Must render at least one show page (show resource - 'one specific thing') via JavaScript and an Active Model Serialization JSON Backend.
 In this requirement I want to display order show page, I wanted this page to be able to render via JavaScript and an Active Model Serialization JSON Backend too. In my orders.js file I code  const getOrderShow (id) with ajax request and add it to $(document).on('click', ".show_link", function (e). Clearout the page with $('div#notice.container').html('') and put in orderHTML with formatShow prototype.   
      `$(document).on('click', ".show_link", function (e) {
        e.preventDefault()
        $('div#notice.container').html('')
        let id = $(this).attr('data-id')
        getOrderShow(id)
    })`
3.        Your Rails application must dynamically render on the page at least one serialized 'has_many' relationship through JSON using JavaScript.This requirement got fulfilled with rendering many orders at index page with has many comments displayed under
4.      Must translate JSON responses from your Rails app into JavaScript Model Objects using either ES6 class or constructor syntax. The Model Objects must have at least one method on the prototype. Both of my index page and show page fulfill this requirement using JSON responses from your Rails app into JavaScript Model Objects and use prototype.
5.       Must use your Rails application to render a form for creating a resource that is submitted dynamically and displayed through JavaScript and JSON without a page refresh. 
I choose new order's page to render a rails new order form to post Json without a page refresh, inside listenForClick() function:
```                                                      
                   $("#new_order").on("submit", function (e) {
                        e.preventDefault()
                         const values = $(this).serialize()

                    $.post("/orders", values).done(function (data) {
                    $("form#new_order.new_order").html("")
						
                             const newOrder = new Order(data)
                            const htmlToAdd = newOrder.formatShow()
                          $("form#new_order.new_order").html(htmlToAdd)
			         	})
                     })```
  ####    Overall I am happy with how things turned out. Through this process I have learned so much and I can still add some more features I want to include later, since I know how to do it now. Can't wait what is there to learn and be a better full stack web developer. 	
							


