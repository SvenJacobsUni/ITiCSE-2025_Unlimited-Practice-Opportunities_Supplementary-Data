# Input
- Programming Concept: Boolean and None;Operations with numbers;If-Else statements
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Check Relationship Status

Write a function named `relationship_status(age, relationship_duration)` that verifies a person's relationship status based on their age and the duration of their current relationship. The function should return an appropriate message with `return`.

- If the person is younger than 18 years, the function should return "Too young for a serious relationship."
- If the person is 18 years or older and the relationship duration is less than 1 year, the function should return "Newly in love!"
- If the person is 18 years or older and the relationship duration is between 1 and 5 years, the function should return "In a stable relationship."
- If the person is 18 years or older and the relationship duration exceeds 5 years, the function should return "Long-term relationship."

Example calls:
- `relationship_status(16, 0.5)` returns "Too young for a serious relationship."
- `relationship_status(25, 0.8)` returns "Newly in love!"
- `relationship_status(30, 3)` returns "In a stable relationship."
- `relationship_status(40, 6)` returns "Long-term relationship."

## Code Framework
```python
def relationship_status(age, relationship_duration):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(age, relationship_duration):
    if age < 18:
        return "Too young for a serious relationship."
    elif relationship_duration < 1:
        return "Newly in love!"
    elif relationship_duration <= 5:
        return "In a stable relationship."
    else:
        return "Long-term relationship."

# Example calls
print(relationship_status(16, 0.5))
print(relationship_status(25, 0.8))
print(relationship_status(30, 3))
print(relationship_status(40, 6))
```

## Unit Tests
```python
import unittest
from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_too_young(self):
        self.assertEqual(relationship_status(16, 0.5), "Too young for a serious relationship.")

    def test_newly_in_love(self):
        self.assertEqual(relationship_status(25, 0.8), "Newly in love!")

    def test_stable_relationship(self):
        self.assertEqual(relationship_status(30, 3), "In a stable relationship.")

    def test_long_term_relationship(self):
        self.assertEqual(relationship_status(40, 6), "Long-term relationship.")

    def test_boundary_18_years(self):
        self.assertEqual(relationship_status(18, 0.5), "Newly in love!")

    def test_boundary_1_year(self):
        self.assertEqual(relationship_status(25, 1), "In a stable relationship.")

    def test_boundary_5_years(self):
        self.assertEqual(relationship_status(30, 5), "In a stable relationship.")

    def test_exceeds_5_years(self):
        self.assertEqual(relationship_status(30, 5.1), "Long-term relationship.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 587
