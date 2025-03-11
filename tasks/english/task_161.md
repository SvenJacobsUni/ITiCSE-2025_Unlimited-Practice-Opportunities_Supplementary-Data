# Input
- Programming Concept: Functions as variables;Integer;Recursion
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise Task: Mental Health - Recursive Calculation of Well-being

Write a function named `calculate_wellbeing(days)` that calculates a person's well-being over a certain number of days. The well-being is defined by a simple recursive formula:

- On a specific day `n`, the well-being is the sum of the well-being of the two previous days `n-1` and `n-2`.
- The well-being on the first day (`n=1`) is 1.
- The well-being on the second day (`n=2`) is 1.

The function should take the number of days `days` as an argument and return the well-being on the last day.

Example call: `calculate_wellbeing(5)` returns `5`.

### Context

In psychology, it's often studied how a person's well-being develops over time. This task simulates a simple model of well-being, where the well-being on a specific day depends on previous days.

## Code Framework
```python
def calculate_wellbeing(days):
    ## Insert code here
```

## Model Solution
```python
def calculate_wellbeing(days):
    if days <= 2:
        return 1
    return calculate_wellbeing(days-1) + calculate_wellbeing(days-2)

print(calculate_wellbeing(5))
```

## Unit Tests
```python
import unittest
from main import calculate_wellbeing

class TestCalculateWellbeing(unittest.TestCase):
    def test_wellbeing_day_1(self):
        self.assertEqual(calculate_wellbeing(1), 1)

    def test_wellbeing_day_2(self):
        self.assertEqual(calculate_wellbeing(2), 1)

    def test_wellbeing_day_3(self):
        self.assertEqual(calculate_wellbeing(3), 2)

    def test_wellbeing_day_5(self):
        self.assertEqual(calculate_wellbeing(5), 5)

    def test_wellbeing_day_10(self):
        self.assertEqual(calculate_wellbeing(10), 55)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 593
