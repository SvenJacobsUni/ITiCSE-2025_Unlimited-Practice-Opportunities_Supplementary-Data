# Input
- Programming Concept: For loops; Recursion; Operations with numbers
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Sports Points Calculation

Write a function named `points_calculation(player_points)`, which receives a list of points scored by different players in a tournament as an argument. The function should calculate and return the total score of all players. Use a for loop to sum the points. Additionally, implement a recursive function `max_points(points_list)`, which finds and returns the highest score in the list.

Example call:
```python
player_points = [10, 20, 15, 30, 25]
total_points = points_calculation(player_points)
highest_score = max_points(player_points)
print("Total Points:", total_points)  # Output: Total Points: 100
print("Highest Score:", highest_score)  # Output: Highest Score: 30
```

## Code Framework
```python
def points_calculation(player_points):
    ## Insert code here

def max_points(points_list):
    ## Insert code here

```

## Model Solution
```python
def points_calculation(player_points):
    return sum(player_points)

def max_points(points_list):
    if len(points_list) == 1:
        return points_list[0]
    else:
        max_rest = max_points(points_list[1:])
        return points_list[0] if points_list[0] > max_rest else max_rest

player_points = [10, 20, 15, 30, 25]
total_points = points_calculation(player_points)
highest_score = max_points(player_points)
print("Total Points:", total_points)
print("Highest Score:", highest_score)
```

## Unit Tests
```python
import unittest
from main import points_calculation, max_points

class TestPointsCalculation(unittest.TestCase):
    def test_total_points(self):
        self.assertEqual(points_calculation([10, 20, 15, 30, 25]), 100)
        self.assertEqual(points_calculation([0, 0, 0, 0]), 0)
        self.assertEqual(points_calculation([5, 5, 5, 5, 5]), 25)
        self.assertEqual(points_calculation([-10, 20, -15, 30, -25]), 0)
        self.assertEqual(points_calculation([100]), 100)

    def test_max_points(self):
        self.assertEqual(max_points([10, 20, 15, 30, 25]), 30)
        self.assertEqual(max_points([0, 0, 0, 0]), 0)
        self.assertEqual(max_points([5, 5, 5, 5, 5]), 5)
        self.assertEqual(max_points([-10, 20, -15, 30, -25]), 30)
        self.assertEqual(max_points([100]), 100)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 613
