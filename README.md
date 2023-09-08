# Connect Four with Ant Colony Optimization (ACO)

This Python code implements a game of Connect Four where the computer player (Player X) uses the Ant Colony Optimization (ACO) algorithm to make its moves. Connect Four is a two-player connection game in which the players choose a color and take turns dropping colored discs into a grid. The goal is to be the first to form a horizontal, vertical, or diagonal line of four discs of your color.

## How to Play

1. Run the Python script.
2. The game board is displayed, and you will play as Player O, while the computer plays as Player X.
3. Player O selects a column to place their disc by entering a number from 0 to 6 (representing the column number).
4. The computer (Player X) will then make its move using the ACO algorithm.
5. The game continues with players taking turns until one of the following conditions is met:
   - A player forms a horizontal, vertical, or diagonal line of four discs of their color and wins the game.
   - The game board is completely filled with discs, resulting in a tie.
6. The game outcome is displayed, and you can choose to play again if you wish.

## ACO Algorithm

The computer player (Player X) uses the Ant Colony Optimization (ACO) algorithm to select its moves. ACO is a metaheuristic algorithm inspired by the foraging behavior of ants. In this implementation, the algorithm maintains a pheromone matrix that represents the strength of each move. It uses a set of "ants" to update the pheromone levels based on their experience.

- Each ant starts at the current game state and selects a sequence of moves based on the pheromone levels and a heuristic evaluation function.
- The heuristic evaluation function estimates the strength of each possible move by counting the number of pieces in a row, column, or diagonal.
- The algorithm selects the move with the highest pheromone level, with randomness to introduce exploration.
- The pheromone levels are updated based on the moves made by the winning ant.

## How the Code Works

1. The game board is represented as a 6x7 grid, with '.' representing an empty cell, 'O' representing Player O's disc, and 'X' representing Player X's disc.
2. The `select_move` function uses the ACO algorithm to choose Player X's moves.
3. The `heuristic_evaluation` function computes a score for the game state based on the number of discs in a row, column, or diagonal.
4. The `game_over` function checks if the game is over with a win condition.
5. The `game_tied` function checks if the game is tied with no more valid moves.
6. The `print_board` function displays the current game board.
7. The `play_game` function manages the game loop.

## Acknowledgments

- The ACO algorithm in this code is a simplified version for demonstration purposes.
- Connect Four is a classic board game designed by Howard Wexler and Ned Strongin.
