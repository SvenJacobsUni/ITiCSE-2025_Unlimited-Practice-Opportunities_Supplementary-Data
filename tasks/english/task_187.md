# Input
- Programming Concept: Recursion;Higher-order functions;Operations with numbers
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Counting Fish

You are an enthusiastic angler and wish to write a function that helps you count the number of fish in a lake. The function should work recursively and use higher-order functions.

Write a function `count_fish(lake)` that counts the number of fish in a lake. The lake is represented as a list of lists, where each inner list represents a group of fish. Each fish is represented by a number indicating its weight in grams.

The function `count_fish(lake)` should return the total number of fish in the lake.

Example:

```python
lake = [
    [200, 150, 300],  # Group 1
    [100, 250],       # Group 2
    [400, 500, 100]   # Group 3
]

print(count_fish(lake))  # Output: 8
```

In this example, there are a total of 8 fish in the lake.

## Code Framework
```python
def count_fish(lake):
    ## Insert code here

```

## Model Solution
```python
def count_fish(lake):
    return sum(map(len, lake))

lake = [
    [200, 150, 300],
    [100, 250],
    [400, 500, 100]
]

print(count_fish(lake))
```

## Unit Tests
```python
import unittest

from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_simple_lake(self):
        self.assertEqual(count_fish([[200, 150, 300], [100, 250], [400, 500, 100]]), 8)

    def test_empty_lake(self):
        self.assertEqual(count_fish([]), 0)

    def test_lake_with_one_group(self):
        self.assertEqual(count_fish([[200, 150, 300]]), 3)

    def test_lake_with_empty_group(self):
        self.assertEqual(count_fish([[200, 150, 300], [], [400, 500, 100]]), 6)

    def test_lake_with_many_groups(self):
        self.assertEqual(count_fish([[200], [150], [300], [100], [250], [400], [500], [100]]), 8)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 619
