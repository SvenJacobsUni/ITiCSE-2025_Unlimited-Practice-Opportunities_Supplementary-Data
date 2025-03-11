# Input
- Programming Concept: Recursion
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Recursive Calculation of Rugby Score

In a rugby game, a team scores points through different actions:

- A Try scores 5 points.
- A Conversion scores 2 points.
- A Penalty or a Dropgoal scores 3 points each.

Write a recursive function `calculate_points(actions)` that receives a list of actions as input and calculates the total score of the team. Each action in the list is a string that can be either "Try", "Conversion", "Penalty", or "Dropgoal".

Sample call:
```python
actions = ["Try", "Conversion", "Penalty", "Try", "Dropgoal"]
print(calculate_points(actions))  # Output: 18
```

Implement the function `calculate_points(actions)` that calculates and returns the total score of the team.

## Code Framework
```python
def calculate_points(actions):
    ## Insert code here
```

## Model Solution
```python
def calculate_points(actions):
    if not actions:
        return 0
    points = {"Try": 5, "Conversion": 2, "Penalty": 3, "Dropgoal": 3}
    return points[actions[0]] + calculate_points(actions[1:])

actions = ["Try", "Conversion", "Penalty", "Try", "Dropgoal"]
print(calculate_points(actions))
```

## Unit Tests
```python
import unittest
from main import calculate_points

class TestCalculatePoints(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(calculate_points([]), 0)

    def test_only_try(self):
        self.assertEqual(calculate_points(["Try"]), 5)

    def test_only_conversion(self):
        self.assertEqual(calculate_points(["Conversion"]), 2)

    def test_only_penalty(self):
        self.assertEqual(calculate_points(["Penalty"]), 3)

    def test_only_dropgoal(self):
        self.assertEqual(calculate_points(["Dropgoal"]), 3)

    def test_mixed_actions(self):
        self.assertEqual(calculate_points(["Try", "Conversion", "Penalty", "Try", "Dropgoal"]), 18)

    def test_multiple_tries(self):
        self.assertEqual(calculate_points(["Try", "Try", "Try"]), 15)

    def test_multiple_conversions(self):
        self.assertEqual(calculate_points(["Conversion", "Conversion", "Conversion"]), 6)

    def test_multiple_penalties(self):
        self.assertEqual(calculate_points(["Penalty", "Penalty", "Penalty"]), 9)

    def test_multiple_dropgoals(self):
        self.assertEqual(calculate_points(["Dropgoal", "Dropgoal", "Dropgoal"]), 9)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 483
