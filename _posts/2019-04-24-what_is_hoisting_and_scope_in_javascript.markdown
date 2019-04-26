---
layout: post
title:      "What is Hoisting and Scope in JavaScript?  "
date:       2019-04-24 17:16:11 -0400
permalink:  what_is_hoisting_and_scope_in_javascript
---


In this blog, I will introduce the concept of JavaScript hoisting, Hoisting was thought up as a general way of thinking about how execution contexts(specifically the creation and execution phases) work in JavaScript. Which deals with how function and variable declarations seem to get 'hoisted' to the top of the current scope. The variable and function declarations are put into memory during the compile phase, but stay where you typed them in your code.

When hoisting remember to follow these two simple rules: first declare all of your functions at the top of their scope. If the functions are declared in the global scope, simply put them at the top of the JavaScript file. If they're declared inside another function, put the declaration at the top of the function body. Second only use ES6 syntaxes const and let. Never use var, because var will cause some hoisting issues.

Given a good example for hoisting:

dogName("Lucky");

function dogName(name) {

  console.log("My dog's name is " + name);
}

/*
The result of the code above is: "My dog's name is Lucky"
*/

Although we call the function in our code first before the function, the code will still work. This is because of how context execution works in JavaScript.By the time the JavaScript engine reaches the execution phase, dogName("Lucky") has already been created in memory. The engine starts over at the top of the code and begins executing it line-by-line. Also JavaScript only hoists declarations not initializations. If a variable is declared and initialized after using it, the value will be undefined.

Bad example:

console.log(num); // Returns undefined 

var num;

num = 6;

Moreover context and scope play a significant role in JavaScript, context is related to objects and it refers to which a function belongs. When you use the JavaScript “this” keyword, it refers to the object which function belongs. Scope is variables defined inside a function and not visible from outside the function. If a variable is not "in the current scope," then we can not use it. Scopes can also be layered in a hierarchy, child scopes have access to parent scopes. Function scope can only be accessed from within the function,local variables are only recognized inside their functions. Block scope is called within the body of a function or a block statement that creates its own scope.

Scope example: 

// code here can NOT use catName

function myFunction() {

  var catName = "toby";

  // code here CAN use catName
}

However, a variable declared outside a function is called global scope, all scripts and functions on a web page can access it.

 It is important to understand scope, hoisting and context in JavaScript, it will assist you better understand all the concept before advanced JavaScript. They play a fundamental role in modern JavaScript, helps you reach your goal to master this language.  

