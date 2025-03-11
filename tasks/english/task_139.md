# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not); While loops
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Check Relationship Status

Write a function named `relationship_status(examinations)` that takes a list of examinations (as tuples). Each tuple contains two elements: the name of a person and their relationship status (as a string). The function should count the number of people in each of the following categories: "Single", "In a relationship", "Married", and "It's complicated". The function should return a dictionary that contains the number of people in each category.

Example call:
```python
examinations = [("Anna", "Single"), ("Ben", "In a relationship"), ("Clara", "Married"), ("David", "It's complicated"), ("Eva", "Single")]
print(relationship_status(examinations))
```

Expected output:
```python
{
    "Single": 2,
    "In a relationship": 1,
    "Married": 1,
    "It's complicated": 1
}
```

## Code Framework
```python
def relationship_status(examinations):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(examinations):
    status_dict = {"Single": 0, "In a relationship": 0, "Married": 0, "It's complicated": 0}
    for _, status in examinations:
        if status in status_dict:
            status_dict[status] += 1
    return status_dict

examinations = [("Anna", "Single"), ("Ben", "In a relationship"), ("Clara", "Married"), ("David", "It's complicated"), ("Eva", "Single")]
print(relationship_status(examinations))
```

## Unit Tests
```python
import unittest
from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_all_categories(self):
        examinations = [("Anna", "Single"), ("Ben", "In a relationship"), ("Clara", "Married"), ("David", "It's complicated"), ("Eva", "Single")]
        expected = {"Single": 2, "In a relationship": 1, "Married": 1, "It's complicated": 1}
        self.assertEqual(relationship_status(examinations), expected)

    def test_only_single(self):
        examinations = [("Anna", "Single"), ("Ben", "Single"), ("Clara", "Single")]
        expected = {"Single": 3, "In a relationship": 0, "Married": 0, "It's complicated": 0}
        self.assertEqual(relationship_status(examinations), expected)

    def test_empty_list(self):
        examinations = []
        expected = {"Single": 0, "In a relationship": 0, "Married": 0, "It's complicated": 0}
        self.assertEqual(relationship_status(examinations), expected)

    def test_all_married(self):
        examinations = [("Anna", "Married"), ("Ben", "Married"), ("Clara", "Married")]
        expected = {"Single": 0, "In a relationship": 0, "Married": 3, "It's complicated": 0}
        self.assertEqual(relationship_status(examinations), expected)

    def test_all_complicated(self):
        examinations = [("Anna", "It's complicated"), ("Ben", "It's complicated"), ("Clara", "It's complicated")]
        expected = {"Single": 0, "In a relationship": 0, "Married": 0, "It's complicated": 3}
        self.assertEqual(relationship_status(examinations), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 571
