# Write a Function

[Medium Problem](https://www.hackerrank.com/challenges/write-a-function/problem)

Write a function that checks if a given year is a leap year.  It is a leap year if it meets the 3 following criteria:

- It is divisible by 4 UNLESS
  - It is also divisible by 100 UNLESS
    - It is also divisible by 400

## Solution

### Python

```python
def is_leap(year):
    leap = False
    
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                return True
        else:
            return True
    
    return leap
```
