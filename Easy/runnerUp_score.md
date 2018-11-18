# Find the Runner-Up Score!

[Easy Problem](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem)

- Given an array, print the runner-up score.
- Example
  - ```
    Input: [2, 3, 6, 6, 5]
    Output: 5
    ```

## Solution

- The input is a map type that contains all the integers.
  - We must convert the map to a list to make it iterable and compatible with list methods.
  
- Repeats of the first place score do not count.
  - I set a variable equal to the max number and removed all occurrences until the count is zero using the count and remove methods.
  - After that, the runner-up would be the max of the remaining integer in the list.

### Python

```python
arr = list(arr)
first = max(arr)

while arr.count(first) > 0:
    arr.remove(max(arr))

print(max(arr))
```
