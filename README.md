# README


## Genetic Programming Algorithm with Enhanced Features

This repository implements a Genetic Programming (GP) algorithm with several advanced enhancements, including dynamic mutation rates, probabilistic crossover, fitness penalties for complexity, and dynamic population size adjustments. The primary goal is to evolve trees (representing Boolean expressions) that match a target truth table.

---

## Features

1. **Boolean Tree Representation**
   - Boolean operators (`AND`, `OR`, `NOT`) are used to create tree structures.
   - Leaf nodes are variables (`A`, `B`, `C`) or constants (`0`, `1`).

2. **Fitness Evaluation**
   - Compares each tree's output to a target truth table.
   - Applies a penalty for larger or more complex trees to balance accuracy and simplicity.

3. **Enhanced Crossover and Mutation**
   - **Probabilistic Crossover:** Merges two parent trees with a higher probability of inheriting traits from fitter parents.
   - **Dynamic Mutation Rate:** Adjusts mutation probability across generations to fine-tune the exploration-exploitation balance.

4. **Dynamic Population Size**
   - Expands or contracts the population based on stagnation or significant improvements in fitness.

5. **Tournament Selection**
   - Randomly selects a subset of individuals to compete, ensuring diversity and evolutionary pressure.

6. **Fitness Progress Tracking**
   - Visualizes the best individual's fitness score over generations using Matplotlib.


---

### Key Functions
- **`evaluate_tree(tree, inputs)`**  
   Evaluates a tree's output for a given input.
   
- **`random_individual(depth=3, max_depth=6)`**  
   Generates a random tree (individual) with a specified depth.

- **`fitness(individual)`**  
   Computes the fitness score by comparing outputs and applying a complexity penalty.

- **`probabilistic_crossover(parent1, parent2)`**  
   Combines subtrees from two parent trees based on their fitness.

- **`dynamic_mutate(individual, generation, max_generations)`**  
   Mutates an individual with a probability that decreases over generations.

- **`dynamic_population_size(fitness_progress, population)`**  
   Adjusts the population size based on fitness improvement or stagnation.

- **`genetic_programming(generations=50, population_size=100)`**  
   Orchestrates the GP process, evolving a population over multiple generations.

---

## Example Output

- **Best Individual:**  
   The evolved tree that matches the target truth table (e.g., `(OR, (AND, 'A', 'B'), 'C')`).

- **Fitness Progress Plot:**  
   Visual representation of how the best fitness score improved over generations.

---

## Customization

- **Dataset:**  
   Modify the `dataset` variable to experiment with other Boolean expressions.

- **Operators:**  
   Add new operators to the `operators` dictionary (e.g., XOR).

- **Algorithm Parameters:**  
   Adjust parameters like `generations`, `population_size`, or `max_depth` to explore different behaviors.

---



## How to Customize

- Modify the `dataset` to test different truth tables.
- Adjust parameters like population size and number of generations to explore different results.

