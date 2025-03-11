# Input
- Programming Concept: While loops
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise Task: Aquarium - Count Fish

Write a function named `count_fish(fish_list)` that takes a list of fish as an argument. The function should use a while loop to count the number of fish in the list and return this number.

Example call:
```python
fish_list = ["Goldfish", "Guppy", "Neon Tetra", "Platy"]
print(count_fish(fish_list))  # Output: 4
```

Implement the function `count_fish(fish_list)` that counts and returns the number of fish in the list.

## Code Framework
```python
def count_fish(fish_list):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_list):
    count = 0
    i = 0
    while i < len(fish_list):
        count += 1
        i += 1
    return count

fish_list = ["Goldfish", "Guppy", "Neon Tetra", "Platy"]
print(count_fish(fish_list))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_fish([]), 0)

    def test_single_fish(self):
        self.assertEqual(count_fish(["Goldfish"]), 1)

    def test_multiple_fish(self):
        self.assertEqual(count_fish(["Goldfish", "Guppy", "Neon Tetra", "Platy"]), 4)

    def test_same_fish(self):
        self.assertEqual(count_fish(["Guppy", "Guppy", "Guppy"]), 3)

    def test_mixed_fish(self):
        self.assertEqual(count_fish(["Goldfish", "Guppy", "Guppy", "Neon Tetra", "Platy", "Platy"]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 509
