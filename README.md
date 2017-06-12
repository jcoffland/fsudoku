# FSudoku
I hate Sudoku.  It's a pointless waste of time that unlike crossword puzzles
leaves you with no new knowledge.  What really irritates me about Sudoku is
that it pretends to be an puzzle for the math minded intelligentsia.  This I
cannot abide.  So a few years ago, while stuck over night in the Lima Airport,
I decided to crush Sudoku, once and for all, by solving all Sudoku puzzles in
one fell swoop and in less than 300 lines of Python.

FSudoku not only solves any Sudoku puzzle it solves it quickly.  The most
difficult standard sized puzzles can be solved in less than two seconds a 3.1GHz
Intel i7-3770S.  The ``puzzles`` directory contains a number of different test
puzzles which you can input into FSudoku like so:

    ./fsudoku < puzzles/hardest.txt

The above produces this output:

```
? ? ?  ? ? ?  ? ? ? 
? 1 ?  6 2 ?  ? 9 ? 
? ? 2  ? ? 9  3 1 ? 

? ? 4  ? ? 6  ? 8 ? 
? ? 8  7 ? 2  1 ? ? 
? 3 ?  8 ? ?  5 ? ? 

? 6 9  1 ? ?  4 ? ? 
? 8 ?  ? 7 3  ? 5 ? 
? ? ?  ? ? ?  ? ? ? 
-------------------
Solving . . . hard . . . done
9 4 5  3 1 7  2 6 8 
8 1 3  6 2 5  7 9 4 
6 7 2  4 8 9  3 1 5 
`
1 2 4  5 3 6  9 8 7 
5 9 8  7 4 2  1 3 6 
7 3 6  8 9 1  5 4 2 

2 6 9  1 5 8  4 7 3 
4 8 1  2 7 3  6 5 9 
3 5 7  9 6 4  8 2 1 
```

Note that FSudoku will also tell you if a puzzle is hard or not.  Any puzzle
which does not succumb immediately to the greedy algorithm is considered hard.
Harder puzzles require testing different possible solutions and backtracking
when those tests fail, until a solution is found.
