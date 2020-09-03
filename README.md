# Week 4

This is the first comprehensive lab. The only new concept is objects. 

Problem: make a sudoku checker using the methods developed in previous labs:
1. Create a board object, and simulate a set of moves:
  * board: 2-D 9x9 int array {private}
  * constuctor: set up empty board (values as -1 * position counter or -1*(9*x+y), all distinct originally) {public}
  * check board: returns true if the board does not have any sudoku rules violations {public} (uses extract sub array and none true from week 2, and grid of multiples from week 2)
  * set location: takes `x`,`y`, and `value`. returns true if valid {public}
  * get possible values: takes `x`,`y` return array of integers with possible values by trying to set each one then returning the state to the empty value {public}
  * 
  
