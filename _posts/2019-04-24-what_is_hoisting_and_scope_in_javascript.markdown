---
layout: post
title:      "What is Hoisting and Scope in JavaScript?  "
date:       2019-04-24 17:16:11 -0400
permalink:  what_is_hoisting_and_scope_in_javascript
---


   First of all we run the JavaScript file from the top, so it is better to define a function before we invoked it. JavaScript engine will get the definition in advance, thus will not return undefined or causing any bugs. Moreover JavaScript hoisting is where variables and function declarations are moved to the top of their scope before we run the code. As in this example below JavaScript engine experience two phases, one is compilation phase and the other is execution phase. During the compilation phase JavaScript engine stores the declared function myWhat() in memory, and in execution phase myWhat() has already been created in memory start to execute line by line from the top. The term for this process is the hoisting because your declarations are being hoisted to the top of the current scope, and the best way to avoid any confusion for hoisting in JavaScript code is to declare your functions at the very top.
```
myWhat(); 
function myWhat () {
  return 'Hi, there';	
}
// =>  "Hi, there"
```

 Furthermore hoisting only applies to variable declarations, and not variable assignments. For example:
```
 // This is Declaration:
let cat;
 
// This is Assignment:
cat = 'kitty';
 
// This is Declaration and assignment on the same line:
let hello = 'world';
```
   As I mentioned before JavaScript during compilation phase hoisting will only get variable declarations, variable assignments will be undefined. yet it is better to use const and let in JavaScript hoisting, because var will cause hoisting issues and your programs are susceptible to oddly bugs. let and const make our block scope code hoisting easier, plus JavaScript engine will execute it easier at execution phase.
 
Scope in JavaScript is where our code like variables and methods place at, our code can place at in many different scopes like global scope and function scope. Global scope are where variables and functions declared in the global execution context, where all scripts and functions on a web page can access it.
```
function myNum () {
  return 2;
}
// => undefined

const myVar = myNum() * 2;
// => undefined
 
myVar;
// => 4
//we can use myNum() in myVar in the same scope or the global execution context, because myNum is declared in the global scope we can use it anywhere in our code.
```
  Yet function scope is variable or function that is declared inside a function or block, where we code in the function body. Also we can reference anything declared inside of its own scope, not outside the scope unlike global scope.
```
function myNum () {
  const myVar = 2;
 
  return myVar * 2;
}
// => undefined
 
myNum();
// => 4
//This example creates its own scope within its function body
```
 Moreover block scoping is a block statement that create its own scope within a set of curly brackets. While var are not block scoped, variables are set with const and let can be block scoped. Hence const and let are always better to use in JavaScript and it's a good way to avoid errors or bugs. Sometimes we also use context, context is always the value of the "this" keyword often refer to object that “owns” the currently executing code.

 In conclusion remember to use const and let to declare variables, const and let are more JavaScript developer coding friendly. In addition its important to understand scope and hoisting in JavaScript, scopes and hoisting will not only help you better understand the concept before advanced JavaScript. Good understand of scope will avoid coding mistakes. They all play a fundamental role in modern JavaScript to reach your goal in master this language.  

