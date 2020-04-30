# Binary Search
Works on sorted arrays. 

## step-by-step description of using binary search to play the guessing game:
1 Let min = 1min=1m, i, n, equals, 1 and max = nmax=nm, a, x, equals, n.
2 Guess the average of max and min, rounded down so that it is an integer.
3 If you guessed the number, stop. You found it!
4 If the guess was too low, set minminm, i, n to be one larger than the guess.
5 If the guess was too high, set maxmaxm, a, x to be one smaller than the guess.
6 Go back to step two.
