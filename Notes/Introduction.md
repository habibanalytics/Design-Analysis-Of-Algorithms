# Algorithms
Set of steps to solving a problem. Or

An algorithm is a set of well-defined instructions in sequence to solve a problem.

Here's an example of writing an algorithm:

**An algorithm to add two numbers entered by the user in Python.**

* Step 1: Start
* Step 2: Read values num1 and num2. 
* Step 3: Add num1 and num2 and assign the result to sum.
          sum = num1+num2
* Step 4: Display sum 
* Step 5: Stop
### How to measure efficiency
Checking time isn’t the computer science approach because dfferent time results on different computers with different programming languages.

We use [**Asymtotic Analysis**](https://github.com/Habib0308/Design-Analysis-Of-Algorithms/blob/master/Notes/Asymtotic%20Analysis.md) to Check the efficiency and correctness of algorithm allowing us to think independently of hardware and programminng language. 

In Asymptotic Analysis, we evaluate the performance of an algorithm in terms of input size (we don’t measure the actual running time). We calculate, how the time (or space) taken by an algorithm increases with the input size.
### Correctness & Efficiency
**Correctness** means that a right result is obtained for all possible problem instances (size of the data structure, state of the input — sorted, unsorted, random, nearly-sorted etc)

Algorithm resulting in correct answer or best answer (Perfect algorithms take a lot of time)

**Efficiency** means how the time and computer resources needed to successfully carry out the algorithm

Algorithm that gives good but not best result in minimum time.

### The Cases to analyze an algorithm
We can have three cases to analyze an algorithm:

Best, Average & Worse Case.
#### Best case
Best case is the function which performs the minimum number of steps on input data of n elements.
#### Average case
Average case is the function which performs an average number of steps on input data of n elements.
#### Worse case
Worst case is the function which performs the maximum number of steps on input data of size n. 
* Most of the times, we do worst case analysis to analyze algorithms.
* We must know the case that causes maximum number of operations to be executed.
## Algorithm Comparison
Let's solve a searching problem.

Given a Sorted list of 300 Elements we have to find a number in it.

We will use Linear Search Algorithm and Binary Search to solve our problem. 

In both algorithms the algorithms will perform differently. 

Let's find out how.

## Linear Search
Searching the list from 0th index to the end in order is **Linear search**.

**For example:** In the Problem we have a list of **300 elements**

**(Best Case)**
If the Number to find is in the first index of list, than the algorithm will find it in the first step.

**(Worse Case)**
Number to find is in the end of the list, allgorithm will take 300 iterations to find the number. 

**(Average Case)**
Number to find is somewhere in the center of the list, allgorithm will take 100-200 iterations to find the number. 
# Binary Search
It Searches a sorted array by repeatedly dividing the search interval in half. Begining with an interval covering the whole array. If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. Otherwise narrow it to the upper half. Repeatedly check until the value is found or the interval is empty.

To visualize this algorithm you can check this game:

[Play Guessing Game](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/a-guessing-game)

**For example:** For a list of **300 elements**

**(Best Case)**
 We have to find a number that is present in either the start or end of the list, Algorithm will find the number on its first iteration. 

**(Worse Case)**
We have to find a number that is present in an unknown place in the list, Algorithm will take almost 9 steps to find the number for a 300 elements list. 
