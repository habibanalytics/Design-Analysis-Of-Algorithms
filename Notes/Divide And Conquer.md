## Divide-And-Conquer
A divide-and-conquer algorithm works by recursively breaking down a problem into two or more sub-problems of the same or related type, until these become simple enough to be solved directly. The solutions to the sub-problems are then combined to give a solution to the original problem.

This technique can be divided into the following three parts:

1). Divide: This involves dividing the problem into some sub problem.
2). Conquer: Sub problem by calling recursively until sub problem solved.
3). Combine: The Sub problem Solved so that we will get find problem solution.

```
DAC(a, i, j)
{
    if(small(a, i, j))
      return(Solution(a, i, j))
    else 
      m = divide(a, i, j)               // f1(n)
      b = DAC(a, i, mid)                 // T(n/2)
      c = DAC(a, mid+1, j)            // T(n/2)
      d = combine(b, c)                 // f2(n)
   return(d)
}
```

### Algorithms that are under Divide And Conquer
Binary Search 
Quicksort
Merge Sort 
Closest Pair of Points 
Strassen’s Algorithm 
Cooley–Tukey Fast Fourier Transform (FFT) algorithm
Karatsuba algorithm for fast multiplication





