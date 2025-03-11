# Input
- Programming Concept: For loops; Control structures (==, !=, <, >, <=, >=, or, and, not); If-Else statements
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Ingredient Check for a Recipe

Write a function named `check_ingredients(ingredient_list)`, which receives a list of ingredients as an argument. The function should check whether all necessary ingredients for a particular recipe are present. The recipe requires the following ingredients: 'flour', 'eggs', 'milk', 'sugar', and 'butter'.

The function should:
1. Check if each required ingredient is included in the provided list.
2. Return a message indicating whether all ingredients are present or which ingredients are missing.

Example call:
```python
check_ingredients(['flour', 'eggs', 'milk', 'sugar', 'butter'])
```
should return:
```python
'All ingredients are present.'
```

Another example call:
```python
check_ingredients(['flour', 'eggs', 'milk'])
```
should return:
```python
'The following ingredients are missing: sugar, butter'
```

## Code Framework
```python
def check_ingredients(ingredient_list):
    ## Insert code here
```

## Model Solution
```python
def check_ingredients(ingredient_list):
    recipe_ingredients = {'flour', 'eggs', 'milk', 'sugar', 'butter'}
    missing_ingredients = recipe_ingredients - set(ingredient_list)
    if missing_ingredients:
        return f'The following ingredients are missing: {', '.join(missing_ingredients)}'
    else:
        return 'All ingredients are present.'

print(check_ingredients(['flour', 'eggs', 'milk', 'sugar', 'butter']))
print(check_ingredients(['flour', 'eggs', 'milk']))
```

## Unit Tests
```python
import unittest

from main import check_ingredients

class TestCheckIngredients(unittest.TestCase):
    def test_all_ingredients_present(self):
        self.assertEqual(check_ingredients(['flour', 'eggs', 'milk', 'sugar', 'butter']), 'All ingredients are present.')

    def test_some_ingredients_missing(self):
        self.assertEqual(check_ingredients(['flour', 'eggs', 'milk']), 'The following ingredients are missing: sugar, butter')

    def test_all_ingredients_missing(self):
        self.assertEqual(check_ingredients([]), 'The following ingredients are missing: flour, eggs, milk, sugar, butter')

    def test_one_ingredient_missing(self):
        self.assertEqual(check_ingredients(['flour', 'eggs', 'milk', 'sugar']), 'The following ingredient is missing: butter')

    def test_duplicate_ingredients(self):
        self.assertEqual(check_ingredients(['flour', 'eggs', 'milk', 'sugar', 'butter', 'butter']), 'All ingredients are present.')

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 625
