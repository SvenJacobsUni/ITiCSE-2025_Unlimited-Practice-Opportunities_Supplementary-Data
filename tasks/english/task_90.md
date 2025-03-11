# Input
- Programming Concept: For loops
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Count Fish

Write a function named `count_fish(fish_list)` that takes a list of fish as input and counts the number of fish in the list. The function should return the number of fish using `return`.

Example call:
```python
fish = ["Pike", "Carp", "Trout", "Pike", "Perch"]
number = count_fish(fish)
print(number)  # Output: 5
```

Use a for loop to determine the number of fish in the list.

## Code Framework
```python
def count_fish(fish_list):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_list):
    return len(fish_list)

fish = ["Pike", "Carp", "Trout", "Pike", "Perch"]
number = count_fish(fish)
print(number)  # Output: 5
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
        self.assertEqual(count_fish(["Pike", "Carp", "Trout", "Pike", "Perch"]), 5)

    def test_all_same_fish(self):
        self.assertEqual(count_fish(["Pike", "Pike", "Pike"]), 3)

    def test_different_fish(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Trout", "Perch", "Zander"]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 508
