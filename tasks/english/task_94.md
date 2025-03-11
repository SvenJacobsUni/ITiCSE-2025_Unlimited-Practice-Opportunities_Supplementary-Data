# Input
- Programming Concept: Float
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Rugby Score Calculation

Write a function named `calculate_score(tries, conversions, penalties)` that calculates the score of a rugby game.

- A try scores 5 points.
- A conversion scores 2 points.
- A penalty scores 3 points.

The function should take three parameters:
- `tries` (float): Number of tries scored.
- `conversions` (float): Number of conversions scored.
- `penalties` (float): Number of penalties scored.

The function should return the total score as a float.

Example call:
```python
calculate_score(3.0, 2.0, 1.0)
```
This call should return the value `21.0`.

## Code Framework
```python
def calculate_score(tries, conversions, penalties):
    ## Insert code here
```

## Model Solution
```python
def calculate_score(tries, conversions, penalties):
    return tries * 5 + conversions * 2 + penalties * 3

print(calculate_score(3.0, 2.0, 1.0))
```

## Unit Tests
```python
import unittest

from main import calculate_score

class TestCalculateScore(unittest.TestCase):
    def test_all_types_of_points(self):
        self.assertEqual(calculate_score(3.0, 2.0, 1.0), 21.0)

    def test_only_tries(self):
        self.assertEqual(calculate_score(4.0, 0.0, 0.0), 20.0)

    def test_only_conversions(self):
        self.assertEqual(calculate_score(0.0, 3.0, 0.0), 6.0)

    def test_only_penalties(self):
        self.assertEqual(calculate_score(0.0, 0.0, 5.0), 15.0)

    def test_no_points(self):
        self.assertEqual(calculate_score(0.0, 0.0, 0.0), 0.0)

    def test_mixed_points(self):
        self.assertEqual(calculate_score(2.0, 3.0, 4.0), 25.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 512
