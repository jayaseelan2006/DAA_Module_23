# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm
1. Take a list of numbers as input.
2. Initialize two variables: max_sum and current_sum, both starting with the first element.
3. Iterate through the list, update current_sum by adding the current element, and reset current_sum to 0 if it becomes negative.
4. Update max_sum with the maximum of max_sum and current_sum.
5. After the loop, return max_sum, which is the maximum sum of the contiguous subarray.
## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: Jayaseelan U
Register Number:  212223220039
*/
```
```
def maxSubArraySum(a,size):
    max_so_far = a[0]
    max_ending_here = 0
    for i in range(0, size):
        max_ending_here = max(a[i], max_ending_here + a[i])
        max_so_far = max(max_so_far, max_ending_here)
    return max_so_far
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:
![Screenshot 2025-05-07 110527](https://github.com/user-attachments/assets/e9f3be06-1c9e-46d5-9c3e-964ec991df77)
## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
