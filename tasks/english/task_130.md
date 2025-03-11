# Input
- Programming Concept: If-Else statements; String
- Context: Amusement Park

# Generated Task Components
## Task Description
### Exercise: Admission Control in the Amusement Park

Write a function named `admission_allowed(age, height)` that checks if a person is allowed into a specific attraction in the amusement park. The function should take two parameters: `age` (an integer) and `height` (a float, representing the height in meters).

The conditions for admission are:
- The person must be at least 12 years old.
- The person must be at least 1.40 meters tall.

The function should return `True` if both conditions are met, and `False` if one or both conditions are not met.

Example calls:
- `admission_allowed(14, 1.50)` returns `True`.
- `admission_allowed(10, 1.50)` returns `False`.
- `admission_allowed(14, 1.35)` returns `False`.

## Code Framework
```python
def admission_allowed(age, height):
    ## Insert code here
```

## Model Solution
```python
def admission_allowed(age, height):
    return age >= 12 and height >= 1.4

print(admission_allowed(14, 1.50))  # True
print(admission_allowed(10, 1.50))  # False
print(admission_allowed(14, 1.35))  # False
```

## Unit Tests
```python
import unittest
from main import admission_allowed

class TestAdmissionAllowed(unittest.TestCase):
    def test_allowed(self):
        self.assertTrue(admission_allowed(14, 1.50))

    def test_too_young(self):
        self.assertFalse(admission_allowed(10, 1.50))

    def test_too_short(self):
        self.assertFalse(admission_allowed(14, 1.35))

    def test_age_boundary(self):
        self.assertTrue(admission_allowed(12, 1.50))

    def test_height_boundary(self):
        self.assertTrue(admission_allowed(14, 1.40))

    def test_both_boundaries(self):
        self.assertTrue(admission_allowed(12, 1.40))

    def test_under_boundary_age(self):
        self.assertFalse(admission_allowed(11, 1.40))

    def test_under_boundary_height(self):
        self.assertFalse(admission_allowed(12, 1.39))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 562
