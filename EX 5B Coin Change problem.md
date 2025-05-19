# EX 5B Coin Change Problem
## DATE:
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1. Given a list of coin denominations and an amount N.
2. If N == 0, return 0 (no coins needed).
3. If N < 0, return infinity (not possible to make this amount).
4. Recursively subtract each coin from N and find the fewest coins for the remaining amount.
5. Return the minimum number of coins across all possibilities.
## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: jayaseelan U
Register Number:  212223220039
*/
```
```
class Solution(object):
    def coinChange(self, coins, amount):
        dp=[float('inf')]*(amount+1)
        dp[0]=0
        for c in coins:
            for i in range(c,amount+1):
              dp[i]=min(dp[i],dp[i-c]+1)
        if dp[amount]!=float('inf'):
          return dp[amount]
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```
## Output:
![Screenshot 2025-05-07 110304](https://github.com/user-attachments/assets/f8f55c58-123b-47df-a89e-0e7d9a60563d)
## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
