# Input
- Programming Concept: String; Integer; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Catch Quota in Fishing

Write a function named `catch_quota(fish_type, weight)` that checks whether a caught fish meets the minimum requirements. The function should take two parameters: `fish_type` (String) and `weight` (Integer).

The minimum requirements are as follows:
- For 'Pike', the weight must be at least 5 kg.
- For 'Zander', the weight must be at least 3 kg.
- For 'Perch', the weight must be at least 1 kg.

The function should return `True` if the fish meets the minimum requirements, and `False` if it does not.

Example calls:
- `catch_quota('Pike', 6)` returns `True`.
- `catch_quota('Zander', 2)` returns `False`.

## Code Framework
```python
def catch_quota(fish_type, weight):
    ## Insert code here
```

## Model Solution
```python
def catch_quota(fish_type, weight):
    minimum_weight = {'Pike': 5, 'Zander': 3, 'Perch': 1}
    return weight >= minimum_weight.get(fish_type, float('inf'))

# Example calls
print(catch_quota('Pike', 6))  # True
print(catch_quota('Zander', 2))  # False
```

## Unit Tests
```python
import unittest
from main import catch_quota

class TestCatchQuota(unittest.TestCase):
    def test_pike_above_minimum(self):
        self.assertTrue(catch_quota('Pike', 6))

    def test_pike_below_minimum(self):
        self.assertFalse(catch_quota('Pike', 4))

    def test_zander_above_minimum(self):
        self.assertTrue(catch_quota('Zander', 4))

    def test_zander_below_minimum(self):
        self.assertFalse(catch_quota('Zander', 2))

    def test_perch_above_minimum(self):
        self.assertTrue(catch_quota('Perch', 2))

    def test_perch_below_minimum(self):
        self.assertFalse(catch_quota('Perch', 0.5))

    def test_unknown_fish_type(self):
        self.assertFalse(catch_quota('Carp', 10))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 583
