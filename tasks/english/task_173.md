# Input
- Programming Concept: Operations with numbers; Tuples; For loops
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Analyzing Sports Performances

Write a function named `analyze_performances(performances)` that takes a list of tuples as an argument. Each tuple contains the name of an athlete and their score in a competition. The function should calculate and return the average score of all athletes.

Example call:
```python
performances = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
average = analyze_performances(performances)
print(average)  # Expected output: 18.75
```

**Note:** The function should not expect input from standard input.

## Code Framework
```python
def analyze_performances(performances):
    ## Insert code here
```

## Model Solution
```python
def analyze_performances(performances):
    return sum(score for _, score in performances) / len(performances)

performances = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
average = analyze_performances(performances)
print(average)  # Expected output: 18.75
```

## Unit Tests
```python
import unittest

from main import analyze_performances

class TestAnalyzePerformances(unittest.TestCase):
    def test_average(self):
        performances = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
        self.assertEqual(analyze_performances(performances), 18.75)

    def test_empty_list(self):
        performances = []
        with self.assertRaises(ZeroDivisionError):
            analyze_performances(performances)

    def test_single_athlete(self):
        performances = [("Anna", 15)]
        self.assertEqual(analyze_performances(performances), 15)

    def test_negative_scores(self):
        performances = [("Anna", -5), ("Ben", 10)]
        self.assertEqual(analyze_performances(performances), 2.5)

    def test_mixed_scores(self):
        performances = [("Anna", 0), ("Ben", 10), ("Clara", 20)]
        self.assertEqual(analyze_performances(performances), 10)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 605
