# **Game Playing in Artificial Intelligence**

This repository contains an AI-powered implementation of **Tic-Tac-Toe** using the **Minimax Algorithm** with **Alpha-Beta Pruning** to optimize decision-making and gameplay.

---

## **Submission Guidelines**
- Submit your work via **Google Classroom**.
- Submissions outside of Google Classroom will **not be accepted**.
- Include:
  - A Python file: `YourRollNo.py`
  - A Jupyter Notebook: `YourRollNo.ipynb`

---

## **Problem Description**

### **Game Overview**
Tic-Tac-Toe is a simple, two-player game played on a 3x3 grid. The players alternately mark the cells with `X` or `O`. The objective is to place three consecutive marks in:
1. A horizontal row,
2. A vertical column, or
3. A diagonal line.

If all cells are occupied without three consecutive marks for either player, the game ends in a draw.

---

### **Algorithmic Approach**

#### **1. Minimax Algorithm**
The Minimax algorithm simulates all possible moves to determine the optimal strategy for both players.

- **Key Components**:
  - **MOVEGEN**: Generates all possible moves for the current state.
  - **STATICEVALUATION**: Assigns a score to game states based on the outcome.

- **Backtracking Logic**:
  - For `Player X` (Maximizer): Choose the move that maximizes the score.
  - For `Player O` (Minimizer): Choose the move that minimizes the score.

#### **2. Alpha-Beta Pruning**
Alpha-Beta pruning optimizes the Minimax algorithm by eliminating unnecessary branches that don't affect the outcome.

- **Alpha**: The highest score achievable by the Maximizer so far.
- **Beta**: The lowest score achievable by the Minimizer so far.

- **Key Conditions**:
  - If `alpha >= beta`, stop exploring further down the tree.

- **Benefits**:
  - Reduces the number of nodes evaluated, improving efficiency.

---

## **Lab Task: AI Tic-Tac-Toe Implementation**

### **Rules of the Game**
1. Two players alternate turns, choosing either `X` or `O`.
2. A player wins by forming three consecutive marks in a row, column, or diagonal.
3. The game ends when:
   - A player wins, or
   - All cells are occupied (resulting in a draw).

---

### **Provided Helper Functions**

The following helper functions are included in the implementation:

1. `def initial_state()`: Returns the starting state of the board.
2. `def player(board)`: Returns the player whose turn is next.
3. `def actions(board)`: Returns a set of all possible actions `(i, j)` available on the board.
4. `def result(board, action)`: Returns the resulting board state after a specific action.
5. `def winner(board)`: Identifies the winner of the game, if there is one.
6. `def terminal(board)`: Checks if the game is over. Returns `True` if over, otherwise `False`.
7. `def utility(board)`: Evaluates the board:
   - Returns `1` if `X` wins.
   - Returns `-1` if `O` wins.
   - Returns `0` for a draw.

---
