---
layout: post
title:  "What's an interesting problem you solved while learning CSS?"
date:   2017-09-26 00:39:40 +0000
---


I was building a CLI Tic Tac Toe game at object orientation Tic Tac Toe earlier and learned something new, I learned initialize method can be used after Class;        
   We know that any Ruby class can produce new instances of itself, via the <Class Name>.new method, whether or not that class has an #initialize method. However, if we want each instance of our class to be created with certain attributes, we must define an #initialize method. An #initialize method is a method that is called automatically whenever #new is used.
   When #new is called with an argument, it will pass that argument (or arguments) to the #initialize method and invoke that method. The code in #initialize will then run, using any arguments from #new.
     In this lab initialize method should set a @board variable equal to a new, empty array that represents the game board.
          class TicTacToe
          Def initialize (board= [" "," "," "," "," "," "," "," "," "])  
             @board = board
          End
 def board=(board)
        @board = board
  end
  def board
    @board
  End
Since we have initialize the board at the beginning, now we can use  @board in later helper methods. We don’t need to put an additional argument of board. 

