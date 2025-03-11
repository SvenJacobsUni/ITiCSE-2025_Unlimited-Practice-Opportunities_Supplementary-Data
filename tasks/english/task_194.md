# Input
- Programming Concept: Boolean and None;String;Operations with numbers
- Context: Sports

# Generated Task Components
## Task Description
### Exercise Task: Evaluate Athletic Performance

Write a function named `evaluate_performance(points)` that receives a score as an argument and returns a corresponding evaluation as a string. The evaluation is based on the following criteria:

- If the score is greater than or equal to 90, the function should return "Excellent".
- If the score is between 70 and 89 (inclusive), the function should return "Good".
- If the score is between 50 and 69 (inclusive), the function should return "Satisfactory".
- If the score is between 30 and 49 (inclusive), the function should return "Sufficient".
- If the score is less than 30, the function should return "Insufficient".
- If the score is `None`, the function should return "No evaluation possible".

Example calls:
- `evaluate_performance(95)` returns "Excellent".
- `evaluate_performance(75)` returns "Good".
- `evaluate_performance(None)` returns "No evaluation possible".

## Code Framework
```python
def evaluate_performance(points):
    ## Insert code here
```

## Model Solution
```python
def evaluate_performance(points):
    if points is None:
        return "No evaluation possible"
    if points >= 90:
        return "Excellent"
    if points >= 70:
        return "Good"
    if points >= 50:
        return "Satisfactory"
    if points >= 30:
        return "Sufficient"
    return "Insufficient"

# Example calls
print(evaluate_performance(95))  # Excellent
print(evaluate_performance(75))  # Good
print(evaluate_performance(None))  # No evaluation possible
```

## Unit Tests
```python
import unittest
from main import evaluate_performance

class TestEvaluatePerformance(unittest.TestCase):
    def test_excellent(self):
        self.assertEqual(evaluate_performance(95), "Excellent")
        self.assertEqual(evaluate_performance(90), "Excellent")

    def test_good(self):
        self.assertEqual(evaluate_performance(75), "Good")
        self.assertEqual(evaluate_performance(70), "Good")

    def test_satisfactory(self):
        self.assertEqual(evaluate_performance(60), "Satisfactory")
        self.assertEqual(evaluate_performance(50), "Satisfactory")

    def test_sufficient(self):
        self.assertEqual(evaluate_performance(40), "Sufficient")
        self.assertEqual(evaluate_performance(30), "Sufficient")

    def test_insufficient(self):
        self.assertEqual(evaluate_performance(20), "Insufficient")
        self.assertEqual(evaluate_performance(0), "Insufficient")

    def test_no_evaluation(self):
        self.assertEqual(evaluate_performance(None), "No evaluation possible")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 626
