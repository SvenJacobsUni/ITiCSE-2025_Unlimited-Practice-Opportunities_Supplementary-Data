# Input
- Programming Concept: Operations with numbers
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Calculate Basketball Score

Write a function named `calculate_score(twos, threes)` that calculates the score of a basketball game based on the number of two-point and three-point shots made. The function should take two arguments:

- `twos`: The number of two-point shots made.
- `threes`: The number of three-point shots made.

The function should calculate and return the total score.

Example call:
```python
score = calculate_score(10, 5)
print(score)  # Output: 35
```

In this example, 10 two-point shots (10 * 2 = 20 points) and 5 three-point shots (5 * 3 = 15 points) were made, resulting in a total of 35 points.

## Code Framework
```python
def calculate_score(twos, threes):
    ## Insert code here
```

## Model Solution
```python
def calculate_score(twos, threes):
    return twos * 2 + threes * 3

print(calculate_score(10, 5))  # Output: 35
```

## Unit Tests
```python
import unittest
from main import calculate_score

class TestCalculateScore(unittest.TestCase):
    def test_no_points(self):
        self.assertEqual(calculate_score(0, 0), 0)

    def test_only_twos(self):
        self.assertEqual(calculate_score(10, 0), 20)

    def test_only_threes(self):
        self.assertEqual(calculate_score(0, 5), 15)

    def test_mixed(self):
        self.assertEqual(calculate_score(10, 5), 35)

    def test_large_numbers(self):
        self.assertEqual(calculate_score(1000, 500), 3500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 470
