# Input
- Programming Concept: Float
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Practice Task: Calculating Player Score

In modern video games, it is crucial to accurately calculate a player's score, especially when it comes to highscores. Write a function called `calculate_score(kills, assists, deaths)` that calculates the player's score based on the following criteria:

- Each kill gives 10.5 points.
- Each assist gives 5.25 points.
- Each death subtracts 2.75 points.

The function should return the calculated score as a float value.

Example Call:
```python
calculate_score(10, 5, 2)
```
This call should calculate the score for a player with 10 kills, 5 assists, and 2 deaths.

## Code Framework
```python
def calculate_score(kills, assists, deaths):
    ## Insert code here
```

## Model Solution
```python
def calculate_score(kills, assists, deaths):
    return kills * 10.5 + assists * 5.25 - deaths * 2.75

# Example call
print(calculate_score(10, 5, 2))
```

## Unit Tests
```python
import unittest
from main import calculate_score

class TestCalculateScore(unittest.TestCase):
    def test_positive_values(self):
        self.assertAlmostEqual(calculate_score(10, 5, 2), 123.75)

    def test_zero_values(self):
        self.assertAlmostEqual(calculate_score(0, 0, 0), 0.0)

    def test_negative_values(self):
        self.assertAlmostEqual(calculate_score(-10, -5, -2), -123.75)

    def test_mixed_values(self):
        self.assertAlmostEqual(calculate_score(10, 0, 5), 89.75)

    def test_large_values(self):
        self.assertAlmostEqual(calculate_score(1000, 500, 200), 12375.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 435
