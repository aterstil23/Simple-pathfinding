# Simple-pathfinding
Using the layout of pacman with walls as printed "X" and spaces to move in printed with " "(space) from https://github.com/patriciateroltolsa/Pacman, i used the algorithm for pathfinding to find the shortest distance to go from position (y1, x1) to (y2, x1) where y1 is the vertical number of lines from the top and x is how many characters from right to left from wikipedia from the section "sample algorithm" (https://en.wikipedia.org/wiki/Pathfinding).
The function removecells1 used in the function pathfinding1 removes all paths that are walls (so are not valid to move in) and removecells2 used also in pathfinding1 checks if the same position is repeated in later paths(so not to return to the same position as previously).
I have one enemy which is monster1 that is represented by the symbol "#". And the player controlled by arrows key is represented by "O".
Unfortunetaly i didn't use any librairies to represent the graphics in a better way (so the labyrinth is printed in a loop after each iteration the screen is cleared and the cursor is moved to the top right).
I made the enemy monster go towards the player for 15 moves than retreat for 6 moves. (You can change that by timing the bool flags flee and chase to change value from true to false or false to true every time with a modulus operation that checks the state (number of total moves of enemy) is a multiple of the number of moves you want to chase it n+ the number of moves you it to flee m (state % (n+m)==0) and to switch from chase mode to flee mode you can verify if ((state-n)%(n+m)==0).
Even though there is a pop up of debug error, i just ignored it and it still worked.
![image](https://user-images.githubusercontent.com/121896803/215297077-85da37b4-d12b-4431-a288-9f1bc098858d.png)
One more exception to the functionality of the code is that when the monster reaches the player, the line in which the monster reached the player will be shifted to the right by 1 so the program works only if you manage to evade the monster otherwise you can still try to move away from it and the layout will return to normal if you gain distance from the monster.
I added a second version of the code that removes the fleeing behaviour of the monster so you can see how the pathfinding algorithm from the monster to the player is efficient.



 


https://user-images.githubusercontent.com/121896803/227750442-ede9b2f7-048a-4b7c-9722-79c4e31befc7.mp4

