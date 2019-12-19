---
layout: post
title:      "Algorithms/Procedure"
date:       2019-12-19 03:18:52 +0000
permalink:  algorithms_procedure
---


   Our programming languages need algorithms, we can apply algorithm's technique to solve alot problems in programming.
 
first make it work,
make it readable
and make it fast.

Something I learned today:
Evaluate the value of an arithmetic expression in Reverse Polish Notation.

Valid operators are +, -, *, /. Each operand may be an integer or another expression.

```
var evalRPN = function(tokens) {
    let signs={
        "+":1,
        "-":1,
        "*":1,
        "/":1
    }
    let temp=[]
    let result
    for(let i=0; i<tokens.length; i++){
        if(!signs[tokens[i]]) {
            temp.push(tokens[i])
        }else{
            let last=parseInt(temp.pop())
            let secondLast=parseInt(temp.pop())
            
            switch(tokens[i]) {
              case "+":
                result = secondLast + last 
                break;
              case "-":
                result = secondLast - last 
                break;
              case "*":
                result = secondLast * last 
                break;
              case "/":
                result = secondLast / last
                break;
              default:
                break;
            }
            temp.push(result)
        }
    }
    return Math.floor(temp[0])
};
```
