# Input
- Programming Concept: Recursion; Functions as variables
- Context: Basketball

# Generated Task Components
## Task Description
### Practice Task: Recursive Calculation of Basketball Points

Write a recursive function named `calculate_points(player_points)` that calculates the total score of a basketball player. The function should take a list of points as an argument, where each entry in the list represents the points from a single game. The function should sum the points of all games and return the result.

Example call:
```python
points = [10, 15, 20, 5]
total_points = calculate_points(points)
print(total_points)  # Output: 50
```

### Requirements:
- The function `calculate_points` should be implemented recursively.
- The function should sum the points of all games in the list and return the result.
- The function should not expect any input from standard input.

### Example:
```python
points = [12, 8, 25, 10]
total_points = calculate_points(points)
print(total_points)  # Output: 55
```

Implement the function `calculate_points(player_points)` in Python.

## Code Framework
```python
def calculate_points(player_points):
    ## Insert code here
```

## Model Solution
```python
def calculate_points(player_points):
    if not player_points:
        return 0
    return player_points[0] + calculate_points(player_points[1:])

points = [12, 8, 25, 10]
total_points = calculate_points(points)
print(total_points)  # Output: 55
```

## Unit Tests
```python
import unittest
from main import calculate_points

class TestCalculatePoints(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(calculate_points([]), 0)

    def test_single_game(self):
        self.assertEqual(calculate_points([10]), 10)

    def test_multiple_games(self):
        self.assertEqual(calculate_points([10, 15, 20, 5]), 50)

    def test_negative_points(self):
        self.assertEqual(calculate_points([10, -5, 20, -10]), 15)

    def test_large_numbers(self):
        self.assertEqual(calculate_points([1000, 2000, 3000, 4000]), 10000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 564
