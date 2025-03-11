# Input
- Programming Concept: Integer
- Context: Cooking

# Generated Task Components
## Task Description
### Practice Task: Calculate Ingredients for a Recipe

Write a function named `calculate_ingredients(number_of_people)` that calculates the required amount of ingredients for a recipe. The recipe is designed for 4 people and requires the following ingredients:

- 200 grams of flour
- 100 grams of sugar
- 2 eggs

The function should adjust the amounts of the ingredients according to the number of people and return a message with the calculated amounts. Example call: `calculate_ingredients(2)` returns "For 2 people, you need: 100 grams of flour, 50 grams of sugar, 1 egg."


## Code Framework
```python
def calculate_ingredients(number_of_people):
    ## Insert code here

```

## Model Solution
```python
def calculate_ingredients(number_of_people):
    flour = 200 * number_of_people / 4
    sugar = 100 * number_of_people / 4
    eggs = 2 * number_of_people / 4
    return f"For {number_of_people} people, you need: {flour} grams of flour, {sugar} grams of sugar, {eggs} eggs."

calculate_ingredients(2)

```

## Unit Tests
```python
import unittest
from main import calculate_ingredients

class TestCalculateIngredients(unittest.TestCase):
    def test_two_people(self):
        self.assertEqual(calculate_ingredients(2), "For 2 people, you need: 100.0 grams of flour, 50.0 grams of sugar, 1.0 egg.")

    def test_four_people(self):
        self.assertEqual(calculate_ingredients(4), "For 4 people, you need: 200.0 grams of flour, 100.0 grams of sugar, 2.0 eggs.")

    def test_zero_people(self):
        self.assertEqual(calculate_ingredients(0), "For 0 people, you need: 0.0 grams of flour, 0.0 grams of sugar, 0.0 eggs.")

    def test_eight_people(self):
        self.assertEqual(calculate_ingredients(8), "For 8 people, you need: 400.0 grams of flour, 200.0 grams of sugar, 4.0 eggs.")

    def test_negative_people(self):
        self.assertEqual(calculate_ingredients(-2), "For -2 people, you need: -100.0 grams of flour, -50.0 grams of sugar, -1.0 egg.")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 478
