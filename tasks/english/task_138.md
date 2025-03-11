# Input
- Programming Concept: Boolean and None; String
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Check Relationship Status

Write a function named `relationship_status(status)`, that checks the relationship status of a person and returns a corresponding message. The function should take a string `status` as an argument and return an appropriate message based on the input.

- If the `status` is "in a relationship", the function should return "Congratulations on your relationship!".
- If the `status` is "single", the function should return "Enjoy your freedom!".
- If the `status` is "complicated", the function should return "Relationships can sometimes be difficult.".
- For all other inputs, the function should return `None`.

Example Calls:
- `relationship_status("in a relationship")` returns "Congratulations on your relationship!".
- `relationship_status("single")` returns "Enjoy your freedom!".
- `relationship_status("complicated")` returns "Relationships can sometimes be difficult.".
- `relationship_status("unknown")` returns `None`.

## Code Framework
```python
def relationship_status(status):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(status):
    if status == "in a relationship":
        return "Congratulations on your relationship!"
    elif status == "single":
        return "Enjoy your freedom!"
    elif status == "complicated":
        return "Relationships can sometimes be difficult."
    else:
        return None

# Example Calls
print(relationship_status("in a relationship"))
print(relationship_status("single"))
print(relationship_status("complicated"))
print(relationship_status("unknown"))
```

## Unit Tests
```python
import unittest

from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_in_a_relationship(self):
        self.assertEqual(relationship_status("in a relationship"), "Congratulations on your relationship!")

    def test_single(self):
        self.assertEqual(relationship_status("single"), "Enjoy your freedom!")

    def test_complicated(self):
        self.assertEqual(relationship_status("complicated"), "Relationships can sometimes be difficult.")

    def test_unknown(self):
        self.assertIsNone(relationship_status("unknown"))

    def test_empty_string(self):
        self.assertIsNone(relationship_status(""))

    def test_none(self):
        self.assertIsNone(relationship_status(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 570
