# Input
- Programming Concept: Integer; Logical operators (==, !=, <, >, <=, >=, or, and, not); Lists
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Basketball Statistics

Write a function called `evaluate_player(points_list)`, which receives a list of points scored by a basketball player in different games. The function should assess the player's performance and return an appropriate message.

- If the player scored more than 30 points in any game, the message 'Outstanding performance!' should be returned.
- If the player scored at least 10 points in all games, the message 'Consistently good performance!' should be returned.
- If the player scored no more than 5 points in any game, the message 'Weak performance!' should be returned.
- In all other cases, the message 'Average performance.' should be returned.

Example calls:
- `evaluate_player([12, 15, 8, 22, 30])` returns 'Average performance.'
- `evaluate_player([35, 28, 40, 22, 31])` returns 'Outstanding performance!'
- `evaluate_player([10, 12, 14, 11, 10])` returns 'Consistently good performance!'
- `evaluate_player([3, 4, 2, 5, 1])` returns 'Weak performance!'

## Code Framework
```python
def evaluate_player(points_list):
    ## Insert code here
```

## Model Solution
```python
def evaluate_player(points_list):
    if any(p > 30 for p in points_list):
        return 'Outstanding performance!'
    elif all(p >= 10 for p in points_list):
        return 'Consistently good performance!'
    elif all(p <= 5 for p in points_list):
        return 'Weak performance!'
    else:
        return 'Average performance.'

# Example calls
print(evaluate_player([12, 15, 8, 22, 30]))
print(evaluate_player([35, 28, 40, 22, 31]))
print(evaluate_player([10, 12, 14, 11, 10]))
print(evaluate_player([3, 4, 2, 5, 1]))
```

## Unit Tests
```python
import unittest
from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_outstanding_performance(self):
        self.assertEqual(evaluate_player([35, 28, 40, 22, 31]), 'Outstanding performance!')

    def test_consistently_good_performance(self):
        self.assertEqual(evaluate_player([10, 12, 14, 11, 10]), 'Consistently good performance!')

    def test_weak_performance(self):
        self.assertEqual(evaluate_player([3, 4, 2, 5, 1]), 'Weak performance!')

    def test_average_performance(self):
        self.assertEqual(evaluate_player([12, 15, 8, 22, 30]), 'Average performance.')

    def test_empty_list(self):
        self.assertEqual(evaluate_player([]), 'Average performance.')

    def test_boundary_30_points(self):
        self.assertEqual(evaluate_player([30, 30, 30]), 'Average performance.')

    def test_boundary_10_points(self):
        self.assertEqual(evaluate_player([10, 10, 10]), 'Consistently good performance.')

    def test_boundary_5_points(self):
        self.assertEqual(evaluate_player([5, 5, 5]), 'Weak performance.')

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 620
