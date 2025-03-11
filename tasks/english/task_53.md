# Input
- Programming Concept: While loops
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Basketball Training

Write a function named `basketball_training(target_points)`, which uses a while loop to calculate the number of throws needed for a player to reach a certain number of points. Each successful throw counts as 2 points. The function should return the number of throws.

Example call: `basketball_training(10)` returns `5` because 5 successful throws are needed to reach 10 points.

## Code Framework
```python
def basketball_training(target_points):
    ## Insert code here
```

## Model Solution
```python
def basketball_training(target_points):
    points, throws = 0, 0
    while points < target_points:
        points += 2
        throws += 1
    return throws

basketball_training(10)
```

## Unit Tests
```python
import unittest
from main import basketball_training

class TestBasketballTraining(unittest.TestCase):
    def test_ten_points(self):
        self.assertEqual(basketball_training(10), 5)

    def test_zero_points(self):
        self.assertEqual(basketball_training(0), 0)

    def test_odd_points(self):
        self.assertEqual(basketball_training(7), 4)

    def test_large_points(self):
        self.assertEqual(basketball_training(100), 50)

    def test_negative_points(self):
        self.assertEqual(basketball_training(-5), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 471
