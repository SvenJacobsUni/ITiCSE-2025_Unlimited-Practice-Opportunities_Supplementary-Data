# Input
- Programming Concept: Float; Lists
- Context: Animals

# Generated Task Components
## Task Description
### Practice Task: Average Weight of Animals

Write a function named `average_weight(animals)`, which takes a list of floats as an argument. This list represents the weights of different animals in kilograms. The function should calculate and return the average weight of the animals.

Example call:
```python
weights = [4.5, 7.2, 3.8, 5.0, 6.1]
print(average_weight(weights))  # Output: 5.32
```

Note: The output may vary slightly due to rounding differences.

## Code Framework
```python
def average_weight(animals):
    ## Insert code here
```

## Model Solution
```python
def average_weight(animals):
    return sum(animals) / len(animals)

weights = [4.5, 7.2, 3.8, 5.0, 6.1]
print(average_weight(weights))
```

## Unit Tests
```python
import unittest
from main import average_weight

class TestAverageWeight(unittest.TestCase):
    def test_average(self):
        self.assertAlmostEqual(average_weight([4.5, 7.2, 3.8, 5.0, 6.1]), 5.32, places=2)

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            average_weight([])

    def test_single_element(self):
        self.assertEqual(average_weight([5.0]), 5.0)

    def test_integers(self):
        self.assertEqual(average_weight([1, 2, 3, 4, 5]), 3.0)

    def test_mixed_numbers(self):
        self.assertAlmostEqual(average_weight([1.5, 2.5, 3.5, 4.5, 5.5]), 3.5, places=2)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 558
