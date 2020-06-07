---
layout: post
title:      "Count Islands"
date:       2020-06-07 16:23:14 +0000
permalink:  count_islands
---


Given a 2d grid map of '1's (land) and '0's (water), count the number of islands. An island is surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You may assume all four edges of the grid are all surrounded by water.

```
Example 1:

Input:
11110
11010
11000
00000

Output: 1
```

```
Example 2:

Input:
11000
11000
00100
00011

Output: 3
```
***JavaScript Solution:***
```
var numIslands = function(grid) {
    
  let countIslands = 0 ;
     for(let rowIndex in grid){
         for(let colIndex in grid[rowIndex]){
             if(grid[rowIndex][colIndex] === '1'){
             countIslands++;
         teraform(parseInt(rowIndex), parseInt(colIndex), grid);
          }
        }
     }
    return countIslands;
    };
    
    //helper method
    //convert stuff around us to water
    const teraform = (rowIndex, colIndex, grid) => {
        if(grid[rowIndex] === undefined || grid[rowIndex][colIndex] === undefined ||grid[rowIndex][colIndex] === '0') return;
        
           grid[rowIndex][colIndex] = '0';
         teraform(rowIndex+1, colIndex, grid);
         teraform(rowIndex-1, colIndex, grid);
         teraform(rowIndex, colIndex+1, grid);
         teraform(rowIndex, colIndex-1, grid);
    }
```
    
    

***Ruby psudocode:***

```
function getNumberOfIslands(binaryMatrix):
    islands = 0
    rows = binaryMatrix.length # number of rows
    cols = binaryMatrix[0].length # number of columns

    for i from 0 to rows-1:
        for j from 0 to cols-1:
            if (binaryMatrix[i][j] == 1):
                markIsland(binaryMatrix, rows, cols, i, j)
                islands++
                
    return islands


function markIsland(binaryMatrix, rows, cols, i, j):
    q = new Queue()
    q.push([i,j])
    while (!q.isEmpty()):
        item = q.pop()
        x = item[0]
        y = item[1]
        if (binaryMatrix[x][y] == 1):
            binaryMatrix[x][y] = -1
            pushIfValid(q, rows, cols, x-1, y)
            pushIfValid(q, rows, cols, x, y-1)
            pushIfValid(q, rows, cols, x+1, y)
            pushIfValid(q, rows, cols, x, y+1)


function pushIfValid(q, rows, cols, x, y):
    if (x >= 0 AND x < rows AND y >= 0 AND y < cols):
        q.push([x,y])
```
        
 input:  binaryMatrix = [ [0,    1,    0,    1,    0],
                         [0,    0,    1,    1,    1],
                         [1,    0,    0,    1,    0],
                         [0,    1,    1,    0,    0],
                         [1,    0,    1,    0,    1] ]

**output: 6 # since this is the number of islands in binaryMatrix.
       
