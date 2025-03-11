# Input
- Programming Concept: Tuples
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Fishing with Tuples

Write a function named `catch_fish(fishes)` that takes a tuple of fish species as an argument. The function should count the number of different species in the tuple and return a new tuple containing the species and their respective frequencies.

Example call:
```python
fishes = ("Pike", "Carp", "Pike", "Trout", "Carp", "Pike")
print(catch_fish(fishes))
```

Expected output:
```python
(("Pike", 3), ("Carp", 2), ("Trout", 1))
```

## Code Framework
```python
def catch_fish(fishes):
    ## Insert code here
```

## Model Solution
```python
def catch_fish(fishes):
    return tuple((fish, fishes.count(fish)) for fish in set(fishes))

fishes = ("Pike", "Carp", "Pike", "Trout", "Carp", "Pike")
print(catch_fish(fishes))
```

## Unit Tests
```python
import unittest
from main import catch_fish

class TestCatchFish(unittest.TestCase):
    def test_simple_case(self):
        fishes = ("Pike", "Carp", "Pike", "Trout", "Carp", "Pike")
        expected = (("Pike", 3), ("Carp", 2), ("Trout", 1))
        self.assertEqual(catch_fish(fishes), expected)

    def test_empty_tuple(self):
        fishes = ()
        expected = ()
        self.assertEqual(catch_fish(fishes), expected)

    def test_one_fish(self):
        fishes = ("Pike",)
        expected = (("Pike", 1),)
        self.assertEqual(catch_fish(fishes), expected)

    def test_all_different(self):
        fishes = ("Pike", "Carp", "Trout")
        expected = (("Pike", 1), ("Carp", 1), ("Trout", 1))
        self.assertEqual(catch_fish(fishes), expected)

    def test_same_fishes(self):
        fishes = ("Pike", "Pike", "Pike")
        expected = (("Pike", 3),)
        self.assertEqual(catch_fish(fishes), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 442
