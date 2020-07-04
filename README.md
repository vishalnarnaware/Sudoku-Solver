# Solve Sudoku with AI

## Synopsis

In this project, you will extend the Sudoku-solving agent developed in the classroom lectures to solve _diagonal_ Sudoku puzzles and implement a new constraint strategy called "naked twins". A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the added constraint that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the rows, columns, and 3x3 blocks). The naked twins strategy says that if you have two or more unallocated boxes in a unit and there are only two digits that can go in those two boxes, then those two digits can be eliminated from the possible assignments of all other boxes in the same unit.


## Quickstart Guide

## Instructions

You must complete the required functions in the 'solution.py' file (copy in code from the classroom where indicated, and add or extend with new code as described below). The `test_solution.py` file includes a few unit tests for local testing, but the primary mechanism for testing your code is the Udacity Project Assistant command line utility described in the next section.

YOU SHOULD EXPECT TO MODIFY OR WRITE YOUR OWN UNIT TESTS AS PART OF COMPLETING THIS PROJECT. There is no requirement to write test cases, but the Project Assistant test suite is not shared with students so writing your own tests may be necessary to find and resolve any errors that arise there.

1. Add the two new diagonal units to the `unitlist` at the top of solution.py. Re-run the local tests with `python -m unittest` to confirm your solution. 

1. Copy your code from the classroom for the `eliminate()`, `only_choice()`, `reduce_puzzle()`, and `search()` into the corresponding functions in the `solution.py` file.

1. Implement the `naked_twins()` function (see the pseudocode [here](https://github.com/udacity/artificial-intelligence/blob/master/Projects/1_Sudoku/pseudocode.md) for help), and update `reduce_puzzle()` to call it (along with the other existing strategies). Re-run the local tests with `python -m unittest -v` to confirm your solution.

1. Run the remote tests with `udacity submit` to confirm your solution. If any of the remote test cases fail, use the feedback to write your own local test cases for debugging.

## Visualization

**Note:** The `pygame` library is required to visualize your solution -- however, the `pygame` module can be troublesome to install and configure. It should be installed by default with the AIND conda environment, but it is not reliable across all operating systems or versions. Please refer to the pygame documentation [here](http://www.pygame.org/download.shtml), or discuss among your peers in the slack group if you need help.

Running `python solution.py` will automatically attempt to visualize your solution, but you mustuse the provided `assign_value` function (defined in `utils.py`) to track the puzzle solution progress for reconstruction during visuzalization.
