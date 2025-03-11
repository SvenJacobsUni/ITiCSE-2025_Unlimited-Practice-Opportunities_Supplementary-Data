# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Logical Operators in Fishing

Write a function named `catch_fish(weight, length)` that checks if a caught fish meets the minimum requirements to be kept. A fish can only be kept if it weighs at least 2 kg and is at least 30 cm long. The function should return `True` if the fish can be kept, and `False` otherwise.

Example Calls:
- `catch_fish(2.5, 35)` returns `True`.
- `catch_fish(1.8, 32)` returns `False`.
- `catch_fish(2.0, 29)` returns `False`.

## Code Framework
```python
def catch_fish(weight, length):
    ## Insert code here

```

## Model Solution
```python
def catch_fish(weight, length):
    return weight >= 2 and length >= 30

# Example Calls
print(catch_fish(2.5, 35))  # True
print(catch_fish(1.8, 32))  # False
print(catch_fish(2.0, 29))  # False

```

## Unit Tests
```python
import unittest
from main import catch_fish

class TestCatchFish(unittest.TestCase):
    def test_keep_fish(self):
        self.assertTrue(catch_fish(2.5, 35))

    def test_fish_too_light(self):
        self.assertFalse(catch_fish(1.8, 32))

    def test_fish_too_short(self):
        self.assertFalse(catch_fish(2.0, 29))

    def test_fish_exact_boundary(self):
        self.assertTrue(catch_fish(2.0, 30))

    def test_fish_below_boundary(self):
        self.assertFalse(catch_fish(1.9, 29))

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 488
