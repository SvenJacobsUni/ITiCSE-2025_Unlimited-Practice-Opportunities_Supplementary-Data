# Input
- Programming Concept: Float;Operations with numbers;Control structures (==, !=, <, >, <=, >=, or, and, not)
- Context: Pets

# Generated Task Components
## Task Description
### Exercise Task: Pet Weight Control

Write a function named `weight_control(weight)` that takes the weight of a pet (in kilograms) as a float and returns an appropriate message with `return`. The function should decide whether the pet is underweight, normal weight, or overweight based on its weight.

- If the weight is less than 2.0 kg, the message "The pet is underweight." should be returned.
- If the weight is between 2.0 kg and 5.0 kg (inclusive), the message "The pet has a normal weight." should be returned.
- If the weight is greater than 5.0 kg, the message "The pet is overweight." should be returned.

Example Calls:
- `weight_control(1.5)` returns "The pet is underweight."
- `weight_control(3.0)` returns "The pet has a normal weight."
- `weight_control(6.0)` returns "The pet is overweight."

## Code Framework
```python
def weight_control(weight):
    ## Insert code here
```

## Model Solution
```python
def weight_control(weight):
    if weight < 2.0:
        return "The pet is underweight."
    elif weight <= 5.0:
        return "The pet has a normal weight."
    else:
        return "The pet is overweight."

# Example calls
print(weight_control(1.5))
print(weight_control(3.0))
print(weight_control(6.0))
```

## Unit Tests
```python
import unittest
from main import weight_control

class TestWeightControl(unittest.TestCase):
    def test_underweight(self):
        self.assertEqual(weight_control(1.5), "The pet is underweight.")

    def test_normal_weight_lower_bound(self):
        self.assertEqual(weight_control(2.0), "The pet has a normal weight.")

    def test_normal_weight_middle(self):
        self.assertEqual(weight_control(3.0), "The pet has a normal weight.")

    def test_normal_weight_upper_bound(self):
        self.assertEqual(weight_control(5.0), "The pet has a normal weight.")

    def test_overweight(self):
        self.assertEqual(weight_control(6.0), "The pet is overweight.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 621
