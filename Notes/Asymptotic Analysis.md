# Asymtotic Analysis
In Asymptotic Analysis, we evaluate the performance of an algorithm in terms of input size (we don’t measure the actual running time). We calculate, how the time (or space) taken by an algorithm increases with the input size.

## Asymptotic Notations
Mathematical way of representing time complexity.
We check how many number of times a statement is executed by some notations.
So we can't say it takes 1.2 seconds of time. We will always represent time-complexity with some notation

**Types of Asymptotic Notations:**
* Big-Oh(O) notation
* Big-Theta(Θ) notation
* Big-Omega(Ω) notation
### Big-Oh(O) notation
* Mostly used
* Used for Worse Case analysis
* Represents upper bound

[For More Details](http://web.mit.edu/16.070/www/lecture/big_o.pdf)
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
**Here are some Asymtotic Notations for the above Functions:**
| Type| Notation |
| ------------------ |:-------------:|
| constant |O(1)|
| logarithmic |O(log(n))|
| polylogarithmic |O((log(n<sup>c</sup>))|
| linear|O(n)|
| quadratic|O(n<sup>2</sup>)|
| polynomial|O(n<sup>c</sup>)|
| exponential|O(c<sup>n</sup>)|

## Order of Complexity
1 **<** log(n) **<** n<sup>(1/2)</sup> **<** n **<** nlog(n) **<** n<sup>2</sup> **<** n<sup>3</sup> **<** ........ n<sup>c</sup> **<** 2<sup>n</sup> **<** 3<sup>n</sup> ...... **<** c<sup>n</sup>

![image](https://cdn-media-1.freecodecamp.org/images/1*HwLR-DKk0lYNEMpkH475kg.png "Source: freecodecamp.org")

For more info, you can also check out efficiency of Algorithms over each other [here.](https://www.bigocheatsheet.com/) 

**Now Let's Discuss Some Orders of Complexity step by step with some code examples**

## Rules for Big Oh Notations
Before We begin. Here are some Rules for Big Oh Notations:
* Add the steps
* Ignore the constants
* Drop non dominant notations
* represent different Inputs differently

## O(1)
Constant running time. This is the least complexity an algorithm can achieve.

Consider the following code:
### Example 1:
**Python3 program to add two numbers**
```python
num1 = 15
num2 = 12
# Adding both numbers
sum = num1 + num2 
# printing values 
print("Sum of {0} and {1} is {2}" .format(num1, num2, sum)) 
```
In this program we have 4 lines of code. Each line takes **O(1)** amount of time and following the rule we add them up, it becomes:
```O(1)+O(1)+O(1)+O(1) = 4*O(1)```
Now Ignoring the constants we get:
```O(1)```
### Example 2:
**Consider annother Python program that finds Area of a circle**
```python  
def findArea(r): 
    PI = 3.142
    return PI * (r*r);
    
print("Area is %.6f" % findArea(5)); 
```
Even if function call is considered a step than result is same:
```
= O(1)+O(1)+O(1)+O(1)
= 4*O(1)
= O(1)
```
### Example 3:
**If the number is positive or negative, we print an appropriate message**
```python
num = int(input("Input a number"))
if num > 0:
    print(num, "is a positive number.")
print("This is always printed.")
elif num < 0:
    print(num, "is a Negative number.")
else:
    print("Number is Zero")
```
Each Conditional statement has O(1) time complexity.
```
= O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)+O(1)
= 8*O(1)
= O(1)  #ignoring constants
```
**Conclusion**

The conclusion for O(1) is that when ever we find sequence of statements we consider them to be O(1) instead of counting how many lines there are.



















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


