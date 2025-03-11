# Input
- Programming Concept: Boolean and None; Float
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Assessing Athletic Performance

Write a function named `evaluate_performance(points)`, which evaluates an athlete's performance based on the score. The function should return a `Boolean` value indicating whether the performance is considered "good" (True) or "poor" (False).

Additionally, the function should return `None` if the score is a `Float`, to indicate that the score is invalid.

- If the score is 50 or more, the performance should be considered "good" (True).
- If the score is less than 50, the performance should be considered "poor" (False).
- If the score is a `Float`, the function should return `None`.

Example calls:
- `evaluate_performance(75)` returns `True`.
- `evaluate_performance(30)` returns `False`.
- `evaluate_performance(45.5)` returns `None`.

## Code Framework
```python
def evaluate_performance(points):
    ## Insert code here
```

## Model Solution
```python
def evaluate_performance(points):
    if isinstance(points, float):
        return None
    return points >= 50

# Example calls
print(evaluate_performance(75))  # True
print(evaluate_performance(30))  # False
print(evaluate_performance(45.5))  # None
```

## Unit Tests
```python
import unittest

from main import evaluate_performance

class TestEvaluatePerformance(unittest.TestCase):
    def test_good_performance(self):
        self.assertTrue(evaluate_performance(75))

    def test_poor_performance(self):
        self.assertFalse(evaluate_performance(30))

    def test_invalid_score(self):
        self.assertIsNone(evaluate_performance(45.5))

    def test_boundary_good(self):
        self.assertTrue(evaluate_performance(50))

    def test_boundary_poor(self):
        self.assertFalse(evaluate_performance(49))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 543
