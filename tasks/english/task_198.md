# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not); Tuples; For loops
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Mental Health and Activity Level

Write a function named `evaluate_activity(days)` that takes a tuple of 7 integers (each between 0 and 24) as input. Each number in the tuple represents the number of hours a person was active on a specific day of the week. The function should evaluate the person's activity levels and return an appropriate message.

- If the person was active for more than 1 hour on at least 5 days of the week, return the message "Well done! You are very active."
- If the person was active for more than 1 hour on at least 3 days of the week, return the message "Not bad, but there's room for improvement."
- Otherwise, return the message "Try to be more active to improve your mental health."

Example call:
```python
evaluate_activity((1, 2, 0, 3, 4, 0, 1))
```

Expected output:
```
Not bad, but there's room for improvement.
```

## Code Framework
```python
def evaluate_activity(days):
    ## Insert code here
```

## Model Solution
```python
def evaluate_activity(days):
    active_days = sum(1 for hours in days if hours > 1)
    if active_days >= 5:
        return "Well done! You are very active."
    elif active_days >= 3:
        return "Not bad, but there's room for improvement."
    else:
        return "Try to be more active to improve your mental health."

evaluate_activity((1, 2, 0, 3, 4, 0, 1))
```

## Unit Tests
```python
import unittest
from main import evaluate_activity

class TestEvaluateActivity(unittest.TestCase):
    def test_very_active(self):
        self.assertEqual(evaluate_activity((2, 3, 4, 5, 6, 1, 0)), "Well done! You are very active.")

    def test_moderately_active(self):
        self.assertEqual(evaluate_activity((1, 2, 0, 3, 4, 0, 1)), "Not bad, but there's room for improvement.")

    def test_less_active(self):
        self.assertEqual(evaluate_activity((0, 1, 0, 1, 0, 0, 0)), "Try to be more active to improve your mental health.")

    def test_boundary_active(self):
        self.assertEqual(evaluate_activity((1, 2, 1, 2, 1, 2, 1)), "Not bad, but there's room for improvement.")

    def test_boundary_very_active(self):
        self.assertEqual(evaluate_activity((2, 2, 2, 2, 2, 0, 0)), "Well done! You are very active.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 630
