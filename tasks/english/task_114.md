# Input
- Programming Concept: While loops; Higher-order functions
- Context: Cooking

# Generated Task Components
## Task Description
### Practice Task: Cooking Recipe Counter

Write a function named `count_ingredients(recipe, criterion)` that receives a list of ingredients (`recipe`) and a function (`criterion`) as parameters. The function should count the number of ingredients in the recipe that meet the criterion. Use a `while` loop to iterate through the ingredients list.

Example call:
```python
def is_vegetable(ingredient):
    vegetables = ["Carrot", "Tomato", "Cucumber", "Pepper"]
    return ingredient in vegetables

recipe = ["Carrot", "Chicken", "Tomato", "Rice", "Pepper"]
print(count_ingredients(recipe, is_vegetable))  # Output: 3
```

In this example, the function `is_vegetable` is used as the criterion to count the number of vegetable ingredients in the recipe.

## Code Framework
```python
def count_ingredients(recipe, criterion):
    ## Insert code here
```

## Model Solution
```python
def count_ingredients(recipe, criterion):
    count, i = 0, 0
    while i < len(recipe):
        if criterion(recipe[i]):
            count += 1
        i += 1
    return count

def is_vegetable(ingredient):
    vegetables = ["Carrot", "Tomato", "Cucumber", "Pepper"]
    return ingredient in vegetables

recipe = ["Carrot", "Chicken", "Tomato", "Rice", "Pepper"]
print(count_ingredients(recipe, is_vegetable))  # Output: 3
```

## Unit Tests
```python
import unittest

from main import count_ingredients

def is_vegetable(ingredient):
    vegetables = ["Carrot", "Tomato", "Cucumber", "Pepper"]
    return ingredient in vegetables

def is_meat(ingredient):
    meat = ["Chicken", "Beef", "Pork"]
    return ingredient in meat

class TestCountIngredients(unittest.TestCase):
    def test_vegetables(self):
        recipe = ["Carrot", "Chicken", "Tomato", "Rice", "Pepper"]
        self.assertEqual(count_ingredients(recipe, is_vegetable), 3)

    def test_meat(self):
        recipe = ["Carrot", "Chicken", "Tomato", "Rice", "Pepper"]
        self.assertEqual(count_ingredients(recipe, is_meat), 1)

    def test_empty_recipe(self):
        recipe = []
        self.assertEqual(count_ingredients(recipe, is_vegetable), 0)

    def test_no_criterion_met(self):
        recipe = ["Rice", "Noodles", "Potatoes"]
        self.assertEqual(count_ingredients(recipe, is_vegetable), 0)

    def test_all_criteria_met(self):
        recipe = ["Carrot", "Tomato", "Cucumber", "Pepper"]
        self.assertEqual(count_ingredients(recipe, is_vegetable), 4)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 546
