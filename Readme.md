# N-Queens Genetic Algorithm Solver

## Overview

This repository contains an implementation of a Genetic Algorithm (GA) to solve the N-Queens problem. The N-Queens problem involves placing N queens on an N×N chessboard so that no two queens threaten each other. This implementation uses GA techniques such as selection, crossover, mutation, and elitism to evolve solutions over generations.

## Features

- **Genetic Algorithm Techniques**: The solution employs key GA techniques including initialization, fitness evaluation, selection, crossover, mutation, and elitism.
- **Flexible Parameters**: The board size, population size, number of generations, and mutation rate can be adjusted.
- **Visualization**: The final solution is printed in a readable board format.

## How It Works

### Initialization

The initial population is generated with each individual represented as a permutation of queen positions. Each individual is a list where the index represents the column and the value at that index represents the row position of the queen.

### Fitness Function

The fitness function calculates the number of non-attacking pairs of queens. A higher fitness score indicates fewer clashes (attacks) between queens.

### Selection

Selection is performed using a weighted random choice based on the fitness scores. Fitter individuals have a higher chance of being selected for reproduction.

### Crossover

Crossover combines pairs of parents to produce offspring. A random crossover point is chosen, and the offspring inherit segments from both parents, ensuring no duplicate positions in a single individual.

### Mutation

Mutation introduces random changes to individuals to maintain genetic diversity. Each gene (queen position) in an individual has a chance to be swapped with another position.

### Elitism

Elitism ensures that the top-performing individuals are carried over to the next generation, preserving good solutions.

### Evolution

The algorithm evolves the population over a set number of generations, continuously improving the solutions through selection, crossover, mutation, and elitism.

## Example Output
Solution:
. . . . . . Q .
. Q . . . . . .
. . . Q . . . .
Q . . . . . . .
. . . . . . . Q
. . . . Q . . .
. . Q . . . . .
. . . . . Q . .

## Usage

1. **Initialize the Solver**: Create an instance of `NQueensGeneticAlgorithm` with desired parameters.
2. **Solve the Problem**: Call the `solve()` method to find a solution.
3. **Print the Solution**: Use `print_board(solution)` to display the solution in a readable format.

### Example

```python
board_size = 8
genetic_solver = NQueensGeneticAlgorithm(board_size)
solution = genetic_solver.solve()
print("Solution:")
print_board(solution)

