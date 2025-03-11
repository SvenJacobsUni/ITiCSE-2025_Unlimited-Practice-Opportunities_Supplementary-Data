# Input
- Programming Concept: Integer
- Context: Sports

# Generated Task Components
## Task Description
### Practice Task: Sporting Score Calculation

Write a function named `calculate_points(goals, assists)` that calculates the total score of a player in a football match. The player receives 3 points for each goal scored and 1 point for each assist. The function should return the total score as an integer.

Example Call:
```python
calculate_points(2, 3)
```
This call should return 9 because the player scored 2 goals (2 * 3 = 6 points) and made 3 assists (3 * 1 = 3 points), totaling 9 points.

## Code Framework
```python
def calculate_points(goals, assists):
    ## Insert code here
```

## Model Solution
```python
def calculate_points(goals, assists):
    return goals * 3 + assists

# Example call
print(calculate_points(2, 3))
```

## Unit Tests
```python
import unittest

from main import calculate_points

class TestCalculatePoints(unittest.TestCase):
    def test_no_goals_and_assists(self):
        self.assertEqual(calculate_points(0, 0), 0)

    def test_only_goals(self):
        self.assertEqual(calculate_points(3, 0), 9)

    def test_only_assists(self):
        self.assertEqual(calculate_points(0, 4), 4)

    def test_goals_and_assists(self):
        self.assertEqual(calculate_points(2, 3), 9)

    def test_large_numbers(self):
        self.assertEqual(calculate_points(100, 200), 500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 506
