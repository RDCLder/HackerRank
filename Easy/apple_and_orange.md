# Apple and Orange

[Easy Problem](https://www.hackerrank.com/challenges/apple-and-orange/problem)

## Solution

### Python

```python
def countApplesAndOranges(s, t, a, b, apples, oranges):
    
    appleTotal = 0
    orangeTotal = 0
    
    for i in apples:
        if s <= a + i <= t:
            appleTotal += 1
    
    for j in oranges:
        if s <= b + j <= t:
            orangeTotal += 1
    
    print(appleTotal)
    print(orangeTotal)
```
