# Input
- Programming Concept: Recursion;If-Else statements
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Recursive Fish Counting

Write a recursive function named `count_fish(fish_list)` that counts the number of fish in a lake. The function should take a list of fish as an argument, where each fish is represented by a string. If the list is empty, the function should return 0. Otherwise, the function should return the number of fish in the list.

Example calls:
- `count_fish([])` returns `0`.
- `count_fish(["Pike", "Carp", "Trout"])` returns `3`.

## Code Framework
```python
def count_fish(fish_list):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_list):
    if not fish_list:
        return 0
    return 1 + count_fish(fish_list[1:])

print(count_fish([]))
print(count_fish(["Pike", "Carp", "Trout"]))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_fish([]), 0)

    def test_one_fish(self):
        self.assertEqual(count_fish(["Pike"]), 1)

    def test_multiple_fish(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Trout"]), 3)

    def test_many_fish(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Trout", "Perch", "Catfish", "Zander"]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 533
