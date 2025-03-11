# Input
- Programming Concept: Recursion
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise: Recursion in the Aquarium

Write a recursive function named `count_fish(aquarium)` that counts the number of fish in a nested aquarium. An aquarium can either be empty, contain a list of fish, or a list of other aquariums (which in turn can contain fish or further aquariums).

An example call could look like this:
```python
aquarium = [[], ["Fish1", "Fish2"], [["Fish3"], []], "Fish4"]
print(count_fish(aquarium))  # Output: 4
```

Implement the function `count_fish(aquarium)` that returns the total number of fish in the entire nested aquarium.

## Code Framework
```python
def count_fish(aquarium):
    ## Insert code here

```

## Model Solution
```python
def count_fish(aquarium):
    if not isinstance(aquarium, list):
        return 1
    return sum(count_fish(item) for item in aquarium)

aquarium = [[], ["Fish1", "Fish2"], [["Fish3"], []], "Fish4"]
print(count_fish(aquarium))  # Output: 4

```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_empty_aquarium(self):
        self.assertEqual(count_fish([]), 0)

    def test_one_fish(self):
        self.assertEqual(count_fish(["Fish1"]), 1)

    def test_multiple_fish(self):
        self.assertEqual(count_fish(["Fish1", "Fish2", "Fish3"]), 3)

    def test_nested_aquarium(self):
        self.assertEqual(count_fish([[], ["Fish1", "Fish2"], [["Fish3"], []], "Fish4"]), 4)

    def test_deeply_nested_aquarium(self):
        self.assertEqual(count_fish([[[[[["Fish1"]]]]]]), 1)

    def test_aquarium_with_empty_and_full_subaquariums(self):
        self.assertEqual(count_fish([[], ["Fish1"], [], ["Fish2", ["Fish3"]], []]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 429
