# Input
- Programming Concept: Lists;Float
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise: Olympics - Calculate Average Score

Write a function named `average_score(scores)` that receives a list of scores (as float values) and calculates and returns the average score of athletes.

Example call:
```python
scores = [9.5, 8.7, 9.8, 7.6, 8.9]
print(average_score(scores))  # Output: 8.9
```

The function should calculate the average score of the athletes and return it as a float value.

## Code Framework
```python
def average_score(scores):
    ## Insert code here

```

## Model Solution
```python
def average_score(scores):
    return sum(scores) / len(scores)

scores = [9.5, 8.7, 9.8, 7.6, 8.9]
print(average_score(scores))
```

## Unit Tests
```python
import unittest
from main import average_score

class TestAverageScore(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(average_score([9.5, 8.7, 9.8, 7.6, 8.9]), 8.9)

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            average_score([])

    def test_single_element(self):
        self.assertEqual(average_score([10.0]), 10.0)

    def test_mixed_values(self):
        self.assertEqual(average_score([1.0, 2.0, 3.0, 4.0, 5.0]), 3.0)

    def test_negative_values(self):
        self.assertEqual(average_score([-1.0, -2.0, -3.0, -4.0, -5.0]), -3.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 550
