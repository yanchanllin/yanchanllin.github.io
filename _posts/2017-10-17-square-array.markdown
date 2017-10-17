---
layout: post
title:      "Square-Array  "
date:       2017-10-17 20:24:57 +0000
permalink:  square-array
---

something I learned today, and I thought it will be helpful if I write this down. I am very bad at this,but I believe practice make it better each time.

def square_array(array)

    result =[]    #new array right here. Let's call it result
    array.each do |number|
    result << number**2    #put in to new array
  end
     
  result  #returning the result array
end


map/collect
# create an empty array
# iterates through the parameter
# does whatever code you tell it to do in the block
# then it adds that result to the array 
# when the iteration over, returns the array

http://speakingjs.com/es5/ch15.html#_terminology_parameter_versus_argument
