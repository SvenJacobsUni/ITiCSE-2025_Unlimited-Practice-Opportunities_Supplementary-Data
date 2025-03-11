# Input
- Programming Concept: Functions as variables; Float; For loops
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Calculating Average Stress Level

In this task, you should implement a function that calculates the average stress level of a person over a week. The stress level is given as a list of floating point numbers (floats) for each day of the week.

Write a function named `average_stress_level(stress_level_list)`, which takes a list of floats as an argument and calculates and returns the average stress level.

Example call:
```python
stress_level = [3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]
print(average_stress_level(stress_level))  # Expected output: 3.9714285714285715
```

### Requirements:
1. The function should accept a list of floats as input.
2. The function should return the average stress level as a float.
3. Use a `for` loop to calculate the sum of the stress levels.
4. Calculate the average by dividing the sum by the number of days.

### Context:
A person's stress level can vary greatly and is an important indicator of mental health. By calculating the average stress level over a week, one can better understand how stressed a person is on average and whether stress management measures are necessary.

## Code Framework
```python
def average_stress_level(stress_level_list):
    # Insert code here
```

## Model Solution
```python
def average_stress_level(stress_level_list):
    return sum(stress_level_list) / len(stress_level_list)

stress_level = [3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]
print(average_stress_level(stress_level))
```

## Unit Tests
```python
import unittest
from main import average_stress_level

class TestAverageStressLevel(unittest.TestCase):
    def test_average(self):
        self.assertAlmostEqual(average_stress_level([3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]), 3.9714285714285715)

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            average_stress_level([])

    def test_single_element(self):
        self.assertEqual(average_stress_level([4.0]), 4.0)

    def test_negative_values(self):
        self.assertAlmostEqual(average_stress_level([-1.0, -2.0, -3.0]), -2.0)

    def test_mixed_values(self):
        self.assertAlmostEqual(average_stress_level([1.0, -1.0, 1.0, -1.0]), 0.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 606
