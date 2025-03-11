# Input
- Programming Concept: Float
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Calculating the Average Stress Level

Mental health is an important topic, and understanding stress levels can help improve well-being. In this task, you will write a function that calculates the average stress level of a person.

Write a function named `average_stress_level(stress_values)`, which takes a list of floating-point numbers (floats) as an argument. This list represents a person's daily stress levels over a certain period. The function should calculate and return the average stress level.

Example call:
```python
stress_values = [3.5, 4.0, 2.8, 5.0, 3.9]
print(average_stress_level(stress_values))  # Output: 3.84
```

Note: The output does not have to be exactly 3.84, as this is just an example.

## Code Framework
```python
def average_stress_level(stress_values):
    ## Insert code here
```

## Model Solution
```python
def average_stress_level(stress_values):
    return sum(stress_values) / len(stress_values)

stress_values = [3.5, 4.0, 2.8, 5.0, 3.9]
print(average_stress_level(stress_values))
```

## Unit Tests
```python
import unittest
from main import average_stress_level

class TestAverageStressLevel(unittest.TestCase):
    def test_average_stress_level_simple(self):
        self.assertAlmostEqual(average_stress_level([3.5, 4.0, 2.8, 5.0, 3.9]), 3.84, places=2)

    def test_average_stress_level_empty(self):
        with self.assertRaises(ZeroDivisionError):
            average_stress_level([])

    def test_average_stress_level_single_element(self):
        self.assertEqual(average_stress_level([4.2]), 4.2)

    def test_average_stress_level_negative_values(self):
        self.assertAlmostEqual(average_stress_level([-1.0, -2.0, -3.0]), -2.0, places=2)

    def test_average_stress_level_mixed_values(self):
        self.assertAlmostEqual(average_stress_level([1.0, -1.0, 1.0, -1.0]), 0.0, places=2)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 501
