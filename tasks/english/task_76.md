# Input
- Programming Concept: For loops
- Context: Basketball

# Generated Task Components
## Task Description
### Practice Task: Basketball Score

Write a function named `calculate_score(point_list)` that receives a list of scored points in a basketball game as an argument. The function should calculate and return the total score. Use a for loop to sum the points.

Example Call:
```python
points = [2, 3, 2, 1, 3, 2]
total_score = calculate_score(points)
print(total_score)  # Output: 13
```

Implement the function `calculate_score(point_list)` so that it correctly calculates and returns the total score.

## Code Framework
```python
def calculate_score(point_list):
    ## Insert code here
```

## Model Solution
```python
def calculate_score(point_list):
    return sum(point_list)

points = [2, 3, 2, 1, 3, 2]
total_score = calculate_score(points)
print(total_score)  # Output: 13
```

## Unit Tests
```python
import unittest
from main import calculate_score

class TestCalculateScore(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(calculate_score([]), 0)

    def test_single_point(self):
        self.assertEqual(calculate_score([2]), 2)

    def test_multiple_points(self):
        self.assertEqual(calculate_score([2, 3, 2, 1, 3, 2]), 13)

    def test_negative_point(self):
        self.assertEqual(calculate_score([2, -1, 3]), 4)

    def test_mixed_points(self):
        self.assertEqual(calculate_score([2, 3, 0, 1, 3, 2]), 11)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 494
