# Input
- Programming Concept: Boolean and None
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Sporting Activity

Write a function named `is_sporty(activity)`, which checks if a given activity is considered sporty. The function should return a Boolean value: `True` if the activity is sporty, and `False` if it is not. If the activity is not included in the list of known activities, the function should return `None`.

Known sporty activities are:
- "Running"
- "Swimming"
- "Cycling"
- "Football"
- "Basketball"

Sample calls:
- `is_sporty("Running")` returns `True`.
- `is_sporty("Chess")` returns `False`.
- `is_sporty("Dancing")` returns `None`.

## Code Framework
```python
def is_sporty(activity):
    ## Insert code here
```

## Model Solution
```python
def is_sporty(activity):
    sporty_activities = ["Running", "Swimming", "Cycling", "Football", "Basketball"]
    if activity in sporty_activities:
        return True
    elif activity in ["Chess", "Dancing"]:
        return False
    return None

# Sample calls
print(is_sporty("Running"))  # True
print(is_sporty("Chess"))  # False
print(is_sporty("Dancing"))  # None
```

## Unit Tests
```python
import unittest
from main import is_sporty

class TestIsSporty(unittest.TestCase):
    def test_sporty_activity(self):
        self.assertTrue(is_sporty("Running"))
        self.assertTrue(is_sporty("Swimming"))
        self.assertTrue(is_sporty("Cycling"))
        self.assertTrue(is_sporty("Football"))
        self.assertTrue(is_sporty("Basketball"))

    def test_non_sporty_activity(self):
        self.assertFalse(is_sporty("Chess"))

    def test_unknown_activity(self):
        self.assertIsNone(is_sporty("Dancing"))
        self.assertIsNone(is_sporty("Reading"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 485
