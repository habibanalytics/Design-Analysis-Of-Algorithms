# Binary Search
Works on sorted arrays. 

## step-by-step description of using binary search to play the guessing game:
1. Let min = 1 and max = n.
2. Guess the average of max and min, rounded down so that it is an integer.
3. If you guessed the number, stop. You found it!
4. If the guess was too low, set min to be one larger than the guess.
5. If the guess was too high, set max to be one smaller than the guess.
6. Go back to step two.
