# Input
- Programming Concept: Recursion;For loops
- Context: Basketball

# Generated Task Components
## Task Description
### Practice Task: Basketball Score

Write a function named `calculate_score(player_points)` that takes a list of points scored by different basketball players in a game as an argument. The function should recursively calculate and return the sum of all points. Additionally, use a for loop to output the points of each player.

Example:
```python
player_points = [12, 15, 10, 8, 20]
```

Function Call:
```python
calculate_score(player_points)
```

Expected Output:
```
Player 1 scored 12 points.
Player 2 scored 15 points.
Player 3 scored 10 points.
Player 4 scored 8 points.
Player 5 scored 20 points.
```

Return Value:
```
65
```


## Code Framework
```python
def calculate_score(player_points):
    ## Insert code here
```

## Model Solution
```python
def calculate_score(player_points):
    def sum_points(points):
        if not points:
            return 0
        return points[0] + sum_points(points[1:])
    
    for i, points in enumerate(player_points, 1):
        print(f"Player {i} scored {points} points.")
    
    return sum_points(player_points)

player_points = [12, 15, 10, 8, 20]
print(calculate_score(player_points))
```

## Unit Tests
```python
import unittest
from main import calculate_score

class TestCalculateScore(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(calculate_score([12, 15, 10, 8, 20]), 65)

    def test_empty_list(self):
        self.assertEqual(calculate_score([]), 0)

    def test_single_element(self):
        self.assertEqual(calculate_score([25]), 25)

    def test_negative_and_positive(self):
        self.assertEqual(calculate_score([-5, 10, -3, 8]), 10)

    def test_large_numbers(self):
        self.assertEqual(calculate_score([1000, 2000, 3000, 4000]), 10000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 565
