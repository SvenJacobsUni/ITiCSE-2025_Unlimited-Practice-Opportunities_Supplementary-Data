# Input
- Programming Concept: Higher-order functions
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Higher-order functions in the context of "Cooking"

Write a function `cooking_assistant(recipe, preparation)` that accepts two arguments: a list of ingredients (`recipe`) and a function (`preparation`) that describes the preparation steps. The function `cooking_assistant` should apply the preparation steps to each ingredient and return a list of results.

Example call:
```python
def chop(ingredient):
    return f"Chop {ingredient}"

ingredients = ["Tomatoes", "Onions", "Peppers"]
result = cooking_assistant(ingredients, chop)
print(result)  # Output: ["Chop Tomatoes", "Chop Onions", "Chop Peppers"]
```

Implement the function `cooking_assistant` so that it applies the preparation steps to each ingredient in the list and returns the results in a new list.

## Code Framework
```python
def cooking_assistant(recipe, preparation):
    ## Insert code here
```

## Model Solution
```python
def cooking_assistant(recipe, preparation):
    return [preparation(ingredient) for ingredient in recipe]

def chop(ingredient):
    return f"Chop {ingredient}"

ingredients = ["Tomatoes", "Onions", "Peppers"]
result = cooking_assistant(ingredients, chop)
print(result)
```

## Unit Tests
```python
import unittest
from main import cooking_assistant

def chop(ingredient):
    return f"Chop {ingredient}"

def cook(ingredient):
    return f"Cook {ingredient}"

class TestCookingAssistant(unittest.TestCase):
    def test_chop(self):
        ingredients = ["Tomatoes", "Onions", "Peppers"]
        expected = ["Chop Tomatoes", "Chop Onions", "Chop Peppers"]
        self.assertEqual(cooking_assistant(ingredients, chop), expected)

    def test_cook(self):
        ingredients = ["Potatoes", "Carrots"]
        expected = ["Cook Potatoes", "Cook Carrots"]
        self.assertEqual(cooking_assistant(ingredients, cook), expected)

    def test_empty_list(self):
        ingredients = []
        expected = []
        self.assertEqual(cooking_assistant(ingredients, chop), expected)

    def test_single_ingredient(self):
        ingredients = ["Cucumber"]
        expected = ["Chop Cucumber"]
        self.assertEqual(cooking_assistant(ingredients, chop), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 463
