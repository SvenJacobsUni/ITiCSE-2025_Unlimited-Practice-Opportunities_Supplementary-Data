# Input
- Programming Concept: Boolean and None; Logical operators (==, !=, <, >, <=, >=, or, and, not); Float
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Check Relationship Status

Write a function named `relationship_status(age, relationship_duration, shared_interests)` that checks the relationship status based on the person's age, the duration of the relationship (in years), and the number of shared interests. The function should apply the following rules:

1. If the person's age is under 18, the function should return `None`.
2. If the relationship duration is less than 1 year and the number of shared interests is less than 3, the function should return `False`.
3. If the relationship duration is 1 year or more and the number of shared interests is 3 or more, the function should return `True`.
4. In all other cases, the function should return `False`.

Example calls:
- `relationship_status(17, 2, 5)` returns `None`.
- `relationship_status(25, 0.5, 2)` returns `False`.
- `relationship_status(30, 2, 4)` returns `True`.
- `relationship_status(22, 1, 2)` returns `False`.

## Code Framework
```python
def relationship_status(age, relationship_duration, shared_interests):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(age, relationship_duration, shared_interests):
    if age < 18:
        return None
    if relationship_duration >= 1 and shared_interests >= 3:
        return True
    return False

print(relationship_status(17, 2, 5))  # None
print(relationship_status(25, 0.5, 2))  # False
print(relationship_status(30, 2, 4))  # True
print(relationship_status(22, 1, 2))  # False
```

## Unit Tests
```python
import unittest

from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_under_18(self):
        self.assertIsNone(relationship_status(17, 2, 5))

    def test_short_relationship_few_interests(self):
        self.assertFalse(relationship_status(25, 0.5, 2))

    def test_long_relationship_many_interests(self):
        self.assertTrue(relationship_status(30, 2, 4))

    def test_long_relationship_few_interests(self):
        self.assertFalse(relationship_status(22, 1, 2))

    def test_short_relationship_many_interests(self):
        self.assertFalse(relationship_status(25, 0.5, 3))

    def test_edge_case_18_years(self):
        self.assertFalse(relationship_status(18, 0.5, 2))

    def test_edge_case_1_year(self):
        self.assertTrue(relationship_status(25, 1, 3))

    def test_edge_case_3_interests(self):
        self.assertTrue(relationship_status(25, 1, 3))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 597
