# Input
- Programming Concept: Lists
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Fishing and Lists in Python

Write a function named `catch_fishes(fishes)` that takes a list of fishes as an argument. The function should count the number of fishes caught and return a message indicating the number of fishes.

Example call:
```python
catch_fishes(["Pike", "Bass", "Trout", "Pike"])
```

Expected return:
```python
"You have caught 4 fishes."
```

## Code Framework
```python
def catch_fishes(fishes):
    ## Insert code here

```

## Model Solution
```python
def catch_fishes(fishes):
    print(f"You have caught {len(fishes)} fishes.")

catch_fishes(["Pike", "Bass", "Trout", "Pike"])

```

## Unit Tests
```python
import unittest
from main import catch_fishes

class TestCatchFishes(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(catch_fishes([]), "You have caught 0 fishes.")

    def test_one_fish(self):
        self.assertEqual(catch_fishes(["Pike"]), "You have caught 1 fish.")

    def test_multiple_fishes(self):
        self.assertEqual(catch_fishes(["Pike", "Bass", "Trout", "Pike"]), "You have caught 4 fishes.")

    def test_many_fishes(self):
        self.assertEqual(catch_fishes(["Pike"] * 100), "You have caught 100 fishes.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 502
