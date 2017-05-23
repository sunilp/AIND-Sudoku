# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A:
Constraint propagation is a technique of applying the same constraint in loop  until a solution is obtained,
 or the constraint can no longer be provide better solution (converges).

In this sudoku, we apply naked twins as a new strategy to reduce the number of possibilities and thus calculations.
 Naked twins is the strategy as explained in the class videos, to identify a pair of boxes belonging to the same set of peers that have the same 2 numbers as possibilities,
 and eleminate these two numbers from all the boxes that have these two boxes as peers.
We applied constrains propagation, as seen in naked_twins method, to first find the potential twins by checking the length as 2 , and then remove from other peer boxes.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A:
For diagonal sudoku, we incorporated diagonal contraint as an additional unit in sudoku.
 Once this is done, all the diagonal entries will have the corresponding diagonal entries as their peers. so the diagonal constrains get satisfied.
 As, this approach might not work for general sudoku cases which are not diagonal, so captured a diagonalFlag to set which can used when working with not
 a diagonal sudoku.
 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

