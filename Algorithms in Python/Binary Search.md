# Binary Search
It is a searching algorithm that finds the position of a target value within a sorted array. 
Binary search compares the target value to the middle element of the array.

## Algorithm:
Steps of the binary search:
* Calculate the middle of the list.
* If the searched value is lower than the value in the middle of the list, set a new right bounder.
* If the searched value is higher than the value in the middle of the list, set a new left bounder.
* If the search value is equal to the value in the middle of the list, return the middle (the index).
* Repeat the steps above until the value is found or the left bounder is equal or higher the right bounder.
## Iterative Code in Python:
```python
def binary_search(data, value):
    n = len(data)
    left = 0
    right = n - 1
    while left <= right:
        middle = (left + right) // 2
        if value < data[middle]:
            right = middle - 1
        elif value > data[middle]:
            left = middle + 1
        else:
            return middle
    raise ValueError('Value is not in the list')

data= [1, 3, 5, 7, 9, 11, 13, 15, 16, 17, 19, 32, 64, 128, 256, 512]
```
## Recursive Code in Python:
Compare x with the middle element.
* If x matches with middle element, we return the mid index.
* Else If x is greater than the mid element, then x can only lie in right half subarray after the mid element. So we recur for right half.
* Else (x is smaller) recur for the left half.
```python
# Returns index of x in arr if present, else -1 
def binarySearch (arr, l, r, x): 
    # Check base case 
    if r >= l:  
        mid = (l + r)//2
        # If element is present at the middle itself 
        if arr[mid] == x: 
            return mid 
          
        # If element is smaller than mid, then it can only 
        # be present in left subarray 
        elif x < arr[mid]: 
            return binarySearch(arr, l, mid-1, x) 
        # Else the element can only be present in right subarray 
        else: 
            return binarySearch(arr, mid+1, r, x) 
  
    else: 
        # Element is not present in the array 
        return "Not Found"
data= [1, 3, 5, 7, 9, 11, 13, 15, 16, 17, 19, 32, 64, 128, 256, 512]
l= 0
r= len(data)-1
x= 256
binarySearch(data, l, r, x)
```




