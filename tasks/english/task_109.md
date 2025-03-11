# Input
- Programming Concept: Functions as variables; Operations with numbers
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Functions as Variables and Operations with Numbers in the context of 'Fishing'

Write a function named `calculate_fish_weight(fish_weight_list)`, which takes a list of weights (in kilograms) of caught fish and calculates the total weight of the fish. The function should return the total weight of the fish.

Additionally, implement a second function `average_weight(fish_weight_list)` that calculates and returns the average weight of the fish.

Example calls:
```python
fish_weight_list = [2.5, 3.0, 1.2, 4.8]
total_weight = calculate_fish_weight(fish_weight_list)
print(total_weight)  # Output: 11.5

average = average_weight(fish_weight_list)
print(average)  # Output: 2.875
```

Implement both functions so that they operate correctly and deliver the expected results.

## Code Framework
```python
def calculate_fish_weight(fish_weight_list):
    ## Insert code here

def average_weight(fish_weight_list):
    ## Insert code here

```

## Model Solution
```python
def calculate_fish_weight(fish_weight_list):
    return sum(fish_weight_list)

def average_weight(fish_weight_list):
    return sum(fish_weight_list) / len(fish_weight_list)

fish_weight_list = [2.5, 3.0, 1.2, 4.8]
total_weight = calculate_fish_weight(fish_weight_list)
print(total_weight)  # Output: 11.5

average = average_weight(fish_weight_list)
print(average)  # Output: 2.875
```

## Unit Tests
```python
import unittest

from main import calculate_fish_weight, average_weight

class TestCalculateFishWeight(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(calculate_fish_weight([2.5, 3.0, 1.2, 4.8]), 11.5)

    def test_empty_list(self):
        self.assertEqual(calculate_fish_weight([]), 0)

    def test_single_element(self):
        self.assertEqual(calculate_fish_weight([5.0]), 5.0)

    def test_negative_weight(self):
        self.assertEqual(calculate_fish_weight([2.5, -1.0, 3.0]), 4.5)

class TestAverageWeight(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(average_weight([2.5, 3.0, 1.2, 4.8]), 2.875)

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            average_weight([])

    def test_single_element(self):
        self.assertEqual(average_weight([5.0]), 5.0)

    def test_negative_weight(self):
        self.assertEqual(average_weight([2.5, -1.0, 3.0]), 1.5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 541
