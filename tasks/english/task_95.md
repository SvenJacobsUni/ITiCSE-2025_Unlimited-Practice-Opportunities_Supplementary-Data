# Input
- Programming Concept: Higher-order functions
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise: Higher-order Functions in Gardening

Write a function called `manage_plants(plant_list, function)` that takes a list of plants and a function as arguments. The function `manage_plants` should apply the given function to each plant in the list and return the results in a new list.

Example call:
```python
def describe_plant(plant):
    return f"The plant {plant} grows well in the garden."

plants = ["Tomato", "Cucumber", "Zucchini"]
results = manage_plants(plants, describe_plant)
print(results)
```

Expected output:
```
['The plant Tomato grows well in the garden.', 'The plant Cucumber grows well in the garden.', 'The plant Zucchini grows well in the garden.']
```

Implement the function `manage_plants` so it applies the passed function to each plant in the list and returns the results in a new list.

## Code Framework
```python
def manage_plants(plant_list, function):
    ## Insert code here
```

## Model Solution
```python
def manage_plants(plant_list, function):
    return [function(plant) for plant in plant_list]

def describe_plant(plant):
    return f"The plant {plant} grows well in the garden."

plants = ["Tomato", "Cucumber", "Zucchini"]
results = manage_plants(plants, describe_plant)
print(results)
```

## Unit Tests
```python
import unittest
from main import manage_plants

def describe_plant(plant):
    return f"The plant {plant} grows well in the garden."

class TestManagePlants(unittest.TestCase):
    def test_simple_list(self):
        plants = ["Tomato", "Cucumber", "Zucchini"]
        expected = [
            "The plant Tomato grows well in the garden.",
            "The plant Cucumber grows well in the garden.",
            "The plant Zucchini grows well in the garden."
        ]
        self.assertEqual(manage_plants(plants, describe_plant), expected)

    def test_empty_list(self):
        plants = []
        expected = []
        self.assertEqual(manage_plants(plants, describe_plant), expected)

    def test_single_plant(self):
        plants = ["Tomato"]
        expected = ["The plant Tomato grows well in the garden."]
        self.assertEqual(manage_plants(plants, describe_plant), expected)

    def test_various_plants(self):
        plants = ["Tomato", "Cucumber", "Zucchini", "Pepper"]
        expected = [
            "The plant Tomato grows well in the garden.",
            "The plant Cucumber grows well in the garden.",
            "The plant Zucchini grows well in the garden.",
            "The plant Pepper grows well in the garden."
        ]
        self.assertEqual(manage_plants(plants, describe_plant), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 513
