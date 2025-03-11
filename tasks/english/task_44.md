# Input
- Programming Concept: String
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise Task: Relationships and Strings

Write a function named `relationship_status(status)` that takes the relationship status of a person as a string and returns an appropriate message. The possible relationship statuses are:

- "Single"
- "In a relationship"
- "Married"
- "It's complicated"

The function should return a matching message depending on the relationship status:

- For "Single": return "Enjoy your freedom!"
- For "In a relationship": return "Good luck to you both!"
- For "Married": return "Congratulations on your marriage!"
- For "It's complicated": return "All the best for the future!"

Example call: `relationship_status("Married")` returns "Congratulations on your marriage!"

## Code Framework
```python
def relationship_status(status):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(status):
    return {
        "Single": "Enjoy your freedom!",
        "In a relationship": "Good luck to you both!",
        "Married": "Congratulations on your marriage!",
        "It's complicated": "All the best for the future!"
    }.get(status, "Unknown status")

# Example call
print(relationship_status("Married"))
```

## Unit Tests
```python
import unittest
from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_single(self):
        self.assertEqual(relationship_status("Single"), "Enjoy your freedom!")

    def test_in_a_relationship(self):
        self.assertEqual(relationship_status("In a relationship"), "Good luck to you both!")

    def test_married(self):
        self.assertEqual(relationship_status("Married"), "Congratulations on your marriage!")

    def test_its_complicated(self):
        self.assertEqual(relationship_status("It's complicated"), "All the best for the future!")

    def test_unknown_status(self):
        self.assertEqual(relationship_status("Unknown"), "Unknown status")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 462
