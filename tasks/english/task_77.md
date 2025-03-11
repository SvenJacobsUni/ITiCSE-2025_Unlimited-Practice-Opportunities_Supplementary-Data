# Input
- Programming Concept: Boolean and None
- Context: Aquarium

# Generated Task Components
## Task Description
### Practice Task: Aquarium Check

Write a function called `is_aquarium_full(water_level, capacity)` that checks if an aquarium is full. The function should take two parameters: `water_level` (in liters) and `capacity` (in liters). The function should return `True` if the aquarium is full, `False` if it is not full, and `None` if the water level is greater than the capacity.

Example Calls:
- `is_aquarium_full(50, 100)` returns `False`.
- `is_aquarium_full(100, 100)` returns `True`.
- `is_aquarium_full(150, 100)` returns `None`.

## Code Framework
```python
def is_aquarium_full(water_level, capacity):
    ## Insert code here
```

## Model Solution
```python
def is_aquarium_full(water_level, capacity):
    if water_level > capacity:
        return None
    return water_level == capacity

# Example Calls
print(is_aquarium_full(50, 100))  # False
print(is_aquarium_full(100, 100)) # True
print(is_aquarium_full(150, 100)) # None
```

## Unit Tests
```python
import unittest

class TestIsAquariumFull(unittest.TestCase):
    def test_aquarium_not_full(self):
        self.assertEqual(is_aquarium_full(50, 100), False)

    def test_aquarium_full(self):
        self.assertEqual(is_aquarium_full(100, 100), True)

    def test_aquarium_overfilled(self):
        self.assertEqual(is_aquarium_full(150, 100), None)

    def test_aquarium_empty(self):
        self.assertEqual(is_aquarium_full(0, 100), False)

    def test_aquarium_exactly_full(self):
        self.assertEqual(is_aquarium_full(100, 100), True)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 495
