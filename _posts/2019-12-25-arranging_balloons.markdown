---
layout: post
title:      "Arranging Balloons "
date:       2019-12-25 19:00:03 +0000
permalink:  arranging_balloons
---

You are decorating your friend's birthday party. There are balloons K different colors, and you have access to infinite amount of balloons of any color. You want to arrange N balloons in a row, with the only condition that no two adjacent balloons can be the same color, becuase your friend will dislike it. 

How many ways are there to decorate the balloons?

```
function baloon(n,k){
    let result = k
    for(i = 0 ; i< n-1 ; i++){
    result*=k-1
    }
    return result
}
```


I used math in it (permutation)
result is # of ways you can re arrange it
