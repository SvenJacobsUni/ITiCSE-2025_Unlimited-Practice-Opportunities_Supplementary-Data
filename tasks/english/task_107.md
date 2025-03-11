# Input
- Programming Concept: If-Else statements; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Basketball Player Evaluation

Write a function named `evaluate_player(points, assists, rebounds)`, which evaluates a basketball player's performance based on their statistics. The function should take three parameters:

- `points`: Number of points scored
- `assists`: Number of assists
- `rebounds`: Number of rebounds

The evaluation is based on the following criteria:

- If the player scored more than 20 points and provided more than 5 assists, the function should return "Outstanding performance!"
- If the player scored more than 15 points or collected more than 10 rebounds, the function should return "Good performance!"
- If the player scored less than 5 points and provided less than 3 assists, the function should return "Poor performance!"
- In all other cases, the function should return "Average performance"

Example calls:

```python
evaluate_player(25, 6, 8)  # returns "Outstanding performance!"
evaluate_player(18, 4, 11)  # returns "Good performance!"
evaluate_player(4, 2, 5)    # returns "Poor performance!"
evaluate_player(10, 4, 7)   # returns "Average performance"
```

## Code Framework
```python
def evaluate_player(points, assists, rebounds):
    ## Insert code here
```

## Model Solution
```python
def evaluate_player(points, assists, rebounds):
    if points > 20 and assists > 5:
        return "Outstanding performance!"
    elif points > 15 or rebounds > 10:
        return "Good performance!"
    elif points < 5 and assists < 3:
        return "Poor performance!"
    else:
        return "Average performance"

# Example calls
print(evaluate_player(25, 6, 8))  # Outstanding performance!
print(evaluate_player(18, 4, 11))  # Good performance!
print(evaluate_player(4, 2, 5))    # Poor performance!
print(evaluate_player(10, 4, 7))   # Average performance
```

## Unit Tests
```python
import unittest

from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_outstanding_performance(self):
        self.assertEqual(evaluate_player(25, 6, 8), "Outstanding performance!")

    def test_good_performance_points(self):
        self.assertEqual(evaluate_player(18, 4, 11), "Good performance!")

    def test_good_performance_rebounds(self):
        self.assertEqual(evaluate_player(10, 4, 11), "Good performance!")

    def test_poor_performance(self):
        self.assertEqual(evaluate_player(4, 2, 5), "Poor performance!")

    def test_average_performance(self):
        self.assertEqual(evaluate_player(10, 4, 7), "Average performance")

    def test_edge_case_outstanding_performance(self):
        self.assertEqual(evaluate_player(21, 6, 8), "Average performance")

    def test_edge_case_good_performance(self):
        self.assertEqual(evaluate_player(16, 4, 10), "Good performance!")

    def test_edge_case_poor_performance(self):
        self.assertEqual(evaluate_player(5, 2, 5), "Average performance")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 539
