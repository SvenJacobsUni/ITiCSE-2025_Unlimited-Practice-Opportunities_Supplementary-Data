# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Recipe Selection Based on Ingredients

Write a function called `recipe_selection(ingredients)` that decides which recipe can be cooked based on a list of ingredients. The function should consider the following recipes:

- **Pasta**: If both 'Pasta' and 'Tomato Sauce' are in the ingredients list.
- **Salad**: If both 'Salad' and 'Tomatoes' are in the ingredients list.
- **Omelette**: If both 'Eggs' and 'Milk' are in the ingredients list.

The function should return the name of the recipe as a string that can be cooked. If none of the ingredient combinations are present, the function should return 'No Recipe Found'.

Example calls:

```python
print(recipe_selection(['Pasta', 'Tomato Sauce', 'Cheese']))  # Output: 'Pasta'
print(recipe_selection(['Salad', 'Tomatoes', 'Cucumber']))    # Output: 'Salad'
print(recipe_selection(['Eggs', 'Milk', 'Cheese']))           # Output: 'Omelette'
print(recipe_selection(['Bread', 'Butter']))                  # Output: 'No Recipe Found'
```

## Code Framework
```python
def recipe_selection(ingredients):
    ## Insert code here
```

## Model Solution
```python
def recipe_selection(ingredients):
    if 'Pasta' in ingredients and 'Tomato Sauce' in ingredients:
        return 'Pasta'
    elif 'Salad' in ingredients and 'Tomatoes' in ingredients:
        return 'Salad'
    elif 'Eggs' in ingredients and 'Milk' in ingredients:
        return 'Omelette'
    return 'No Recipe Found'

print(recipe_selection(['Pasta', 'Tomato Sauce', 'Cheese']))
print(recipe_selection(['Salad', 'Tomatoes', 'Cucumber']))
print(recipe_selection(['Eggs', 'Milk', 'Cheese']))
print(recipe_selection(['Bread', 'Butter']))
```

## Unit Tests
```python
import unittest
from main import recipe_selection

class TestRecipeSelection(unittest.TestCase):
    def test_pasta(self):
        self.assertEqual(recipe_selection(['Pasta', 'Tomato Sauce', 'Cheese']), 'Pasta')

    def test_salad(self):
        self.assertEqual(recipe_selection(['Salad', 'Tomatoes', 'Cucumber']), 'Salad')

    def test_omelette(self):
        self.assertEqual(recipe_selection(['Eggs', 'Milk', 'Cheese']), 'Omelette')

    def test_no_recipe(self):
        self.assertEqual(recipe_selection(['Bread', 'Butter']), 'No Recipe Found')

    def test_empty_list(self):
        self.assertEqual(recipe_selection([]), 'No Recipe Found')

    def test_incomplete_ingredients(self):
        self.assertEqual(recipe_selection(['Pasta']), 'No Recipe Found')
        self.assertEqual(recipe_selection(['Tomato Sauce']), 'No Recipe Found')
        self.assertEqual(recipe_selection(['Salad']), 'No Recipe Found')
        self.assertEqual(recipe_selection(['Tomatoes']), 'No Recipe Found')
        self.assertEqual(recipe_selection(['Eggs']), 'No Recipe Found')
        self.assertEqual(recipe_selection(['Milk']), 'No Recipe Found')

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 456
