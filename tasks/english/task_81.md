# Input
- Programming Concept: Tuples
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise: Gardening with Tuples

Write a function named `plant_info(plant)`, which returns information about different plants in a garden. The information about the plants should be stored in a tuple. Each tuple should contain the name of the plant, the required amount of water (in liters per week), and the preferred sunlight exposure (e.g. "Full sun", "Partial shade", "Shade").

The function should return a tuple with the information of the given plant. If the plant is not present in the garden, the function should return `None`.

Example calls:
```python
plant_info("Tomato")  # could return ("Tomato", 5, "Full sun")
plant_info("Lavender")  # could return ("Lavender", 2, "Full sun")
plant_info("Unknown")  # should return None
```

## Code Framework
```python
def plant_info(plant):
    ## Insert code here
```

## Model Solution
```python
def plant_info(plant):
    garden = {
        "Tomato": ("Tomato", 5, "Full sun"),
        "Lavender": ("Lavender", 2, "Full sun"),
        "Basil": ("Basil", 3, "Partial shade")
    }
    return garden.get(plant)

print(plant_info("Tomato"))
print(plant_info("Lavender"))
print(plant_info("Unknown"))
```

## Unit Tests
```python
import unittest

class TestPlantInfo(unittest.TestCase):
    def test_tomato(self):
        self.assertEqual(plant_info("Tomato"), ("Tomato", 5, "Full sun"))

    def test_lavender(self):
        self.assertEqual(plant_info("Lavender"), ("Lavender", 2, "Full sun"))

    def test_basil(self):
        self.assertEqual(plant_info("Basil"), ("Basil", 3, "Partial shade"))

    def test_unknown(self):
        self.assertIsNone(plant_info("Unknown"))

    def test_empty_string(self):
        self.assertIsNone(plant_info(""))

    def test_none(self):
        self.assertIsNone(plant_info(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 499
