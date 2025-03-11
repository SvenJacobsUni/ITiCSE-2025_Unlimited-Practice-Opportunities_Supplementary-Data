# Input
- Programming Concept: If-Else statements; For loops
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Recipe Selection Based on Ingredients

Write a function named `recipe_selection(ingredients)` that receives a list of ingredients as an argument and selects a recipe based on the available ingredients. The function should consider the following recipes:

1. **Pasta with Tomato Sauce**:
   - Ingredients: Pasta, Tomatoes, Garlic
2. **Vegetable Stir Fry**:
   - Ingredients: Bell Pepper, Zucchini, Onions
3. **Fruit Salad**:
   - Ingredients: Apple, Banana, Orange

The function should check if all the necessary ingredients for a recipe are included in the given list. If multiple recipes are possible, the first fitting recipe should be selected. If no recipe is possible, the function should return "No suitable recipe found".

Example call:
```python
ingredients = ["Pasta", "Tomatoes", "Garlic", "Apple"]
print(recipe_selection(ingredients))
```

Expected output:
```
Pasta with Tomato Sauce
```

## Code Framework
```python
def recipe_selection(ingredients):
    ## Insert code here
```

## Model Solution
```python
def recipe_selection(ingredients):
    recipes = {
        "Pasta with Tomato Sauce": {"Pasta", "Tomatoes", "Garlic"},
        "Vegetable Stir Fry": {"Bell Pepper", "Zucchini", "Onions"},
        "Fruit Salad": {"Apple", "Banana", "Orange"}
    }
    for recipe, required_ingredients in recipes.items():
        if required_ingredients.issubset(ingredients):
            return recipe
    return "No suitable recipe found"

ingredients = ["Pasta", "Tomatoes", "Garlic", "Apple"]
print(recipe_selection(ingredients))
```

## Unit Tests
```python
import unittest
from main import recipe_selection

class TestRecipeSelection(unittest.TestCase):
    def test_pasta_with_tomato_sauce(self):
        self.assertEqual(recipe_selection(["Pasta", "Tomatoes", "Garlic"]), "Pasta with Tomato Sauce")

    def test_vegetable_stir_fry(self):
        self.assertEqual(recipe_selection(["Bell Pepper", "Zucchini", "Onions"]), "Vegetable Stir Fry")

    def test_fruit_salad(self):
        self.assertEqual(recipe_selection(["Apple", "Banana", "Orange"]), "Fruit Salad")

    def test_multiple_recipes(self):
        self.assertEqual(recipe_selection(["Pasta", "Tomatoes", "Garlic", "Bell Pepper", "Zucchini", "Onions"]), "Pasta with Tomato Sauce")

    def test_no_suitable_recipes(self):
        self.assertEqual(recipe_selection(["Rice", "Chicken", "Soy sauce"]), "No suitable recipe found")

    def test_empty_ingredients_list(self):
        self.assertEqual(recipe_selection([]), "No suitable recipe found")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 557
