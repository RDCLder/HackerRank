# Time Conversion

[Easy Problem](https://www.hackerrank.com/challenges/time-conversion/problem)

## Solution

### Python

It's necessary to account for 12:xx PM/AM.  In all cases, the last two characters which designate 'AM' or 'PM' are omitted.

```python
def timeConversion(s):
    newString = ''
    if s[-2] == 'P':
        if s[0] + s[1] == '12':
            newString += s[:len(s) - 2]
        else:
            newString += str(int(s[0]) + 1)
            newString += str(int(s[1]) + 2)
            newString += s[2:len(s) - 2]
    elif s[-2] == 'A':
        if s[0] + s[1] == '12':
            newString += '00'
            newString += s[2:len(s) - 2]
        else:
            newString += s[:len(s) - 2]

    return newString
```
