# Input
- Programming Concept: Recursion
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Recursive Fish Counting

Write a recursive function named `count_fish(pond)`, that counts the number of fish in a pond. The pond is represented as a list of lists, where each inner list is either empty or contains more lists. An empty pond (empty list) contains no fish.

Example calls:

```python
# A pond with no fish
pond1 = []

# A pond with one fish
pond2 = [[], []]

# A pond with three fish
pond3 = [[], [[], []], [[], [[], []]]]

print(count_fish(pond1))  # Output: 0
print(count_fish(pond2))  # Output: 2
print(count_fish(pond3))  # Output: 6
```

Implement the function `count_fish(pond)` that recursively counts and returns the number of fish in the pond.

## Code Framework
```python
def count_fish(pond):
    ## Insert code here
```

## Model Solution
```python
def count_fish(pond):
    return 1 + sum(count_fish(p) for p in pond) if pond else 0

# Example calls
pond1 = []
pond2 = [[], []]
pond3 = [[], [[], []], [[], [[], []]]]

print(count_fish(pond1))  # Output: 0
print(count_fish(pond2))  # Output: 2
print(count_fish(pond3))  # Output: 6
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_empty_pond(self):
        self.assertEqual(count_fish([]), 0)

    def test_one_fish(self):
        self.assertEqual(count_fish([[], []]), 2)

    def test_multiple_fish(self):
        self.assertEqual(count_fish([[], [[], []], [[], [[], []]]]), 6)

    def test_nested_pond(self):
        self.assertEqual(count_fish([[], [[], [[], []]], [[], []]]), 5)

    def test_deeply_nested_pond(self):
        self.assertEqual(count_fish([[], [[], [[], [[], []]]], [[], []]]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 505
