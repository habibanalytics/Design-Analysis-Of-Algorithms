# Algorithms

Set of steps to solving a problem

### How to measure efficiency

Checking time isn’t the computer science approach because dfferent time results on different computers with different programming languages.

We use **Asymtotic Analysis** to Check the efficiency and correctness of algorithm allowing us to think independently of hardware and programminng language

### Correctness
Algorithm resulting in correct answer or best answer (Perfect algorithms take a lot of time)
### Efficient
Algorithm that gives good but not best result in minimum time.

Case Scenerios to know about:

*	#### Best case

Best case is the function which performs the minimum number of steps on input data of n elements.
*	#### Average case

Average case is the function which performs an average number of steps on input data of n elements.
*	#### Worse case

Worst case is the function which performs the maximum number of steps on input data of size n. 

# Guessing Game

Given a **sorted list** computer guessed a random number from it.
We search that number given the computer tells us if the guessed number is larger or smaller than our selected value.

[Play Guessing Game](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/a-guessing-game) (You'll need account of khan academy to access)

# Linear Search
Searching the list from 0th index to the end in order is **Linear search**.
Best, Worse and average case scenerio depends on luck for this matter.

**For example:** For a list of **300 elements**

*Computer selects 1*, and you get the number on your first guess. **(Best Case)**

*Computer selects 300*, you would need 300 guesses **(Worse Case)**

*Computer selects 150*, you would need 150 guesses **(Average Case)**
# Binary Search
* Works on sorted list.
* how many times length of list divided by 2 results in 1 is the number of steps it takes to find our number.

**For example:** For a list of **300 elements**

*Computer selects First Element*, you'll find the number on your first guess. **(Best Case)**

*Computer selects some element in the middle*, you would need maximum of 9 guesses to find the number **(Worse Case)**
