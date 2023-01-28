# Simple-pathfinding
Using the layout of pacman with walls as printed "X" and spaces to move in printed with " "(space) from https://github.com/patriciateroltolsa/Pacman, i used the algorithm for pathfinding to find the shortest distance to go from position (y1, x1) to (y2, x1) where y1 is the vertical number of lines from the top and x is how many characters from right to left from wikipedia from the section "sample algorithm" (https://en.wikipedia.org/wiki/Pathfinding).
The function removecells1 used in the function pathfinding1 removes all paths that are walls (so are not valid to move in) and removecells2 used also in pathfinding1 checks if the same position is repeated in later paths(so not to return to the same position as previously).
I have one enemy which is monster1 that is represented by the symbol "#". And the player controlled by arrows key is represented by "O".
Unfortunetaly i didn't use any librairies to represent the graphics in a better way (so the labyrinth is printed in a loop after each iteration the screen is cleared and the cursor is moved to the top right).