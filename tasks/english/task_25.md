# Input
- Programming Concept: While loops
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise: Gardening with While Loops

Write a function named `water_plant(plants)` that takes a list of plants as an argument. Each plant in the list has a water level represented by a number. The function should water each plant until its water level reaches at least 5. The water level of each plant increases by 1 with each watering. The function should return the number of watering operations needed for each plant.

Example call:
```python
plants = [2, 4, 1]
print(water_plant(plants))  # Output: [3, 1, 4]
```

In this example, the first plant needs 3 waterings, the second plant needs 1 watering, and the third plant needs 4 waterings to reach a water level of at least 5.

## Code Framework
```python
def water_plant(plants):
    ## Insert code here
```

## Model Solution
```python
def water_plant(plants):
    return [max(0, 5 - plant) for plant in plants]

plants = [2, 4, 1]
print(water_plant(plants))
```

## Unit Tests
```python
import unittest
from main import water_plant

class TestWaterPlant(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(water_plant([2, 4, 1]), [3, 1, 4])

    def test_all_plants_already_watered_sufficiently(self):
        self.assertEqual(water_plant([5, 6, 7]), [0, 0, 0])

    def test_all_plants_need_watering(self):
        self.assertEqual(water_plant([0, 0, 0]), [5, 5, 5])

    def test_empty_list(self):
        self.assertEqual(water_plant([]), [])

    def test_edge_conditions(self):
        self.assertEqual(water_plant([4, 5, 6]), [1, 0, 0])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 443
