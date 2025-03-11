# Input
- Programming Concept: For Loops
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Relationships and For Loops

Write a function named `relationship_status(names_list)` that takes a list of names as its argument. The function should output a message for each name in the list describing the relationship status of the person. Use a for loop to iterate through the list and generate the messages.

Example call:
```python
relationship_status(["Anna", "Ben", "Clara"])
```

Example output:
```
Anna is single.
Ben is in a relationship.
Clara is married.
```

Note: The messages can be the same for each name; the goal is to practice using the for loop.

## Code Framework
```python
def relationship_status(names_list):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(names_list):
    for name in names_list:
        print(f"{name} is single.")

relationship_status(["Anna", "Ben", "Clara"])
```

## Unit Tests
```python
import unittest
from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(relationship_status([]), [])

    def test_single_name(self):
        self.assertEqual(relationship_status(["Anna"]), ["Anna is single."])

    def test_multiple_names(self):
        self.assertEqual(relationship_status(["Anna", "Ben", "Clara"]), ["Anna is single.", "Ben is single.", "Clara is single."])

    def test_names_with_spaces(self):
        self.assertEqual(relationship_status([" Anna ", " Ben ", " Clara "]), [" Anna  is single.", " Ben  is single.", " Clara  is single."])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 421
