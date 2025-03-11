# Input
- Programming Concept: While loops; Boolean and None
- Context: Basketball

# Generated Task Components
## Task Description
### Practice Task: Basketball Training

Write a function named `basketball_training()`, which uses a while loop to count the number of successful shots made by a player. The function should take a list of shots as an argument, where each shot is either `True` (successful) or `False` (not successful). The loop should iterate through the list and count the number of successful shots. If the list is empty, the function should return `None`. Otherwise, the function should return the number of successful shots.

Example call:
```python
basketball_training([True, False, True, True, False])
```
This call should return `3`, as there are three successful shots.

## Code Framework
```python
def basketball_training(throws):
    ## Insert code here
```

## Model Solution
```python
def basketball_training(throws):
    if not throws:
        return None
    count = 0
    i = 0
    while i < len(throws):
        if throws[i]:
            count += 1
        i += 1
    return count

# Example call
print(basketball_training([True, False, True, True, False]))
```

## Unit Tests
```python
import unittest
from main import basketball_training

class TestBasketballTraining(unittest.TestCase):
    def test_empty_list(self):
        self.assertIsNone(basketball_training([]))

    def test_all_successful(self):
        self.assertEqual(basketball_training([True, True, True]), 3)

    def test_all_unsuccessful(self):
        self.assertEqual(basketball_training([False, False, False]), 0)

    def test_mixed_results(self):
        self.assertEqual(basketball_training([True, False, True, True, False]), 3)

    def test_single_successful(self):
        self.assertEqual(basketball_training([True]), 1)

    def test_single_unsuccessful(self):
        self.assertEqual(basketball_training([False]), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 569
