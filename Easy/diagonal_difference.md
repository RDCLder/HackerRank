# Diagonal Difference

[Easy Problem](https://www.hackerrank.com/challenges/diagonal-difference/problem)

## Solution

### Python

```python
def diagonalDifference(arr):
    
    left = 0
    right = 0
    
    for i in range(len(arr)):
        left += arr[i][i]
        right += arr[i][len(arr) - i - 1]
    return abs(left - right)
```  
