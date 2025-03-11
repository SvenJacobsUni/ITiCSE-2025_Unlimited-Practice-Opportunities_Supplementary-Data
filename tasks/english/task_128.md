# Input
- Programming Concept: Boolean and None; For loops
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Counting Fish

Write a function named `count_fish(fish_list)`, which takes a list of fish as input. Each entry in the list is either the name of a fish (as a string) or `None`, if no fish was caught. The function should count and return the number of fish caught. 

Example call:
```python
fish_list = ["Pike", None, "Carp", "Trout", None, "Perch"]
print(count_fish(fish_list))  # Output: 4
```

### Requirements:
- The function should accept a list of fish as an argument.
- The function should count and return the number of fish caught (non-`None` entries).
- Use a `for` loop to iterate through the list.
- Use Boolean values to check if an entry is `None` or not.

## Code Framework
```python
def count_fish(fish_list):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_list):
    return sum(1 for fish in fish_list if fish)

fish_list = ["Pike", None, "Carp", "Trout", None, "Perch"]
print(count_fish(fish_list))  # Output: 4
```

## Unit Tests
```python
import unittest

from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(count_fish(["Pike", None, "Carp", "Trout", None, "Perch"]), 4)

    def test_empty_list(self):
        self.assertEqual(count_fish([]), 0)

    def test_all_none(self):
        self.assertEqual(count_fish([None, None, None]), 0)

    def test_all_fish(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Trout", "Perch"]), 4)

    def test_mixed_list(self):
        self.assertEqual(count_fish([None, "Pike", None, "Carp", "Trout", None, "Perch", None]), 4)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 560
