# Week 4

This is the first comprehensive lab and is built on the results from previous labs. 
In all this lab includes the following topics:
* 2-D arrays
* boolean logic
* objects
* methods

# Your Tasks
Your task will be to make a Sudoku simulator. 
The simulator object when constructed will have an empty board, 
and calls to the set location method will simulate the placement of numbers into this grid. 
Each time a number is placed (or at any time) the board can be checked to see if any of the sudoku rules are violated. 
A method call can also list the numbers that can be set at a location without causing a violation. 

You will create two classes, as well as importing (copying) the classes developed in the previous two labs. 
The first new class is the `Sudoku` class which will define the board objects, 
and the second is a `tester` class which will use `JUnit` to test `Sudoku`. 

## `Sudoku.java`
All methods and variables within the `Sudoku` class will be non-static unless specified.
The scope is specified for each and should not be changed. 

Variables:
* `private int[][] board` -- a 2-D 9x9 int array that will store the current state of the board;
Methods:
* `public Sudoku()` -- the only constuctor available for this class. It will perform the following:
  * allocate the `board` variable
  * intialize the `board` so each cell contains a unique value (`-1 * ( ( 9 * row ) + col )` where `row` and `col` are the row and column index).
* `private boolean checkBoard()` -- This method checks if the current board is valid. Returns true if the board does not have any sudoku rules violations. Remember a board is valid if each number 1-9 appears at most once in each row and column, as well as the 9 non-overlapping 3x3 grids.
  * This method will utilize the following methods from the previous labs: `extractAndTest.extractSubArray`, `searchAndPrint.gridOfMultiples`, and `extractAndTest.noneTrue`. This is a chance for students to make up for possible mistakes in the original assignments. 
* `public boolean setLocations(int x, int y, int value)` -- Attempts to set `board[x][y]` to `value`, it returns `true` if this value can be set and `false` if there was a problem. **If a problem was found, the state of the board will be the same as it was.** Problems include:
  * `x` or `y` being out of bounds
  * `board[x][y]` already being set (i.e. had a non-negative value)
  * making the assingment violates the rules (i.e. `checkBoard()` returns `false` when it is assigned)
* `public getPossibleValues()`: takes `x`,`y` return array of integers with possible values by trying to set each one then returning the state to the empty value {public}

