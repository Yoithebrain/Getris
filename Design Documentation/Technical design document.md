# Technical Design Documentation

This document describe the technical design of Getris

## Timers
GoDot features timers, these will be used to keep the game running till the end and update everything in regards to the state of the game.

A ticker to keep blocks moving downwards based on the pace of the game, described as level.
The equation for pace is this:
period = 1 / level

Have a keyboard repeat delay timer (repeater) for moving when holding down a key

Level up timer - increase the level based on time... (I'm changing this for score)...

## State
The game will be started or stopped (Playing or not playing)
The state are booleans due to the fact that they are simplistic in nature as the only time the game will be inactive is when a game hasn't been started.

## Event processing
```
New game button pressed
  Reset game
  Start ticker
  Playing = true
Ticker ticked
  Try to move shape down
  If stuck:
    Add shape to grid
    Check lines
    Remove lines
    Update score
  If end game:
    Stop ticker
    playing = false
    Display game over
    Load highscore table
    Compare score with high score table
    If new highscore:
      Display name input
      Save name and score
    Display high scores
  Else:
    Add shape
    
Left pressed:
  Try to move shape to the left
Right pressed:
  Try to move shape to the right
Rotate pressed:
  Try to rotate shape clockwise
Down just pressed:
  Set ticker period to soft drop speed
Down released:
  Reset ticker period
Space just pressed:
  Set ticker period to hard drop speed
Music button:
  Toggle audio output

## Major functions
Check for valid move postions

Check for completed lines

Add shape to grid
