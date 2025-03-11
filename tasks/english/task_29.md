# Input
- Programming Concept: Recursion
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise Task: Recursive Fish Counting

Write a recursive function named `count_fish(lake)` that counts the number of fish in a lake. The lake is represented as a nested list, where each list either contains a number (the number of fish in that part of the lake) or another list (a deeper part of the lake).

Example:
```python
lake = [2, [3, [1, 4], 5], [6, 7], 8]
```

In this example, the lake contains a total of 36 fish.

Implement the function `count_fish(lake)` that returns the total count of fish in the lake.

Example call:
```python
print(count_fish(lake))  # Output: 36
```

## Code Framework
```python
def count_fish(lake):
    ## Insert code here
```

## Model Solution
```python
def count_fish(lake):
    if isinstance(lake, int):
        return lake
    return sum(count_fish(part) for part in lake)

lake = [2, [3, [1, 4], 5], [6, 7], 8]
print(count_fish(lake))  # Output: 36
```

## Unit Tests
```python
import unittest

from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_simple_lake(self):
        self.assertEqual(count_fish([1, 2, 3]), 6)

    def test_empty_lake(self):
        self.assertEqual(count_fish([]), 0)

    def test_one_fish(self):
        self.assertEqual(count_fish([1]), 1)

    def test_nested_lake(self):
        self.assertEqual(count_fish([1, [2, [3, 4]], 5]), 15)

    def test_deeply_nested_lake(self):
        self.assertEqual(count_fish([1, [2, [3, [4, [5]]]]]), 15)

    def test_mixed_lake(self):
        self.assertEqual(count_fish([2, [3, [1, 4], 5], [6, 7], 8]), 36)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 447
