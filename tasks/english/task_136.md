# Input
- Programming Concept: String; Integer
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Relationship Status

Write a function named `relationship_status(name, years)` that outputs a person's relationship status based on the number of years in the relationship. The function should accept two parameters: `name` (a String) and `years` (an Integer).

The function should return the following messages:
- If `years` is less than 1: "`[Name] is newly in love!`"
- If `years` is between 1 and 5: "`[Name] is in a stable relationship.`"
- If `years` is more than 5: "`[Name] is in a long-term relationship.`"

Example call:
```python
print(relationship_status("Anna", 3))  # Output: "Anna is in a stable relationship."
```

## Code Framework
```python
def relationship_status(name, years):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(name, years):
    if years < 1:
        return f"{name} is newly in love!"
    elif 1 <= years <= 5:
        return f"{name} is in a stable relationship."
    else:
        return f"{name} is in a long-term relationship."

print(relationship_status("Anna", 3))  # Example call
```

## Unit Tests
```python
import unittest

from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_newly_in_love(self):
        self.assertEqual(relationship_status("Anna", 0), "Anna is newly in love!")
        self.assertEqual(relationship_status("Max", -1), "Max is newly in love!")

    def test_stable_relationship(self):
        self.assertEqual(relationship_status("Anna", 1), "Anna is in a stable relationship.")
        self.assertEqual(relationship_status("Max", 5), "Max is in a stable relationship.")
        self.assertEqual(relationship_status("Chris", 3), "Chris is in a stable relationship.")

    def test_long_term_relationship(self):
        self.assertEqual(relationship_status("Anna", 6), "Anna is in a long-term relationship.")
        self.assertEqual(relationship_status("Max", 10), "Max is in a long-term relationship.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 568
