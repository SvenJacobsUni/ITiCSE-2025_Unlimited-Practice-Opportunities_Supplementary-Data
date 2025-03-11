# Input
- Programming Concept: Lists
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Ingredient List for a Recipe

Write a function named `add_ingredient(ingredient_list, new_ingredient)`, which receives a list of ingredients and a new ingredient as parameters. The function should add the new ingredient to the ingredient list and return the updated list.

Example call:
```python
ingredients = ["Flour", "Sugar", "Eggs"]
new_ingredient = "Milk"
print(add_ingredient(ingredients, new_ingredient))
```

Expected Output:
```
["Flour", "Sugar", "Eggs", "Milk"]
```

## Code Framework
```python
def add_ingredient(ingredient_list, new_ingredient):
    ## Insert code here
```

## Model Solution
```python
def add_ingredient(ingredient_list, new_ingredient):
    ingredient_list.append(new_ingredient)
    return ingredient_list

ingredients = ["Flour", "Sugar", "Eggs"]
new_ingredient = "Milk"
print(add_ingredient(ingredients, new_ingredient))
```

## Unit Tests
```python
import unittest
from main import add_ingredient

class TestAddIngredient(unittest.TestCase):
    def test_simple_ingredient(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs"], "Milk"), ["Flour", "Sugar", "Eggs", "Milk"])

    def test_empty_list(self):
        self.assertEqual(add_ingredient([], "Milk"), ["Milk"])

    def test_multiple_ingredients(self):
        self.assertEqual(add_ingredient(["Flour"], "Sugar"), ["Flour", "Sugar"])

    def test_duplicate_ingredient(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs"], "Sugar"), ["Flour", "Sugar", "Eggs", "Sugar"])

    def test_ingredient_as_number(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs"], 123), ["Flour", "Sugar", "Eggs", 123])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 448
