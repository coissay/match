The Matches Game
================


Game players
----------------

The game can be played by 1 or 2 players.   
If only 1 player is playing the CPU will be playing the 2nd player.   
The player can only play during his turn.   
Each player play alternatively.   

Game world
-----------------

There is 20 matches on the table.   
All matches are arranged in a line.   
All matches have the same shape.   

Play goal
-----------------

The goal is to ensure that the opponent takes the last matches.   

Game rules
-----------------

You can take between 1 and 3 matches each turn.   
Taking the last matches is a Game Over   
If the opponent take the last matches you Win the game   
You must take at least 1 matches per turn   
You can't pass his turn   
You have 5 min to play before he loose the game.   

Sample
-----------------

TotalMatchesNbr = 20   
while (TotalMatchesNbr)   
SendMsgTo("Your turn to play, pick between 1 and 3 Matches", Human)   
NbrMatchesPick = ReceiveMsgFrom(Human)      
TotalMatchNbr = TotalMatchNbr - NbrMatchesPick   
if (TotalMatchesNbr == 1)   
{   
PlayerWin   
Quit   
}   
y = randomNumber() % 3 + 1   
if (y > 3)   
y--   
TotalMatchesNbr = TotalMatchesNbr - y   
if (TotalMatchesNbr == 1)   
{
ComputerWin   
Quit   
}   


Sample

While(true)
X = randomNumber()
SendMsgTo("Guess?", Human)
Y = ReceiveMsgFrom(Human)
if(X == Y)
Score++;
if (y ==Quit)
Quit