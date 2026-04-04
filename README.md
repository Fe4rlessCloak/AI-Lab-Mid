
# Project Overview

## This project explores the implementation of Adversarial Search within a discrete, zero-sum environment. By comparing Stochastic (Random) move selection with Deterministic (Minimax) optimization, this agent demonstrates the power of state-space exploration in game theory.
## Core Features

    Matrix-Based State Management: The board is represented as a 3×3 nested list, ensuring O(1) access time for state updates using board[row][column].

    Hybrid Interface: Features a standard CLI for traditional execution and an Event-Driven GUI using ipywidgets for interactive testing in Jupyter.

    Dynamic Game Modes:

        Stochastic Mode: Computer utilizes randrange() for non-heuristic move selection.

        Minimax Mode: An unbeatable agent utilizing recursive backtracking.

        PvP Mode: Local Human-vs-Human state tracking.

# Artificial Intelligence Logic
## 1. The Minimax Algorithm

### The agent’s "intelligence" is derived from the Minimax Algorithm, a recursive search through the game's state space. The agent treats the game as a tree where each node represents a board configuration.

    Maximizing Player (AI): Searches for the move sequence that leads to the highest possible terminal value.

    Minimizing Player (Human): The algorithm assumes the opponent will play optimally to minimize the AI's utility.

    Backtracking: The agent "simulates" moves, evaluates the result, and "undoes" the move to explore alternative branches, ensuring an exhaustive search of all 255,168 possible game positions.

### Terminal State Utilities:

    +1: AI Victory (Maximum Utility)

    −1: Human Victory (Minimum Utility)

    0: Draw (Neutral Utility)

## 2. Strategic Opening Heuristic

### To optimize the search and adhere to laboratory constraints, the agent is programmed with a Center-Square Priority.

    Logic: The center square (Index 5) is the most strategically significant cell, contributing to four possible winning vectors (Horizontal, Vertical, and two Diagonals). By claiming this "High-Ground" immediately, the agent reduces the human player's potential branching factor from the start.

# Technical Stack & Usage
## Prerequisites

    Environment: Python 3.x, Jupyter Notebook / Lab

    Libraries: ipywidgets (for GUI), random (for stochastic testing)

## Execution

    Initialize: Run all cells in the .ipynb file to load the backend logic and Minimax engine.

    Interface: Scroll to the final cell to access the interactive GUI.

    Selection: Use the dropdown menu to toggle between AI difficulty levels.
