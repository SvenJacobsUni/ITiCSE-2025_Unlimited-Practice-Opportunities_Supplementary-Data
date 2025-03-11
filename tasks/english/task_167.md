# Input
- Programming Concept: Functions as variables;Recursion;Tuples
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Recipe Management with Recursion and Tuples

Write a function `cook_recipe(recipe)` that takes a recipe as input and recursively processes the ingredients and preparation steps. The recipe is provided as a nested tuple, where each element is either an ingredient (as a string) or another preparation step (as a tuple). The function should output the ingredients and steps in the correct order.

Example:

```python
recipe = (
    "Prepare ingredients",
    (
        "Chop tomatoes",
        "Chop onions",
        (
            "Peel garlic",
            "Chop garlic"
        )
    ),
    "Put everything in the pan",
    "Season with salt and pepper"
)

cook_recipe(recipe)
```

Expected Output:

```
Prepare ingredients
Chop tomatoes
Chop onions
Peel garlic
Chop garlic
Put everything in the pan
Season with salt and pepper
```

Implement the function `cook_recipe(recipe)` that recursively traverses the recipe and outputs the steps in the correct order.

## Code Framework
```python
def cook_recipe(recipe):
    ## Insert code here
```

## Model Solution
```python
def cook_recipe(recipe):
    for step in recipe:
        if isinstance(step, tuple):
            cook_recipe(step)
        else:
            print(step)

recipe = (
    "Prepare ingredients",
    (
        "Chop tomatoes",
        "Chop onions",
        (
            "Peel garlic",
            "Chop garlic"
        )
    ),
    "Put everything in the pan",
    "Season with salt and pepper"
)

cook_recipe(recipe)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import cook_recipe

class TestCookRecipe(unittest.TestCase):
    def setUp(self):
        self.recipe = (
            "Prepare ingredients",
            (
                "Chop tomatoes",
                "Chop onions",
                (
                    "Peel garlic",
                    "Chop garlic"
                )
            ),
            "Put everything in the pan",
            "Season with salt and pepper"
        )

    def test_cook_recipe(self):
        expected_output = (
            "Prepare ingredients\n"
            "Chop tomatoes\n"
            "Chop onions\n"
            "Peel garlic\n"
            "Chop garlic\n"
            "Put everything in the pan\n"
            "Season with salt and pepper\n"
        )
        captured_output = StringIO()
        sys.stdout = captured_output
        cook_recipe(self.recipe)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 599
