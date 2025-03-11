# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Fishing

# Generated Task Components
## Task Description
### Practice Task: Control Structures in Fishing

Write a function named `catch_fish(weight, length)` that checks whether a caught fish meets the minimum requirements for keeping. The minimum requirements are:

- The fish's weight must be at least 1.5 kilograms.
- The fish's length must be at least 30 centimeters.

The function should return `True` if both conditions are fulfilled and `False` if one or both conditions are not fulfilled.

Example calls:
- `catch_fish(2.0, 35)` returns `True`.
- `catch_fish(1.0, 40)` returns `False`.
- `catch_fish(1.5, 25)` returns `False`.

## Code Framework
```python
def catch_fish(weight, length):
    ## Insert code here
```

## Model Solution
```python
def catch_fish(weight, length):
    return weight >= 1.5 and length >= 30

# Example calls
print(catch_fish(2.0, 35))  # True
print(catch_fish(1.0, 40))  # False
print(catch_fish(1.5, 25))  # False
```

## Unit Tests
```python
import unittest
from main import catch_fish

class TestCatchFish(unittest.TestCase):
    def test_both_conditions_met(self):
        self.assertTrue(catch_fish(2.0, 35))

    def test_weight_below_minimum(self):
        self.assertFalse(catch_fish(1.0, 40))

    def test_length_below_minimum(self):
        self.assertFalse(catch_fish(1.5, 25))

    def test_both_conditions_not_met(self):
        self.assertFalse(catch_fish(1.0, 20))

    def test_threshold_weight(self):
        self.assertTrue(catch_fish(1.5, 30))

    def test_threshold_length(self):
        self.assertTrue(catch_fish(2.0, 30))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 445
