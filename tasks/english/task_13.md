# Input
- Programming Concept: Higher-order functions
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Higher-order functions in a Rugby context

Write a function `calculate_points(player_points, calculation_function)` that takes a list of points scored by different rugby players and a function as arguments. The function `calculate_points` should apply the passed calculation function to the list of player points and return the result.

Example:
- `player_points` is a list of points, e.g., `[5, 3, 7, 2]`.
- `calculation_function` could be a function that calculates the sum of the points.

Example call:
```python
def sum_points(points):
    return sum(points)

points = [5, 3, 7, 2]
result = calculate_points(points, sum_points)
print(result)  # Output: 17
```

Implement the function `calculate_points` and test it with various calculation functions.

## Code Framework
```python
def calculate_points(player_points, calculation_function):
    ## Insert code here
```

## Model Solution
```python
def calculate_points(player_points, calculation_function):
    return calculation_function(player_points)

def sum_points(points):
    return sum(points)

points = [5, 3, 7, 2]
result = calculate_points(points, sum_points)
print(result)  # Output: 17
```

## Unit Tests
```python
import unittest
from main import calculate_points

def sum_points(points):
    return sum(points)

def max_points(points):
    return max(points)

def min_points(points):
    return min(points)

class TestCalculatePoints(unittest.TestCase):
    def test_sum_points(self):
        self.assertEqual(calculate_points([5, 3, 7, 2], sum_points), 17)

    def test_max_points(self):
        self.assertEqual(calculate_points([5, 3, 7, 2], max_points), 7)

    def test_min_points(self):
        self.assertEqual(calculate_points([5, 3, 7, 2], min_points), 2)

    def test_empty_list_sum(self):
        self.assertEqual(calculate_points([], sum_points), 0)

    def test_empty_list_max(self):
        with self.assertRaises(ValueError):
            calculate_points([], max_points)

    def test_empty_list_min(self):
        with self.assertRaises(ValueError):
            calculate_points([], min_points)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 431
