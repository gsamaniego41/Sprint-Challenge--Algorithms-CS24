#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

```python
a)  a = 0 # O(1)
    while (a < n * n * n): # O(n)
      a = a + n * n # O(1)

'''
Runtime: O(n)
At first glance, it looks like O(n^3) but `(a < n * n * n)` does not exponentially increase the number of times it loops. It's simply a checker.
''''
```

```python
b)  sum = 0               #  O(1)
    for i in range(n):    #  O(n)
      j = 1               #  O(1)
      while j < n:        #  O(log(n))
        j *= 2            #  O(1)
        sum += 1          #  O(1)

10  10  10
0   2   4

'''
Runtime: O(n log(n))
Both outer loop and inner loop grow as n grows. However, the while loop runs half the time as the for loop because it doubles the size of j.
''''
```

```python
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)

# bunnies   5   6   7
# recurse   6   7   8
'''
Runtime: O(n)
This function is essentially a for loop. Therefore, it's O(n).
''''
```

## Exercise II

```python
'''
Problem Breakdown:
- n-story building
- list of eggs
- flor f or higher = egg breaks
- less than floor f = egg doesn't break
'''

'''
Pseudocode:
find the mid floor = num of floors // 2
split floors into f1 and f2
throw egg one floor below mid floor
    if it breaks, eliminate f1
    find mid floor of f2, splitting it in half
repeat the process until we find the correct floor
'''
```
