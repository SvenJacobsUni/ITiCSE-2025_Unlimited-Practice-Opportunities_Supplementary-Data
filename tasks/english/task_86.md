# Input
- Programming Concept: While loops
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Fishing with While Loops

Write a function called `fishing()` that simulates how many times a fisherman catches a fish until he has enough fish for a dinner. The fisherman needs at least 5 fish.

The function should use a while loop to simulate the catching process. With each iteration of the loop, the number of caught fish should increase by 1. Once the fisherman has caught 5 or more fish, the loop should terminate and the function should return the total number of caught fish.

Example call: `fishing()` might return `5` if the fisherman catches exactly 5 fish.

## Code Framework
```python
def fishing():
    ## Insert code here
```

## Model Solution
```python
def fishing():
    fish_caught = 0
    while fish_caught < 5:
        fish_caught += 1
    print(fish_caught)

fishing()
```

## Unit Tests
```python
import unittest
from main import fishing

class TestFishing(unittest.TestCase):
    def test_enough_fish(self):
        self.assertEqual(fishing(), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 504
