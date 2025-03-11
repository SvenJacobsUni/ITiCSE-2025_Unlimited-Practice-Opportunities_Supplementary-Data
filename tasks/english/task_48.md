# Input
- Programming Concept: String
- Context: Cooking

# Generated Task Components
## Task Description
### Practice Exercise: Recipe Description

Write a function named `recipe_description(recipe)` that formats a description of a recipe. The function should take a string `recipe` as input, which contains the ingredients and preparation steps. The function should format the string so that each ingredient and each preparation step appears on a new line. 

Example call:
```python
recipe = 'Ingredients: Flour, Sugar, Eggs, Milk. Preparation: Mix, Bake, Cool.'
print(recipe_description(recipe))
```

Expected output:
```
Ingredients:
Flour
Sugar
Eggs
Milk
Preparation:
Mix
Bake
Cool
```

## Code Framework
```python
def recipe_description(recipe):
    ## Insert code here
```

## Model Solution
```python
def recipe_description(recipe):
    ingredients, preparation = recipe.split('Preparation:')
    ingredients = ingredients.replace('Ingredients:', 'Ingredients:\n').replace(', ', '\n')
    preparation = 'Preparation:\n' + preparation.replace(', ', '\n')
    return ingredients + preparation

recipe = 'Ingredients: Flour, Sugar, Eggs, Milk. Preparation: Mix, Bake, Cool.'
print(recipe_description(recipe))
```

## Unit Tests
```python
import unittest

class TestRecipeDescription(unittest.TestCase):
    def test_simple_recipe(self):
        recipe = 'Ingredients: Flour, Sugar, Eggs, Milk. Preparation: Mix, Bake, Cool.'
        expected = 'Ingredients:\nFlour\nSugar\nEggs\nMilk\nPreparation:\nMix\nBake\nCool'
        self.assertEqual(recipe_description(recipe), expected)

    def test_empty_recipe(self):
        recipe = 'Ingredients: . Preparation: .'
        expected = 'Ingredients:\n\nPreparation:\n'
        self.assertEqual(recipe_description(recipe), expected)

    def test_only_ingredients(self):
        recipe = 'Ingredients: Flour, Sugar. Preparation: .'
        expected = 'Ingredients:\nFlour\nSugar\nPreparation:\n'
        self.assertEqual(recipe_description(recipe), expected)

    def test_only_preparation(self):
        recipe = 'Ingredients: . Preparation: Mix, Bake.'
        expected = 'Ingredients:\n\nPreparation:\nMix\nBake'
        self.assertEqual(recipe_description(recipe), expected)

    def test_complex_recipe(self):
        recipe = 'Ingredients: Flour, Sugar, Eggs, Milk, Butter, Salt. Preparation: Mix, Knead, Bake, Cool, Serve.'
        expected = 'Ingredients:\nFlour\nSugar\nEggs\nMilk\nButter\nSalt\nPreparation:\nMix\nKnead\nBake\nCool\nServe'
        self.assertEqual(recipe_description(recipe), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 466
