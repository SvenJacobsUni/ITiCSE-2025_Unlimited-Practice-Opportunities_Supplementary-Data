# Input
- Programming Concept: Lists
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise Task: Ingredient List for a Recipe

Write a function called `add_ingredient(ingredient_list, new_ingredient)`, which receives a list of ingredients and a new ingredient as parameters. The function should add the new ingredient to the ingredient list and return the updated list.

Example call:
```python
ingredients = ["Flour", "Sugar", "Eggs"]
updated_list = add_ingredient(ingredients, "Milk")
print(updated_list)  # Output: ["Flour", "Sugar", "Eggs", "Milk"]
```

### Additional Task: Remove Ingredients

Extend the function to allow the removal of an ingredient from the list. Write a function called `remove_ingredient(ingredient_list, remove_ingredient)`, which receives a list of ingredients and an ingredient to remove as parameters. The function should remove the ingredient from the list and return the updated list.

Example call:
```python
ingredients = ["Flour", "Sugar", "Eggs", "Milk"]
updated_list = remove_ingredient(ingredients, "Sugar")
print(updated_list)  # Output: ["Flour", "Eggs", "Milk"]
```

## Code Framework
```python
def add_ingredient(ingredient_list, new_ingredient):
    ## Insert code here


def remove_ingredient(ingredient_list, remove_ingredient):
    ## Insert code here
```

## Model Solution
```python
def add_ingredient(ingredient_list, new_ingredient):
    ingredient_list.append(new_ingredient)
    return ingredient_list


def remove_ingredient(ingredient_list, remove_ingredient):
    if remove_ingredient in ingredient_list:
        ingredient_list.remove(remove_ingredient)
    return ingredient_list

# Example calls
ingredients = ["Flour", "Sugar", "Eggs"]
updated_list = add_ingredient(ingredients, "Milk")
print(updated_list)  # Output: ["Flour", "Sugar", "Eggs", "Milk"]

updated_list = remove_ingredient(ingredients, "Sugar")
print(updated_list)  # Output: ["Flour", "Eggs", "Milk"]
```

## Unit Tests
```python
import unittest
from main import add_ingredient, remove_ingredient

class TestIngredients(unittest.TestCase):
    def test_add_ingredient(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs"], "Milk"), ["Flour", "Sugar", "Eggs", "Milk"])

    def test_remove_ingredient(self):
        self.assertEqual(remove_ingredient(["Flour", "Sugar", "Eggs", "Milk"], "Sugar"), ["Flour", "Eggs", "Milk"])

    def test_add_ingredient_empty_list(self):
        self.assertEqual(add_ingredient([], "Milk"), ["Milk"])

    def test_remove_ingredient_not_present(self):
        self.assertEqual(remove_ingredient(["Flour", "Sugar", "Eggs"], "Milk"), ["Flour", "Sugar", "Eggs"])

    def test_remove_ingredient_empty_list(self):
        self.assertEqual(remove_ingredient([], "Milk"), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 511
