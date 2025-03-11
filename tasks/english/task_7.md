# Input
- Programming Concept: If-Else statements
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Basketball Player Evaluation

Write a function named `evaluate_player(points)` that evaluates the performance of a basketball player based on the number of points scored. The function should return an appropriate message using `return`.

- If the player scores 30 or more points, the message "Outstanding Performance!" should be returned.
- If the player scores between 20 and 29 points, the message "Good Performance!" should be returned.
- If the player scores between 10 and 19 points, the message "Average Performance." should be returned.
- If the player scores less than 10 points, the message "Needs Improvement." should be returned.

Example calls:
- `evaluate_player(35)` returns "Outstanding Performance!".
- `evaluate_player(25)` returns "Good Performance!".
- `evaluate_player(15)` returns "Average Performance.".
- `evaluate_player(5)` returns "Needs Improvement.".

## Code Framework
```python
def evaluate_player(points):
    ## Insert code here
```

## Model Solution
```python
def evaluate_player(points):
    if points >= 30:
        return "Outstanding Performance!"
    elif points >= 20:
        return "Good Performance!"
    elif points >= 10:
        return "Average Performance."
    else:
        return "Needs Improvement."

# Example calls
print(evaluate_player(35))
print(evaluate_player(25))
print(evaluate_player(15))
print(evaluate_player(5))
```

## Unit Tests
```python
import unittest

from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_outstanding_performance(self):
        self.assertEqual(evaluate_player(35), "Outstanding Performance!")
        self.assertEqual(evaluate_player(30), "Outstanding Performance!")

    def test_good_performance(self):
        self.assertEqual(evaluate_player(25), "Good Performance!")
        self.assertEqual(evaluate_player(20), "Good Performance!")

    def test_average_performance(self):
        self.assertEqual(evaluate_player(15), "Average Performance.")
        self.assertEqual(evaluate_player(10), "Average Performance.")

    def test_needs_improvement(self):
        self.assertEqual(evaluate_player(5), "Needs Improvement.")
        self.assertEqual(evaluate_player(0), "Needs Improvement.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 425
