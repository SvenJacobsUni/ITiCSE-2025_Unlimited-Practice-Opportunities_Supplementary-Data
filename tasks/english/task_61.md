# Input
- Programming Concept: Tuples
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise Task: Gardening with Tuples

Write a function named `plant_info(plant)` that returns information about different plants in a garden. The information about the plants should be stored in a tuple. Each tuple should contain the name of the plant, the required amount of water (in liters per week), and the preferred amount of sunlight (in hours per day).

The function should return a tuple with the information of the given plant. If the plant is not present in the garden, the function should return `None`.

Example calls:
- `plant_info("Tomato")` could return `("Tomato", 5, 8)`.
- `plant_info("Rose")` could return `("Rose", 3, 6)`.
- `plant_info("Cactus")` could return `None` if "Cactus" is not present in the garden.

## Code Framework
```python
def plant_info(plant):
    ## Insert code here
```

## Model Solution
```python
def plant_info(plant):
    garden = {
        "Tomato": ("Tomato", 5, 8),
        "Rose": ("Rose", 3, 6),
        "Basil": ("Basil", 2, 6)
    }
    return garden.get(plant)

# Example calls
print(plant_info("Tomato"))
print(plant_info("Rose"))
print(plant_info("Cactus"))
```

## Unit Tests
```python
import unittest
from main import plant_info

class TestPlantInfo(unittest.TestCase):
    def test_tomato(self):
        self.assertEqual(plant_info("Tomato"), ("Tomato", 5, 8))

    def test_rose(self):
        self.assertEqual(plant_info("Rose"), ("Rose", 3, 6))

    def test_basil(self):
        self.assertEqual(plant_info("Basil"), ("Basil", 2, 6))

    def test_cactus(self):
        self.assertIsNone(plant_info("Cactus"))

    def test_empty_string(self):
        self.assertIsNone(plant_info(""))

    def test_none(self):
        self.assertIsNone(plant_info(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 479
