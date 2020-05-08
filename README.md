# SudokuSolver
Sudoku Solver Application in Python Language using Pygame GUI

## What is sudoku ?

Sudoku is a logic-based, combinatorial number-placement puzzle. The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid (also called "boxes", "blocks", or "regions") contain all of the digits from 1 to 9. The puzzle setter provides a partially completed grid, which for a well-posed puzzle has a single solution.

Completed games are always an example of a Latin square which include an additional constraint on the contents of individual regions. For example, the same single integer may not appear twice in the same row, column, or any of the nine 3×3 subregions of the 9×9 playing board.

French newspapers featured variations of the Sudoku puzzles in the 19th century, and the puzzle has appeared since 1979 in puzzle books under the name Number Place.[5] However, the modern Sudoku only began to gain widespread popularity in 1986 when it was published by the Japanese puzzle company Nikoli under the name Sudoku, meaning "single number".It first appeared in a U.S. newspaper, and then The Times (London), in 2004, thanks to the efforts of Wayne Gould, who devised a computer program to rapidly produce unique puzzles.

## Backtraking Algorithm

The aim of this problem is to construct the smaller 3x3 grid with numbers from 1 to 9. Suppose we have placed a number in the first row to solve the first minigrid but the same number is repeating in the first row when we are trying to solve the seocnd mini-grid - this means we have not reacheda feasible solution for the problem so we backtrack to the first mini-grid and replace the number to find another solution for the first mini-grid. This behaviour of backtracking to a previous position and looking for an alterantive solution to meet all the conditions is knwon as backtracking algorithm.

## Algorithm explained
```
1.Create a function that checks after assigning the current index the grid becomes unsafe or not. Keep Hashmap for a row, column and boxes. If any number has a frequency greater than 1 in the hashMap return false else return true; hashMap can be avoided by using loops.
2.Create a recursive function which takes a grid.
3.Check for any unassigned location. If present then assign a number from 1 to 9, check if assigning the number to current index makes the grid unsafe or not, if safe then recursively call the function for all safe cases from 0 to 9. if any recursive call returns true, end the loop and return true. If no recursive call returns true then return false.
4.If there is no unassigned location then return true.
```


