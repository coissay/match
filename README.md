The Match Game
================


Game players
----------------

The game can be played by 1 or 2 players.   
If only 1 player is playing the CPU will be playing the 2nd player.   
The player can only play during his turn.   
Each player play alternatively.   

Game world
-----------------

There is 20 match on the table.   
All match are arranged in a line.   
All match have the same shape.   

Play goal
-----------------

The goal is to ensure that the opponent takes the last match.   

Game rules
-----------------

You can take between 1 and 3 matches each turn.   
Taking the last match is a Game Over   
If the opponent take the last match you Win the game   
You must take at least 1 match per turn   
You can't pass his turn   
You have 5 min to play before he loose the game.   

Sample
-----------------

TotalMatchNbr = 20   
while (TotalMatchNbr)   
SendMsgTo("Your turn to play, pick between 1 and 3 Match", Human)   
NbrMatchPick = ReceiveMsgFrom(Human)      
TotalMatchNbr = TotalMatchNbr - NbrMatchPick   
if (TotalMatchNbr == 1)   
{   
PlayerWin   
Quit   
}   
y = randomNumber() % 3 + 1   
if (y > 3)   
y--   
TotalMatchNbr = TotalMatchNbr - y   
if (TotalMatchNbr == 1)   
{
ComputerWin   
Quit   
}   


