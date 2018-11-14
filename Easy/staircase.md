# Staircase

[Easy Problem](https://www.hackerrank.com/challenges/staircase/problem?h_r=next-challenge&h_v=zen)

## Solution

### Python

```python
def staircase(n):
    for i in range(1, n + 1):
        print(" " * (n - i) + "#" * i)
```
