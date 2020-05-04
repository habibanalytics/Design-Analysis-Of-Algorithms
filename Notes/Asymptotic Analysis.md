# Asymtotic Analysis
In Asymptotic Analysis, we evaluate the performance of an algorithm in terms of input size (we don’t measure the actual running time). We calculate, how the time (or space) taken by an algorithm increases with the input size.

## Asymptotic Notations
Mathematical way of representing time complexity.
We check how many number of times a statement is executed by some notations.

**Types of Asymptotic Notation:**
* Big-Oh(O) notation
* Big-Theta(Θ) notation
* Big-Omega(Ω) notation
### Big-Oh(O) notation
* Add the  steps
* Represents upper bound.
* Ignores constants
* Drop non dominant notations
* Different Inputs represented differently
* Mostly used
* Used for Worse Case
### Big-Omega(Ω) notation
* Lower Bound
* Best Case
### Big-Theta(Θ) notation
* Average Bound
* Average Case

# Big-Oh(O)
Before we begin representing terms. Here are some Types of functions, limits, and simplification
```
Logarithmic Function:  log n
Linear Function:  an + b
Quadratic Function:  an^2 + bn + c
Polynomial Function:  an^z + . . . + an^2 + a*n^1 + a*n^0, (where z is some constant)
Exponential Function:  a^n, where a is some constant
```
Here are some Asymtotic Notations:

O(1) constant
O(log(n)) logarithmic
O((log(n^c)) polylogarithmic
O(n) linear
O(n^2) quadratic
O(n^c) polynomial
O(c^n) exponential

| Type| Notation |
| ------------------ |:-------------:|
| constant |O(1)|
| logarithmic |O(log(n))|
| polylogarithmic |O((log(n^c))|
| linear|O(n)|
| quadratic|O(n^2)|
| polynomial|O(n^c)|
| exponential|O(c^n)|

1 < log(n) < n^(1/2) < n < nlog(n) < n^2 < n^3 < ........ n^k < 2^n < 3^n ...... < n^n


```python
def func(arrA, arrB):
    coun=0
    for a in arrA:
        for b in arrB:
            if a==b:
                count+=1
     return count
```
This algorithm has O(a*b) complexity

```python
x= 5*(15*20)
y= 15-2
print(x+y)
```
total_time= O(1) + O(1) + O(1) = 3*O(1) "Ignore constants" = O(1)

```python
for a in range(n):
    for b in range(n):
        print("Doing anything")
```
total_time= O(n*n) = O(n^2)


You can check out efficiency of algorithms over each other [here.](https://www.bigocheatsheet.com/) 

![image](https://cdn-media-1.freecodecamp.org/images/1*HwLR-DKk0lYNEMpkH475kg.png)





