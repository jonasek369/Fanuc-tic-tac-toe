# FANUC Tic-Tac-Toe

An autonomous Tic-Tac-Toe game running on a FANUC industrial robot.

Game logic is implemented in **KAREL**, while all robot motion is programmed using **TP (Teach Pendant) programs** by [KurkyOkurky](https://github.com/kurkyokurky) (not public yet).

---

## Features

- Teach Pendant (TP) input for move selection
- Robot vs. player gameplay
- Automatic board cleanup after each game

---

## Automatic Puck Placement

The robot detects button presses on the teach pendant, places a puck in the selected grid position, and then counters the player’s move.

![Gameplay GIF](/media/game.gif)

---

## Automatic Puck Cleanup

After the game concludes, the robot clears the board and returns all pucks to their designated storage stacks.

![Cleanup GIF](/media/cleaning.gif)

---

## How to Run This Project

make sure registers R[10] - R[15] are free, Check `fanuc_piskvorky.kl` for documentation


1. Compile all KAREL programs.
2. Upload all `.PC` and `.STM` files to the robot.
3. Run `fanuc_piskvorky.pc` in automatic mode.
4. Open `fanuc_piskvorky_site.stm` in the TP browser.
5. Press any button on the TP to place a puck on the board and wait for the robot’s response.

---

## The Idea Board

This is the board where we wrote down our ideas. All registers and functions are documented in the code.

![Idea Board](/media/info-board.jpg)

---

## Work in Progress

This project is still a work in progress, and its behavior may change.
