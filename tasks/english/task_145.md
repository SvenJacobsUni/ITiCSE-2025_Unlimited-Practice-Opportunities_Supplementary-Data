# Input
- Programming Concept: Functions as variables; If-Else statements
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Check Relationship Status

Write a function named `relationship_status(status)` that checks a person's current relationship status and returns an appropriate message. The function should return one of the following messages based on the passed status:

- If the status is "taken", the message "Congratulations on the relationship!" should be returned.
- If the status is "single", the message "Enjoy your freedom!" should be returned.
- If the status is "complicated", the message "Relationships can sometimes be difficult." should be returned.
- For all other statuses, the message "Unknown relationship status." should be returned.

Example calls:
- `relationship_status("taken")` returns "Congratulations on the relationship!".
- `relationship_status("single")` returns "Enjoy your freedom!".
- `relationship_status("complicated")` returns "Relationships can sometimes be difficult.".
- `relationship_status("widowed")` returns "Unknown relationship status.".

## Code Framework
```python
def relationship_status(status):
    ## Insert code here
```

## Model Solution
```python
def relationship_status(status):
    if status == "taken":
        return "Congratulations on the relationship!"
    elif status == "single":
        return "Enjoy your freedom!"
    elif status == "complicated":
        return "Relationships can sometimes be difficult."
    else:
        return "Unknown relationship status."

# Example calls
print(relationship_status("taken"))
print(relationship_status("single"))
print(relationship_status("complicated"))
print(relationship_status("widowed"))
```

## Unit Tests
```python
import unittest

from main import relationship_status

class TestRelationshipStatus(unittest.TestCase):
    def test_taken(self):
        self.assertEqual(relationship_status("taken"), "Congratulations on the relationship!")

    def test_single(self):
        self.assertEqual(relationship_status("single"), "Enjoy your freedom!")

    def test_complicated(self):
        self.assertEqual(relationship_status("complicated"), "Relationships can sometimes be difficult.")

    def test_unknown(self):
        self.assertEqual(relationship_status("widowed"), "Unknown relationship status.")

    def test_empty_string(self):
        self.assertEqual(relationship_status(""), "Unknown relationship status.")

    def test_none(self):
        self.assertEqual(relationship_status(None), "Unknown relationship status.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 577
