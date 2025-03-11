# Input
- Programming Concept: For loops;While loops;If-Else statements
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Count Fish

Write a function named `count_fish(fish_list)` that takes a list of fish as input. The function should count the number of fish in the list while distinguishing between "Carp" and "Pike".

- If the fish is a "Carp", it should be added to the Carp count.
- If the fish is a "Pike", it should be added to the Pike count.
- All other fish should be ignored.

The function should return a dictionary containing the number of Carp and Pike.

Example call:
```python
fish = ["Carp", "Pike", "Carp", "Trout", "Pike", "Carp"]
print(count_fish(fish))
```

Expected output:
```python
{"Carp": 3, "Pike": 2}
```

## Code Framework
```python
def count_fish(fish_list):
    ## Insert code here

```

## Model Solution
```python
def count_fish(fish_list):
    count = {"Carp": 0, "Pike": 0}
    for fish in fish_list:
        if fish in count:
            count[fish] += 1
    return count

fish = ["Carp", "Pike", "Carp", "Trout", "Pike", "Carp"]
print(count_fish(fish))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_mixed_fish(self):
        self.assertEqual(count_fish(["Carp", "Pike", "Carp", "Trout", "Pike", "Carp"]), {"Carp": 3, "Pike": 2})

    def test_only_carp(self):
        self.assertEqual(count_fish(["Carp", "Carp", "Carp"]), {"Carp": 3, "Pike": 0})

    def test_only_pike(self):
        self.assertEqual(count_fish(["Pike", "Pike", "Pike"]), {"Carp": 0, "Pike": 3})

    def test_no_fish(self):
        self.assertEqual(count_fish([]), {"Carp": 0, "Pike": 0})

    def test_ignored_fish(self):
        self.assertEqual(count_fish(["Trout", "Perch", "Catfish"]), {"Carp": 0, "Pike": 0})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 611
