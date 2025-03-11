# Input
- Programming Concept: String;Integer;For loops
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Count Fish

Write a function named `count_fish(fish_types)` that receives a list of strings as an argument. Each string in the list represents a type of fish caught on a given day. The function should count the number of each type of fish and return the result as a dictionary, where the fish type is the key and the number of fish caught is the value.

Example call:
```python
fish_types = ["Pike", "Carp", "Pike", "Trout", "Carp", "Pike"]
print(count_fish(fish_types))
```

Expected output:
```python
{"Pike": 3, "Carp": 2, "Trout": 1}
```

## Code Framework
```python
def count_fish(fish_types):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_types):
    counts = {}
    for fish in fish_types:
        if fish in counts:
            counts[fish] += 1
        else:
            counts[fish] = 1
    return counts

fish_types = ["Pike", "Carp", "Pike", "Trout", "Carp", "Pike"]
print(count_fish(fish_types))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Pike", "Trout", "Carp", "Pike"]), {"Pike": 3, "Carp": 2, "Trout": 1})

    def test_empty_list(self):
        self.assertEqual(count_fish([]), {})

    def test_single_fish_type(self):
        self.assertEqual(count_fish(["Pike", "Pike", "Pike"]), {"Pike": 3})

    def test_different_fish_types(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Trout"]), {"Pike": 1, "Carp": 1, "Trout": 1})

    def test_mixed_fish_types(self):
        self.assertEqual(count_fish(["Pike", "Carp", "Pike", "Trout", "Carp", "Pike", "Trout", "Trout"]), {"Pike": 3, "Carp": 2, "Trout": 3})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 616
