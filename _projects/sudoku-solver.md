---
title: Sudoku Solver
layout: page
short: A simple propagation-based Sudoku solver written in Java.
---
A sudoku solver is one of programs, each programmer should write at least once
in their lives. I've created mine back in 2004 to test two things - the first
thing was, how much can techniques from constraint programming (propagation of
possible values) improve efficiency in searching. The other thing I wanted to
try was using Eclipse IDE as a replacement for NetBeans.

As for the efficiency - the solver is based on exhaustive search, but it tracks
the list of possible values for each cell, and maintains it throughout the
search. This list is based on the "fixed" cells in the row, column and square
of the cell, and it is updated each time, a value of a cell is fixed. Moreover,
if there is a single possible value left in a cell, it is fixed "immediately",
outside the search algorithm.

It shows, that for simple problems, backtracking is never really used. The
solution of difficult problems from the [Minimal
sudoku](http://mapleta.maths.uwa.edu.au/~gordon/sudokumin.php) site takes a few
hundreds of milliseconds on a common PC.

If you're interested in the source code, or want to try it out, checkout the
repository on [GitHub](http://github.com/ondrasej/Sudoku-Solver).
