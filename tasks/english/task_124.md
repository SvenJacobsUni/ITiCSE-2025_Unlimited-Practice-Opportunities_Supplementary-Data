# Input
- Programming Concept: Functions as variables; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise Task: Aquarium Temperature Control

Write a function named `check_temperature(temperature)` that verifies if the temperature in an aquarium is within the optimal range. The optimal temperature range for the aquarium is between 22 and 28 degrees Celsius (inclusive). The function should return `True` if the temperature is within the optimal range, and `False` if it is outside this range.

Additionally, implement a function `is_too_hot_or_too_cold(temperature)` that checks if the temperature is either too hot (above 28 degrees) or too cold (below 22 degrees). This function should return `True` if the temperature is outside the optimal range, and `False` if it is within the range.

Example calls:
- `check_temperature(25)` returns `True`.
- `check_temperature(30)` returns `False`.
- `is_too_hot_or_too_cold(18)` returns `True`.
- `is_too_hot_or_too_cold(24)` returns `False`.

## Code Framework
```python
def check_temperature(temperature):
    ## Insert code here

def is_too_hot_or_too_cold(temperature):
    ## Insert code here

```

## Model Solution
```python
def check_temperature(temperature):
    return 22 <= temperature <= 28


def is_too_hot_or_too_cold(temperature):
    return temperature < 22 or temperature > 28

# Example calls
print(check_temperature(25))  # True
print(check_temperature(30))  # False
print(is_too_hot_or_too_cold(18))  # True
print(is_too_hot_or_too_cold(24))  # False

```

## Unit Tests
```python
import unittest

from main import check_temperature, is_too_hot_or_too_cold

class TestAquariumTemperature(unittest.TestCase):
    def test_check_temperature_optimal(self):
        self.assertTrue(check_temperature(25))

    def test_check_temperature_too_hot(self):
        self.assertFalse(check_temperature(30))

    def test_check_temperature_too_cold(self):
        self.assertFalse(check_temperature(18))

    def test_is_too_hot_or_too_cold_too_hot(self):
        self.assertTrue(is_too_hot_or_too_cold(30))

    def test_is_too_hot_or_too_cold_too_cold(self):
        self.assertTrue(is_too_hot_or_too_cold(18))

    def test_is_too_hot_or_too_cold_optimal(self):
        self.assertFalse(is_too_hot_or_too_cold(24))

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 556
