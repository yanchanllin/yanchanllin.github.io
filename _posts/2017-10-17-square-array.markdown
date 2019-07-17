---
layout: post
title:      "Square-Array  "
date:       2017-10-17 16:24:58 -0400
permalink:  square-array
---

something I learned today, and I thought it will be helpful if I write this down. I am very bad at this,but I believe practice make it better each time.

def square_array(array)

   result =[]    #new array right here. Let's call it result
    array.each do |number|
    result << number*2    put in to new array
  end
     
  result  #returning the result array
end

map/collect

1. create an empty array
2.  iterates through the parameter
3.  does whatever code you tell it to do in the block
4.  then it adds that result to the array 
5.  when the iteration over, returns the array

[resource](http://speakingjs.com/es5/ch15.html#_terminology_parameter_versus_argument)
