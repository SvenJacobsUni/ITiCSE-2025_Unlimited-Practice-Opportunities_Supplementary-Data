# Input
- Programming Concept: Functions as variables
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Functions as Variables in the Cooking Context

Write a function `cook_recipe(recipe_name)` that accepts a function as a parameter and executes that function. Create two example recipes as functions: `recipe_pasta()` and `recipe_salad()`.

- `recipe_pasta()` should output the message "Pasta is being cooked!".
- `recipe_salad()` should output the message "Salad is being prepared!".

The function `cook_recipe(recipe_name)` should execute the passed recipe function.

Example calls:
```python
cook_recipe(recipe_pasta)  # Output: Pasta is being cooked!
cook_recipe(recipe_salad)  # Output: Salad is being prepared!
```

## Code Framework
```python
def cook_recipe(recipe_name):
    ## Insert code here

def recipe_pasta():
    ## Insert code here

def recipe_salad():
    ## Insert code here
```

## Model Solution
```python
def cook_recipe(recipe_name):
    recipe_name()

def recipe_pasta():
    print("Pasta is being cooked!")

def recipe_salad():
    print("Salad is being prepared!")

cook_recipe(recipe_pasta)
cook_recipe(recipe_salad)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import cook_recipe, recipe_pasta, recipe_salad

class TestCookRecipe(unittest.TestCase):
    def test_recipe_pasta(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        cook_recipe(recipe_pasta)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pasta is being cooked!")

    def test_recipe_salad(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        cook_recipe(recipe_salad)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Salad is being prepared!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 454
