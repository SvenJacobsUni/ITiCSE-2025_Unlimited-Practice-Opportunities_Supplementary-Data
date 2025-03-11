# Input
- Programming Concept: String; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Basketball

# Generated Task Components
## Task Description
### Practice Task: Basketball Player Evaluation

Write a function named `evaluate_player(points, assists, rebounds)`, which evaluates the performance of a basketball player based on their game statistics. The function should accept three parameters:

- `points`: Number of points scored (int)
- `assists`: Number of assists (int)
- `rebounds`: Number of rebounds (int)

The evaluation should be done according to the following criteria:

- If the player scored more than 20 points and gave more than 5 assists, the function should return "Outstanding Performance!".
- If the player scored more than 15 points and collected more than 10 rebounds, the function should return "Strong Performance!".
- If the player scored more than 10 points or gave more than 5 assists, the function should return "Good Performance!".
- In all other cases, the function should return "Average Performance".

Example calls:

```python
evaluate_player(25, 6, 8)  # returns "Outstanding Performance!"
evaluate_player(18, 3, 12)  # returns "Strong Performance!"
evaluate_player(12, 6, 4)  # returns "Good Performance!"
evaluate_player(8, 4, 3)  # returns "Average Performance"
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
        return "Outstanding Performance!"
    elif points > 15 and rebounds > 10:
        return "Strong Performance!"
    elif points > 10 or assists > 5:
        return "Good Performance!"
    else:
        return "Average Performance"

# Example calls
print(evaluate_player(25, 6, 8))  # Outstanding Performance!
print(evaluate_player(18, 3, 12))  # Strong Performance!
print(evaluate_player(12, 6, 4))  # Good Performance!
print(evaluate_player(8, 4, 3))  # Average Performance

```

## Unit Tests
```python
import unittest
from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_outstanding_performance(self):
        self.assertEqual(evaluate_player(25, 6, 8), "Outstanding Performance!")

    def test_strong_performance(self):
        self.assertEqual(evaluate_player(18, 3, 12), "Strong Performance!")

    def test_good_performance_points(self):
        self.assertEqual(evaluate_player(12, 4, 4), "Good Performance!")

    def test_good_performance_assists(self):
        self.assertEqual(evaluate_player(8, 6, 3), "Good Performance!")

    def test_average_performance(self):
        self.assertEqual(evaluate_player(8, 4, 3), "Average Performance")

    def test_edge_case_outstanding_performance(self):
        self.assertEqual(evaluate_player(21, 6, 5), "Outstanding Performance!")

    def test_edge_case_strong_performance(self):
        self.assertEqual(evaluate_player(16, 4, 11), "Strong Performance!")

    def test_edge_case_good_performance(self):
        self.assertEqual(evaluate_player(11, 6, 4), "Good Performance!")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 573
