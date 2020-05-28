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
## Rules for Big Oh Notations
Before We begin. Here are some Rules for Big Oh Notations:
* Add the steps
* Ignore the constants
* Drop non dominant notations
* represent different Inputs differently

**Now Let's Discuss Some Orders of Complexity step by step with some code examples** [For Reading](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)
## O(1)
Constant running time. This is the least complexity an algorithm can achieve.

Consider the following code:
### Example 1:
**Python3 program to add two numbers**
```python
num1 = 15							# O(1)
num2 = 12							# O(1)
# Adding both numbers						
sum = num1 + num2 						# O(1)
# printing values 						
print("Sum of {0} and {1} is {2}" .format(num1, num2, sum))	# O(1) 
```
In this program we have 4 lines of code. Each line takes **O(1)** amount of time and following the rule we add them up, it becomes:
```O(1)+O(1)+O(1)+O(1) = O(1+1+1+1) = O(4)```
Ignoring the constants we get:
```O(1)```
### Example 2:
**Consider annother Python program that finds Area of a circle**
```python  
def findArea(r): 
    PI = 3.142 					# O(1)
    return PI * (r*r);				# O(1)
    
print("Area is %.6f" % findArea(5)); 		# O(1)
```
```
= O(1)+O(1)+O(1)
= O(1+1+1)
= O(3)
= O(1)    'ignoring constants'
```

**Conclusion**

The conclusion for **O(1)** is that when ever we find sequence of statements we consider them to be O(1) instead of counting how many lines there are.

## O(n)
An algorithm whose performance will grow linearly (or "linear time") and in direct proportion to the size of the input data set.
Our runtime will increase proportionally to how much our input increases.

Consider the following code:

### Example 1:
**Copying a python list**
```python
list = ['cat', 0, 6.7, ]				# size n
new_list = list.copy()					# O(n)
```
In this program we are creating a copy of a list with **n** elements.
The size can be n no of elements, so copying a list takes n number of steps.
```O(n)```

### Example 2:
**Inserting tuple to the list**
```
mixed_list = [{1, 2}, [5, 6, 7]]				# size n
# number tuple
number_tuple = (3, 4)						# O(1)
mixed_list.insert(1, number_tuple)				# O(n)
```
Inserting an element in a list at any index is done linearly underneath. Inserting at any given index would be within the size of list 'n'.
```
O(1)+O(n)
= O(1+n)
= O(n)
```

### Example 3:
**Adding elements of list by condition**
```python
# List of numbers
numbers = [6, 5, 3, 8, 4, 2, 5, 4, 11] 			#n elements
sum = 0						# O(1)

for val in numbers:				# O(n)
	if val%2==0				# O(1)
        sum = sum+val				# O(1)

print("The sum is", sum)			# O(1)
```
In this code the loop is iterating over the list linearly of size n. so the running time complexity will be:
```
O(1)+O(n)+O(1)+O(1)+O(1)
= O(1+n+1+1+1)
= O(4+n)
= O(n)
```

### Example 4:
**Checking element in List / String**
```
s= "kjn nn nkj bkj  kkb kb kjsbakjdbaskdb hbadk b kb bjhabjhsbsajhbcaj ajhb alhb lk hbaj jhba l"     # size n
x="jhba"				# O(1)
x in s				# O(n)
```
```in``` also searches linearly in a list or string.
```
O(1)+O(n)
= O(n+1)
= O(n)
```
### Different Inputs are represented differently so:
### Example 5:
```python
arr1= list(map(int, input().rstrip().split()))
arr2= list(map(int, input().rstrip().split()))
for a in arr1:
    #O(1) Operations
for b in arr2:
    #O(1) Operations
```
```
Represented like this
O(n)+O(m)
```

### Some List operations in python with O(n) complexity:
* Delete Item
* Iteration
* Del Slice
* min(s)
* max(s)
* Remove
* Reverse
* for i in range(len(alist)): is O(N) because it loops **n** times.
### Some Dictionary operations in python with O(n) complexity:
* Copy
* Get Item
* Set Item
* Delete Item
* Iteration

### Some other examples for O(n):
* Traversing an array
* Traversing a linked list
* Linear Search
* Deletion of a specific element in a Linked List (Not sorted)
* Comparing two strings
* Checking for Palindrome





## O(n<sup>2</sup>)
O(N2) represents an algorithm whose performance is directly proportional to the square of the size of the input data set.

Some Examples would be Nested Loops.

[Programs](https://www.ics.uci.edu/~pattis/ICS-33/lectures/complexitypython.txt)

### Example 1:
```python
for a in range(n):			# O(n)
    for b in range(n):			# O(n)
        print("Doing anything")		# O(1)
```
```
O(n)*O(n)
O(n*n)
O(n<sup>2</sup>)
```
### Example 2:
**Different Inputs nested**
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
### Example 3:
**Recursive call and each time n decreases by 1**
```python
def func(n):
    coun=0
    if n>0:
        for b in range(n):
            print(b)
	func(n-1)
```
This algorithm has complexity of:
```
0+1+2+3+4+5+6+7+8........n(n-1)/2
```
O(n<sup>2</sup>)

## O(n<sup>3 or higher</sup>)
It al depends on how much nested loops we have
```python
for a in range(n):			# O(n)
    for b in range(n):			# O(n)
        for c in range(n):		# O(n)
	    print("Doing anything")     # O(1)
```
```
O(n)*O(n)*O(n)
O(n*n*n)
O(n<sup>3</sup>)
```

## O(log(n))
Logarithmic time complexities usually apply to algorithms that divide problems in half every time.

![image](https://files.realpython.com/media/linear_binary_plot.0fc7428a70f0.png)

Algorithms with logarithmic time complexity are commonly found in operations on **binary trees** or when using **binary search**.

**Note:** We are talking Log<sub>2</sub> (Log Base 2) in computer science.

[Binary Search](https://github.com/Habib0308/Design-Analysis-Of-Algorithms/blob/master/Algorithms%20in%20Python/Binary%20Search.md)

```python
n= 1000000
a=1
while a<=n:
    a*=2
```
This program is incrementing twice itself everytime so complexity becomes ```log(n)```


