# The_100_game
Machine learning used to develop an unbeatable player of "The 100 game" programmed in Python

The 100 game is a version of NIM games.
See definition under https://en.wikipedia.org/wiki/Nim#The_100_game
The program has a dumb terminal interface that lets you do the following
  (R)ule: displays game rule
  (P)lay: you can play against the computer
  (L)earn more: runs ML (reinforcement learning) to develop game playing skills
  (S)how my knowledge: shows the knowledge base of the computer
  (E)xit: exits the program

When in learning mode the program generates two instances of a player and they start playing games against each other. 
In the beginning both players select their moves randomly but after each game the 100 different places of the board
are marked as follows:
- all the places have an initial value of 0
- the value of the places that were used by the winner are increased by 1
- the value of the places that were used by the looser are decreased by 1
The values are used to improve the selection of the next move by each player while learning. The place having the 
higest value is selected from the available possible places. If more than one place have the same highest value a
random choice is made among them.
By applying this method the program slowly finds the winning positions after about 150 - 200 games. These winning
positions form the winning strategy.

Interesting observations:
- sometimes "wrong" places are identified initially as winning positions but the program forgets these positions 
(decreases their value) after more learning iterations
- the program converges to the winning positions
- convergence is achieved (meaning the winning positions are found) even if we change the length of the board from 100 
to any other number and also if we change the maximum step size from 10 to anything.

Have fun!
Gabor
