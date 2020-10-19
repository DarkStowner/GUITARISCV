# GUITARISCV
Final Project for CPE233 Cal Poly SLO 2020
## Introduction
The game is essentially a rhythm game, where you have to time tapping keys with “notes” coming down from the top of the screen. It is similar to popular modern games such as Guitar Hero, or the mobile games where you tap on the screen in time with the music. It does not have levels, but each game is different because the notes come down randomly every time. To play the game, a keyboard is required as well as a vga display. The game is lightweight and operates on a 50MHz OTTER processor.

## Software Design
During the initialization, three fixed notes are generated and drawn on screen as a “warm up” sequence. The four notes displayed on screen are stored in a word that shifts everytime a new note gets loaded.
The program runs in a loop, it draws a background, generates a new random note, draws it, and draws the three preceding notes after it. Once everything is drawn, the program waits for an interrupt to be triggered. This interrupt checks to see if the key pressed corresponds to the right note. Once this is determined, the program either proceeds to add one to the score and go back up the loop, or goes to a game over state, waiting to be reset.
