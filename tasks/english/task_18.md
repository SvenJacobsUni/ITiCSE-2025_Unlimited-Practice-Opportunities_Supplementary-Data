# Input
- Programming Concept: Integer
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise: Counting Fish in the Aquarium

Write a function named `count_fish(fish_count)`, which counts the number of fish in an aquarium and returns a corresponding message. The function should take an integer value `fish_count` as a parameter and return a message in the form "There are [fish_count] fish in the aquarium."

Example call:
```python
print(count_fish(10))
```

Expected output:
```
There are 10 fish in the aquarium.
```

## Code Framework
```python
def count_fish(fish_count):
    ## Insert code here
```

## Model Solution
```python
def count_fish(fish_count):
    return f"There are {fish_count} fish in the aquarium."

print(count_fish(10))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_ten_fish(self):
        self.assertEqual(count_fish(10), "There are 10 fish in the aquarium.")

    def test_zero_fish(self):
        self.assertEqual(count_fish(0), "There are 0 fish in the aquarium.")

    def test_one_fish(self):
        self.assertEqual(count_fish(1), "There is 1 fish in the aquarium.")

    def test_negative_fish(self):
        self.assertEqual(count_fish(-5), "There are -5 fish in the aquarium.")

    def test_large_number_of_fish(self):
        self.assertEqual(count_fish(1000), "There are 1000 fish in the aquarium.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 436
