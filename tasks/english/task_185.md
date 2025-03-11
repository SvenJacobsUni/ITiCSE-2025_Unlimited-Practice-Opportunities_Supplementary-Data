# Input
- Programming Concept: Recursion;Float;Integer
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise Task: Recursive Calculation of Medal Points

In the Olympic Games, medals are awarded in gold, silver, and bronze. Each medal has a specific point value:

- Gold: 3 points
- Silver: 2 points
- Bronze: 1 point

Write a recursive function `calculate_medal_points(gold, silver, bronze)` that calculates the total score for a nation based on the number of medals won. The parameters `gold`, `silver`, and `bronze` are integers that indicate the number of each type of medal won. The function should return the total score as a floating-point number (Float).

Example call:
```python
points = calculate_medal_points(5, 3, 2)
print(points)  # Output: 21.0
```

Implement the function to work recursively.

## Code Framework
```python
def calculate_medal_points(gold, silver, bronze):
    ## Insert code here
```

## Model Solution
```python
def calculate_medal_points(gold, silver, bronze):
    if gold == 0 and silver == 0 and bronze == 0:
        return 0.0
    if gold > 0:
        return 3.0 + calculate_medal_points(gold - 1, silver, bronze)
    if silver > 0:
        return 2.0 + calculate_medal_points(gold, silver - 1, bronze)
    return 1.0 + calculate_medal_points(gold, silver, bronze - 1)

points = calculate_medal_points(5, 3, 2)
print(points)  # Output: 21.0
```

## Unit Tests
```python
import unittest
from main import calculate_medal_points

class TestCalculateMedalPoints(unittest.TestCase):
    def test_no_medals(self):
        self.assertEqual(calculate_medal_points(0, 0, 0), 0.0)

    def test_only_gold(self):
        self.assertEqual(calculate_medal_points(5, 0, 0), 15.0)

    def test_only_silver(self):
        self.assertEqual(calculate_medal_points(0, 3, 0), 6.0)

    def test_only_bronze(self):
        self.assertEqual(calculate_medal_points(0, 0, 2), 2.0)

    def test_mixed_medals(self):
        self.assertEqual(calculate_medal_points(5, 3, 2), 21.0)

    def test_edge_case(self):
        self.assertEqual(calculate_medal_points(1, 1, 1), 6.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 617
