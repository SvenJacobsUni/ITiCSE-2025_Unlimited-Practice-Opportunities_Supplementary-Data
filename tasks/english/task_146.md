# Input
- Programming Concept: Lists;Tuples
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise: Gardening with Lists and Tuples

Write a function named `plant_info(plant_list)`, which takes a list of tuples as an argument. Each tuple contains the name of a plant and the number of plants in the garden. The function should return a new list containing only the names of the plants that are present more than 5 times in the garden.

Example call:
```python
plant_list = [("Tomato", 10), ("Cucumber", 3), ("Carrot", 7), ("Lettuce", 2)]
print(plant_info(plant_list))
```

Expected output:
```
['Tomato', 'Carrot']
```

## Code Framework
```python
def plant_info(plant_list):
    ## Insert code here
```

## Model Solution
```python
def plant_info(plant_list):
    return [name for name, count in plant_list if count > 5]

plant_list = [("Tomato", 10), ("Cucumber", 3), ("Carrot", 7), ("Lettuce", 2)]
print(plant_info(plant_list))
```

## Unit Tests
```python
import unittest
from main import plant_info

class TestPlantInfo(unittest.TestCase):
    def test_more_than_five(self):
        self.assertEqual(plant_info([("Tomato", 10), ("Cucumber", 3), ("Carrot", 7), ("Lettuce", 2)]), ["Tomato", "Carrot"])

    def test_no_plants(self):
        self.assertEqual(plant_info([]), [])

    def test_all_less_than_five(self):
        self.assertEqual(plant_info([("Tomato", 1), ("Cucumber", 2), ("Carrot", 3), ("Lettuce", 4)]), [])

    def test_all_more_than_five(self):
        self.assertEqual(plant_info([("Tomato", 6), ("Cucumber", 7), ("Carrot", 8), ("Lettuce", 9)]), ["Tomato", "Cucumber", "Carrot", "Lettuce"])

    def test_exactly_five(self):
        self.assertEqual(plant_info([("Tomato", 5), ("Cucumber", 5), ("Carrot", 5), ("Lettuce", 5)]), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 578
