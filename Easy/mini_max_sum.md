# Mini-Max Sum

[Easy Problem](https://www.hackerrank.com/challenges/mini-max-sum/problem)

## Solution

### Python

Note:  Because HackerRank does not support f-strings, the ```.format()``` method was used.

```python
def miniMaxSum(arr):
    allSums = []
    for n in arr:
        sum = 0
        for i in range(len(arr)):
            sum += arr[i]
        allSums.append(sum - n)
    print("{} {}".format(min(allSums), max(allSums)))
```
