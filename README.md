# Bellman Equation for Reinforcement Learning

![Bellman Equation](https://img.shields.io/badge/Bellman-Equation-blue)
![Reinforcement Learning](https://img.shields.io/badge/Reinforcement-Learning-green)

## Overview

This project implements Value Iteration for solving a 4x4 GridWorld problem using Dynamic Programming. The agent starts at the top-left corner (state 0) and aims to reach the bottom-right corner (state 15). The algorithm iteratively updates state values using the Bellman equation until convergence.

The Bellman equation provides a recursive relationship for estimating the value of a state based on the expected rewards of future states. It is fundamental to reinforcement learning and dynamic programming, enabling optimal decision-making in sequential problems.

## Problem Setup

**Grid Size**: 4x4 (16 states)

**Actions**: Up, Down, Left, Right (equal probability)

**Rewards**: -1 per move, 0 for reaching the terminal state

**Transition Probability**: Equal probability for all valid moves

**Discount Factor (γ)**: 1.0 (no discounting)

**Convergence Threshold (θ)**: 1e-4 (stopping criterion)

## Implementation Details

**Initialization**:

- Set grid size and rewards

- Initialize the value function V(s) = 0 for all states

- Define possible actions

**Value Iteration**:

- Iteratively update state values using the Bellman equation:
  
    V(s) = max_a [ R(s) + γ * Σ P(s'|s,a) * V(s') ]

- Handle boundary conditions to ensure the agent does not move outside the grid.

- Stop when the maximum change in state values is less than θ.

**Output**:

Print the final state value function after convergence.

Example Output:

    [[-59.42368 -57.42387 -54.28131 -51.71013]
    [-57.42387 -54.56699 -49.71029 -45.13927]
    [-54.28131 -49.71029 -40.85392 -29.99767]
    [-51.71013 -45.13927 -29.99767   0.     ]]


**Dependencies**:

- Python 3
- NumPy