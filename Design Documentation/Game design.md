# Game design document

Getris is merely a clone of the original tetris, made to learn the GoDot engine from scratch
The mechanics and shapes of the game will be copied directly from tetris itself as described by wikipedia.
Most of my learning will be done by following GDScript Dudes tutorial in building this thing.

## Controls

* Space bar - Hard drop of shape
* Down arrow - Soft drop of shape
* Left arrow - Move left
* Right arrow - Move right
* Up arrow - Rotate clockwise
* New game button
* Pause button
* Music button - On/Off state

## Scene elements
10 column x 20 row - just like classic tetris

Statistics:
* High scores
* Level
* Scores
* Lines

### Elements around grid
* Next shape
* Game over banner
* New game button
* Pause button
* Music button - State toggle

## Shapes
These will be textures arranged in a grid that have a grid map, color and a probability of occurence(True random like the orignal)

## Scoring
Points will be in one decimal to keep it simple
* Single line - 1 point
* Double line - 2 points
* Triple line - 4 points
* Four line - 8 points

## Highscore
Game will save scores into a table file of scores, only storing around the top 10 scores ever achieved, these will be displayed when a game ends. 
If one is succesfull in beating a score, then all scores including that score moves down one space. This will essentially cause the lowest high score to "fall out of the table".

If I have time I may create a backup file that will contain all scores ever achieved in the game, sorted by the number of points. This backup file would be invoked everytime 
a previous high score "falls out of the top 10"

## Animations
Visual effect when a line or several lines are cleared at once

## Sounds
Some music and other misc. things
