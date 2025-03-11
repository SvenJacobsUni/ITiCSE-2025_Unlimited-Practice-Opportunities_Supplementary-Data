# Input
- Programming Concept: Operations with numbers
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise Task: Operations with numbers in the context 'Aquarium'

Write a function named `calculate_water_volume(length, width, height)` that calculates the volume of a rectangular aquarium in liters. The function should take the length, width, and height of the aquarium in centimeters as parameters and return the volume in liters.

Note: 1 liter equals 1000 cubic centimeters.

Example call:
```python
volume = calculate_water_volume(100, 50, 40)
print(volume)  # Output: 200.0
```

In this example, the aquarium has a length of 100 cm, a width of 50 cm, and a height of 40 cm. The calculated volume is 200 liters.

## Code Framework
```python
def calculate_water_volume(length, width, height):
    ## Insert code here
```

## Model Solution
```python
def calculate_water_volume(length, width, height):
    return (length * width * height) / 1000

volume = calculate_water_volume(100, 50, 40)
print(volume)
```

## Unit Tests
```python
import unittest
from main import calculate_water_volume

class TestCalculateWaterVolume(unittest.TestCase):
    def test_standard_case(self):
        self.assertEqual(calculate_water_volume(100, 50, 40), 200.0)

    def test_zero_volume(self):
        self.assertEqual(calculate_water_volume(0, 50, 40), 0.0)
        self.assertEqual(calculate_water_volume(100, 0, 40), 0.0)
        self.assertEqual(calculate_water_volume(100, 50, 0), 0.0)

    def test_one_liter(self):
        self.assertEqual(calculate_water_volume(10, 10, 10), 1.0)

    def test_large_values(self):
        self.assertEqual(calculate_water_volume(1000, 1000, 1000), 1000000.0)

    def test_small_values(self):
        self.assertAlmostEqual(calculate_water_volume(1, 1, 1), 0.001)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 510
