# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: If we have a set of cells S belonhing to the unit U with the same possible values V and |S| == |V|, then according to the Pigeonhole principle (called in Russian Dirichlet's principle) we'll need all these cells to assign all this values and all these values are required to fill all these cells.
Having the constraint that there exist no 2 cells in the unit having the same value, if there is a cell in U and not in S, then it can't have any of the values in V (since they should be assigned to one of the cells in S).
That allows us to propagate the constraint and reduce the amount of possible solutions by removing ones that definitely violate the constraint of the problem.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: We just add the diagonals of the square to the units used as a constraints in constraint propagation techniques (elminate, only choice, naked twins).

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.