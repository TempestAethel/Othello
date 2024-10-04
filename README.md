# Othello Game - 

## Table of Contents
1. [Game Overview](#game-overview)
2. [User Interface](#user-interface)
   - [Header](#header)
   - [Game Controls](#game-controls)
   - [Game Board](#game-board)
   - [Game Status](#game-status)
3. [Game Logic](#game-logic)
   - [Initialization](#initialization)
   - [Gameplay Mechanics](#gameplay-mechanics)
   - [AI Mechanics](#ai-mechanics)
   - [Game End Conditions](#game-end-conditions)
4. [Reset and Start Features](#reset-and-start-features)
5. [Styling and Responsiveness](#styling-and-responsiveness)
6. [Conclusion](#conclusion)

## Game Overview

Othello is a strategic board game where players take turns placing pieces on the board. The objective is to have the majority of pieces of one's color on the board at the end of the game. The game can be played in three modes: Two Players, Easy AI, and Hard AI.

## User Interface

### Header
- **Title**: Displays "Othello" prominently at the top of the screen with an appealing font size and text shadow.
- **Info Button**: An information button represented by an "ℹ" icon that redirects users to an external info page (`info.html`) when clicked.

### Game Controls
- **Game Mode Selector**: A dropdown menu allowing players to select between:
  - Two Players
  - Easy AI
  - Hard AI
- **Board Size Selector**: A dropdown for selecting the board size, which can range from 4x4 to 14x14, with 8x8 as the default size.
- **Start Game Button**: A button to initiate the game after selecting the game mode and board size.

### Game Board
- The game board is created dynamically as a grid based on the selected size. Each cell of the grid represents a position on the board where players can place their pieces.
- Cells have hover effects to enhance user interaction.

### Game Status
- A status display shows the current score for both players and indicates whose turn it is.
- Initially hidden, it becomes visible once the game starts.

## Game Logic

### Initialization
- **Game State**: Initializes the board to a specific size and sets the initial player pieces. The board is represented as a 2D array filled with `null` values, except for the four central pieces.
- **Visibility**: The game board is hidden at the start and becomes visible once the game is initialized.

### Gameplay Mechanics
- **Handling Moves**: Players can click on cells to place their pieces if the move is valid. The game checks for valid moves based on the Othello rules, which involve capturing opponent pieces.
- **Valid Move Check**: A function that checks if a cell can be played by determining if it captures at least one opponent piece in any direction.

### AI Mechanics
- **Easy AI**: Makes random valid moves.
- **Hard AI**: Evaluates potential moves by simulating the game state and choosing the move with the highest score based on piece advantage.
- Both AI types operate after the human player, with a slight delay to simulate thinking.

### Game End Conditions
- The game checks if it is over after each move. If there are no valid moves left for either player, the game concludes.
- At the end, a message alerts the players of the winner or if it’s a tie.

## Reset and Start Features

- **Start Game**: The game starts upon clicking the "Start Game" button, which also hides the game controls.
- **Reset Game**: A reset button allows players to return to the initial state, clearing the board and resetting scores. The reset button is hidden during gameplay and only shown after the game ends.

## Styling and Responsiveness

- The application features a modern aesthetic with a gradient background and visually appealing buttons. 
- CSS styles enhance user experience with hover effects, transitions, and responsive design to ensure usability across various screen sizes.

## Conclusion

This Othello game web application offers a complete experience with user-friendly controls, engaging gameplay, and solid AI functionality. Players can enjoy both competitive multiplayer and single-player modes, making it accessible for different audiences. The design and implementation prioritize a smooth user experience and aesthetic appeal, making the game enjoyable to play.
