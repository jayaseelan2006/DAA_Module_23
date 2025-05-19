# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. Take an array arr where each element represents the maximum number of steps you can jump forward.
2. Initialize a dp array, where dp[i] will store the minimum jumps to reach index i.
3. Set dp[0] = 0 (no jumps needed to stay at the start) and other values to infinity.
4. Iterate through the array, and for each index, update the dp values of the reachable positions.
5. The result is stored in dp[n-1], which is the minimum number of jumps to reach the end.
## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: Jayaseelan U
Register Number:  212223220039
*/
```
```
def minJumps(arr, n):
    dp=[0]*n
    for i in range(1,n):
        dp[i]=n
        for j in range(i):
             if i <= j + arr[j] and dp[j] != n:
                dp[i] = min(dp[i], dp[j] + 1)
                break
    return dp[n - 1] if dp[n - 1] != n else -1
arr = []
n = int(input())
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
```
## Output:
![Screenshot 2025-05-07 111214](https://github.com/user-attachments/assets/d4eee434-9c05-4b79-a166-4c87f42b234e)
## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
