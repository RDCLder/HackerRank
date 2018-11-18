# Nested Lists

[Easy Problem](https://www.hackerrank.com/challenges/nested-list/problem)

- Given a list of N students and a list of their corresponding scores, print the name(s) of the student(s) with the second lowest score.

- Conditions:
  - First input is an integer N
  - 2 < N < 5

- Example
  
  - Input:
    ```
    5
    Harry
    37.21
    Berry
    37.21
    Tina
    37.2
    Akriti
    41
    Harsh
    39
    ```

  - Output:
    ```
    Berry
    Harry
    ```

## Solution

- Generating the data set with a list comprehension
  - The starting code was commented out so we could use a more efficient list comprehension to generate the data.
  - A list comprehension with nested lists allows us to only use a single for loop to index and compile the names based on their corresponding results.
 
- Finding the second lowest score
  - The score can be indexed by using the set function to remove all non-unique scores.  The set will need to be converted to iterable form with a list function.
  - The remaining scores can then be ordered from least to greatest with the sorted function.

 
### Python
```python
results = [[input(), float(input())] for i in range(int(input()))]
secondLowest = sorted(list(set([score for name, score in results])))[1]
names = []

for r in results:
    if r[1] == secondLowest:
        names.append(r[0])

for n in sorted(names):
    print(n)
```
