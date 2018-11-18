# Designer Door Mat

[Easy Problem](https://www.hackerrank.com/challenges/designer-door-mat/problem)

- Recreate the following design for any input with certain conditions:

  ```
  Size: 7 x 21 
  
  ---------.|.---------
  ------.|..|..|.------
  ---.|..|..|..|..|.---
  -------WELCOME-------
  ---.|..|..|..|..|.---
  ------.|..|..|.------
  ---------.|.---------
  ```

- Conditions:
  - The inputs N x M are always odd.
  - 5 < N < 101
  - 15 < M < 303
  - The second input is 3x the first input.

- Example
  - ```
    Size: 9 x 27
    
    ------------.|.------------
    ---------.|..|..|.---------
    ------.|..|..|..|..|.------
    ---.|..|..|..|..|..|..|.---
    ----------WELCOME----------
    ---.|..|..|..|..|..|..|.---
    ------.|..|..|..|..|.------
    ---------.|..|..|.---------
    ------------.|.------------
    ```

## Solution

- The design has horizontal symmetry therefore the code that prints the top half can be reversed
  - We must still adjust for where to start/stop counting.  In this case, the start/stop shifts down one.
  - This is due to the fact that python formats counting as ```start:up to but not including:step```.

- Since every input is odd, we must account for this by adjusting the change in each iteration.
  - We could change the step size to 2 ```for i in range(start, stop, 2)```
  - We could utilize the fact that ```N // 2``` will return 1, 2, 3, etc. since the ```//``` operator rounds down.  (Chosen method).

### Python

```python
N, M = map(int, input().split())

for i in range(N // 2):
    print("---" * (N // 2 - i) + ".|." * (2 * i + 1) + "---" * (N // 2 - i))

print("-" * (3 * (N // 2) - 2) + "WELCOME" + "-" * (3 * (N // 2) - 2))

for i in range(N // 2 - 1, -1, -1):
    print("---" * (N // 2 - i) + ".|." * (2 * i + 1) + "---" * (N // 2 - i))
```
