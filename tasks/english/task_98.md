# Input
- Programming Concept: Float
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise Task: Calculate Ingredient Quantities

Write a function named `calculate_ingredient_quantity(number_of_people)`, which calculates the required amount of an ingredient for a recipe. The recipe is designed for 4 people and needs 250.0 grams of flour. The function should calculate and return the required amount of flour for the given number of people.

Example call: `calculate_ingredient_quantity(2)` returns `125.0`.

## Code Framework
```python
def calculate_ingredient_quantity(number_of_people):
    ## Insert code here
```

## Model Solution
```python
def calculate_ingredient_quantity(number_of_people):
    return 250.0 * number_of_people / 4

print(calculate_ingredient_quantity(2))
```

## Unit Tests
```python
import unittest
from main import calculate_ingredient_quantity

class TestCalculateIngredientQuantity(unittest.TestCase):
    def test_two_people(self):
        self.assertEqual(calculate_ingredient_quantity(2), 125.0)

    def test_four_people(self):
        self.assertEqual(calculate_ingredient_quantity(4), 250.0)

    def test_eight_people(self):
        self.assertEqual(calculate_ingredient_quantity(8), 500.0)

    def test_zero_people(self):
        self.assertEqual(calculate_ingredient_quantity(0), 0.0)

    def test_half_person(self):
        self.assertEqual(calculate_ingredient_quantity(0.5), 31.25)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 516
