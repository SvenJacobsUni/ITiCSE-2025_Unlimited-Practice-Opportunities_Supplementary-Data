# Input
- Programming Concept: Operations with numbers;Recursion;Float
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise Task: Calculate Rugby Score

In a rugby game, points can be scored in different ways:
- A Try gives 5 points.
- A Conversion gives 2 points.
- A Penalty or a Dropgoal gives 3 points each.

Write a function `calculate_points(tries, conversions, penalties, dropgoals)`, which calculates the total score of a rugby team. The function should take the number of tries, conversions, penalties, and dropgoals as arguments and return the total score as a `float`.

Example call:
```python
points = calculate_points(3, 2, 1, 1)
print(points)  # Output: 22.0
```

### Extension: Recursive Calculation

Extend the function `calculate_points_recursive(tries, conversions, penalties, dropgoals)`, which has the same functionality as `calculate_points`, but performs the computation of total score recursively.

Example call:
```python
points = calculate_points_recursive(3, 2, 1, 1)
print(points)  # Output: 22.0
```

## Code Framework
```python
def calculate_points(tries, conversions, penalties, dropgoals):
    ## Insert code here

def calculate_points_recursive(tries, conversions, penalties, dropgoals):
    ## Insert code here
```

## Model Solution
```python
def calculate_points(tries, conversions, penalties, dropgoals):
    return tries * 5 + conversions * 2 + penalties * 3 + dropgoals * 3

def calculate_points_recursive(tries, conversions, penalties, dropgoals):
    if tries == 0 and conversions == 0 and penalties == 0 and dropgoals == 0:
        return 0
    if tries > 0:
        return 5 + calculate_points_recursive(tries - 1, conversions, penalties, dropgoals)
    if conversions > 0:
        return 2 + calculate_points_recursive(tries, conversions - 1, penalties, dropgoals)
    if penalties > 0:
        return 3 + calculate_points_recursive(tries, conversions, penalties - 1, dropgoals)
    if dropgoals > 0:
        return 3 + calculate_points_recursive(tries, conversions, penalties, dropgoals - 1)

points = calculate_points(3, 2, 1, 1)
print(points)  # Output: 22.0

points_recursive = calculate_points_recursive(3, 2, 1, 1)
print(points_recursive)  # Output: 22.0
```

## Unit Tests
```python
import unittest
from main import calculate_points, calculate_points_recursive

class TestCalculatePoints(unittest.TestCase):
    def test_all_zero(self):
        self.assertEqual(calculate_points(0, 0, 0, 0), 0.0)
    
    def test_only_tries(self):
        self.assertEqual(calculate_points(3, 0, 0, 0), 15.0)
    
    def test_only_conversions(self):
        self.assertEqual(calculate_points(0, 2, 0, 0), 4.0)
    
    def test_only_penalties(self):
        self.assertEqual(calculate_points(0, 0, 1, 0), 3.0)
    
    def test_only_dropgoals(self):
        self.assertEqual(calculate_points(0, 0, 0, 1), 3.0)
    
    def test_mixed(self):
        self.assertEqual(calculate_points(3, 2, 1, 1), 22.0)

class TestCalculatePointsRecursive(unittest.TestCase):
    def test_all_zero(self):
        self.assertEqual(calculate_points_recursive(0, 0, 0, 0), 0.0)
    
    def test_only_tries(self):
        self.assertEqual(calculate_points_recursive(3, 0, 0, 0), 15.0)
    
    def test_only_conversions(self):
        self.assertEqual(calculate_points_recursive(0, 2, 0, 0), 4.0)
    
    def test_only_penalties(self):
        self.assertEqual(calculate_points_recursive(0, 0, 1, 0), 3.0)
    
    def test_only_dropgoals(self):
        self.assertEqual(calculate_points_recursive(0, 0, 0, 1), 3.0)
    
    def test_mixed(self):
        self.assertEqual(calculate_points_recursive(3, 2, 1, 1), 22.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 628
