# Input
- Programming Concept: Float
- Context: Animals

# Generated Task Components
## Task Description
### Practice Task: Animal Weight in Kilograms

Write a function called `weight_in_kg(weight_pounds)`, which takes the weight of an animal in pounds (float) as an argument and returns the weight in kilograms (float). Note that 1 pound is approximately 0.453592 kilograms.

Example call:
```python
weight_in_kg(10.0)
```
should return approximately `4.53592`.

## Code Framework
```python
def weight_in_kg(weight_pounds):
    ## Insert code here
```

## Model Solution
```python
def weight_in_kg(weight_pounds):
    return weight_pounds * 0.453592

print(weight_in_kg(10.0))
```

## Unit Tests
```python
import unittest

from main import weight_in_kg

class TestWeightInKg(unittest.TestCase):
    def test_ten_pounds(self):
        self.assertAlmostEqual(weight_in_kg(10.0), 4.53592, places=5)

    def test_zero_pounds(self):
        self.assertEqual(weight_in_kg(0.0), 0.0)

    def test_one_pound(self):
        self.assertAlmostEqual(weight_in_kg(1.0), 0.453592, places=5)

    def test_negative_weight(self):
        self.assertAlmostEqual(weight_in_kg(-5.0), -2.26796, places=5)

    def test_large_weight(self):
        self.assertAlmostEqual(weight_in_kg(1000.0), 453.592, places=3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 468
