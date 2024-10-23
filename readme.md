# KEYMAN Game
KEYMAN is an assembly language-based console game that runs on Windows. The game features a graphical interface created using ASCII art and allows users to interact with the game using keyboard inputs.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Game Controls](#game-controls)
- [Code Structure](#code-structure)


### Installation
To run the KEYMAN game, you need to have an assembler and linker that supports x86 assembly language. The game is designed to run on Windows.

1. Clone the repository:
```bash
git clone https://github.com/yourusername/KEYMAN.git
cd KEYMAN
```
2. Assemble and link the code using an assembler like MASM:
```bash
ml /c /Zd /coff KEYMAN_final.asm
link /SUBSYSTEM:CONSOLE KEYMAN_final.obj
```

### Usage
After assembling and linking the code, you can run the game by executing the generated executable file:
```bash
KEYMAN_final.exe
```

#### Game Controls
The KEYMAN game can be played using the following keyboard controls:
- Enter: Start the game
- Esc: Exit the game

### Code Structure
The main game logic and data are contained in the KEYMAN_final.asm file. Below is a brief overview of the key sections:

- Data Section: Contains definitions for ASCII art, game text, and other constants.
- Code Section: Contains the main game loop, input handling, and rendering logic.

### Key Variables and Functions
- Data Variables:
    - score: Stores the player's score.
    - scoreBar, lengthofBar, barAttributes: Define the score bar's position, length, and color.
    - ShowScore, scoreText, scoreAttributes: Define the score display's position, text, and attributes.
    - titleStr: Title of the game window.
    - meau0 to meau15: ASCII art for the menu screen.
- Functions:
    - main: Entry point of the game.
    - outmeau: Displays the menu screen.
    - START_GAME: Starts the game (not fully shown in the provided code).
    - GAME_OVER: Ends the game and displays the final score.
    - updateScore: Updates the player's score and renders the score bar.