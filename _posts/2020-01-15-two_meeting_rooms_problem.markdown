---
layout: post
title:      "Two meeting rooms problem "
date:       2020-01-15 21:10:22 +0000
permalink:  two_meeting_rooms_problem
---


n meetings for today. There's only two meeting rooms avaliable today. start [i], end [i]

```
function meeting(start, end){
    if(start.length !== end.length) return 0
   let array= [];
    
//     making 2d  array
   for (let i =0 ; i< start.length; i++){
    array.push([start[i],end[i]])
   }
// sorting according to start time
   let sorted=array.sort(function(el1,el2){
        return el1[0] - el2[0]
    })
    let maxCount = 1   // if maxCount > 2 we need more rooms
    
    
    for(let i = 0; i< sorted.length; i++){
        let count = 1   // check room needed for time start : sorted[i][0] - end :sorted[i][1]
        for(let j = i+1; j<sorted.length; j++){
            if (count > 2) return 0
            if (sorted[i][1] < sorted[j][0]) break;
            if(sorted[i][1] >= sorted[j][0]){
                count ++
            }
            maxCount = Math.max(maxCount, count)
            
        }
    }
    if (maxCount <= 2 ){ 
    return 1
    }else{
        return 0
        }
}

```

