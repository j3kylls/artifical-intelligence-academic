## Chess AI Implementation Overview

This Python-based chess game includes an AI component utilizing the minimax algorithm, integrated with pygame for visualization.

### Getting Started

To initiate the game, run `main.py`, providing the game mode (0 for whites, 1 for blacks) and the desired depth for the AI simulation.

### Board Representation

The `Board` class employs a 2D list to store chess pieces. It includes methods for making and unmaking moves, checking game completion, and evaluating the board.

### Chess Piece Abstraction

The `ChessPiece` class serves as a parent for all pieces, featuring move filtering to prevent illegal moves (e.g., exposing the king). Each piece includes a `get_score()` method for evaluating its importance, with scores ranging from 10 for pawns to 1000 for kings.

### Computer Player

The `Computer` class, a static entity, offers methods for generating random moves or using the minimax algorithm to make AI moves.

### Minimax Algorithm

The minimax algorithm explores all possible moves, recursively simulating opponents' best responses. It assumes adversaries make optimal moves, aiming to maximize its own evaluation score.

### Logging

Enabling logging (`log=True`) during board instantiation produces a `.txt` file via `Logger.py`, displaying the minimax decision tree for the current AI move. This aids in understanding the evaluation process, especially with deeper depths.

### Example

In a given board state, the AI evaluates possible moves at a certain depth, as depicted in a generated `.txt` file. This visualization highlights evaluated scores for each move, aiding in decision-making.

[Custom chess assets!]

By presenting a high-level overview, players and developers gain insight into the game's mechanics and AI decision-making processes.