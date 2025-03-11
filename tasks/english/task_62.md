# Input
- Programming Concept: Lists
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Fishing and Lists in Python

Write a function named `catch_fish(fish_list)` that receives a list of fish as an argument. The function should count the number of caught fish and return a message indicating the number of fish.

Example call:
```python
catch_fish(["Pike", "Perch", "Trout", "Pike"])
```

Expected return:
```
"You caught 4 fish."
```

## Code Framework
```python
def catch_fish(fish_list):
    ## Insert code here
```

## Model Solution
```python
def catch_fish(fish_list):
    print(f"You caught {len(fish_list)} fish.")

catch_fish(["Pike", "Perch", "Trout", "Pike"])
```

## Unit Tests
```python
import unittest
from main import catch_fish

class TestCatchFish(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(catch_fish([]), "You caught 0 fish.")

    def test_one_fish(self):
        self.assertEqual(catch_fish(["Pike"]), "You caught 1 fish.")

    def test_multiple_fish(self):
        self.assertEqual(catch_fish(["Pike", "Perch", "Trout", "Pike"]), "You caught 4 fish.")

    def test_many_fish(self):
        self.assertEqual(catch_fish(["Pike"] * 100), "You caught 100 fish.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 480
