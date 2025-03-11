# Input
- Programming Concept: Higher-order functions; Control structures (==, !=, <, >, <=, >=, or, and, not); Operations with numbers
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Evaluate Athletic Performance

Write a function named `evaluate_performance(points)` that takes a score as an argument and returns a corresponding evaluation. The evaluation is based on the following criteria:

- If the score is 90 or greater, the function should return "Excellent".
- If the score is between 75 and 89 (inclusive), the function should return "Good".
- If the score is between 50 and 74 (inclusive), the function should return "Satisfactory".
- If the score is less than 50, the function should return "Needs Improvement".

Example calls:

```python
print(evaluate_performance(95))  # Output: Excellent
print(evaluate_performance(80))  # Output: Good
print(evaluate_performance(60))  # Output: Satisfactory
print(evaluate_performance(45))  # Output: Needs Improvement
```

## Code Framework
```python
def evaluate_performance(points):
    ## Insert code here
```

## Model Solution
```python
def evaluate_performance(points):
    if points >= 90:
        return "Excellent"
    elif points >= 75:
        return "Good"
    elif points >= 50:
        return "Satisfactory"
    else:
        return "Needs Improvement"

print(evaluate_performance(95))  # Output: Excellent
print(evaluate_performance(80))  # Output: Good
print(evaluate_performance(60))  # Output: Satisfactory
print(evaluate_performance(45))  # Output: Needs Improvement
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
        self.assertEqual(evaluate_performance(80), "Good")
        self.assertEqual(evaluate_performance(75), "Good")

    def test_satisfactory(self):
        self.assertEqual(evaluate_performance(60), "Satisfactory")
        self.assertEqual(evaluate_performance(50), "Satisfactory")

    def test_needs_improvement(self):
        self.assertEqual(evaluate_performance(45), "Needs Improvement")
        self.assertEqual(evaluate_performance(0), "Needs Improvement")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 594
