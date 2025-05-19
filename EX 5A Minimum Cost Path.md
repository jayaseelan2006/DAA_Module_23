# EX 5A Minimum Cost Path
## DATE:
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.




## Algorithm
1. Take a grid where each cell has a cost.
2. Define a recursive function to find the minimum cost path from the top-left to the bottom-right corner.
3. If at the destination, return the cost of that cell.
4. If in the last row, only move right; if in the last column, only move down.
5. For other cells, recursively calculate the cost for moving right and down, then return the minimum of the two.
## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: jayaseelan U
Register Number:  212223220039
*/
```
```
row,col=int(input()),int(input())
def mc(c,n,m):
    dp=[[0]*(m+1) for i in range(n+1)]
    dp[0][0]=c[0][0]
    for i in range(1,n+1):
        dp[i][0]=dp[i-1][0]+c[i][0]
    for j in range(1,m+1):
        dp[0][j]=dp[0][j-1]+c[0][j]
    for i in range(1,n+1):
        for j in range(1,m+1):
            dp[i][j]=c[i][j]+min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1])
    return dp[n][m]
c=[[4,0,0],
   [0,8,0],
   [0,0,4]]
print(mc(c,row-1,col-1))
```
## Output:
![Screenshot 2025-05-07 105849](https://github.com/user-attachments/assets/3d215b37-7eb8-48fd-b549-c9c6b57b912e)
## Result:
Thus the above program was executed successfully for finding the minimum cost.
