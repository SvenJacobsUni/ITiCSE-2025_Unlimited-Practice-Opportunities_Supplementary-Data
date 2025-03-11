# Input
- Programming Concept: Lists
- Context: Cooking

# Generated Task Components
## Task Description
### Practice Task: Ingredient List for a Recipe

Write a function named `add_ingredient(ingredient_list, new_ingredient)`, which receives a list of ingredients and a new ingredient as parameters. The function should add the new ingredient to the ingredient list and return the updated list.

Example call:
```python
ingredients = ["Flour", "Sugar", "Eggs"]
new_ingredient = "Milk"
updated_list = add_ingredient(ingredients, new_ingredient)
print(updated_list)  # Output: ["Flour", "Sugar", "Eggs", "Milk"]
```

Also, create a function `remove_ingredient(ingredient_list, ingredient_to_remove)`, which receives a list of ingredients and an ingredient to remove as parameters. The function should remove the specified ingredient from the ingredient list and return the updated list.

Example call:
```python
ingredients = ["Flour", "Sugar", "Eggs", "Milk"]
ingredient_to_remove = "Sugar"
updated_list = remove_ingredient(ingredients, ingredient_to_remove)
print(updated_list)  # Output: ["Flour", "Eggs", "Milk"]
```

Implement both functions in Python.

## Code Framework
```python
def add_ingredient(ingredient_list, new_ingredient):
    ## Insert code here


def remove_ingredient(ingredient_list, ingredient_to_remove):
    ## Insert code here

```

## Model Solution
```python
def add_ingredient(ingredient_list, new_ingredient):
    ingredient_list.append(new_ingredient)
    return ingredient_list


def remove_ingredient(ingredient_list, ingredient_to_remove):
    ingredient_list.remove(ingredient_to_remove)
    return ingredient_list

# Example calls
ingredients = ["Flour", "Sugar", "Eggs"]
new_ingredient = "Milk"
updated_list = add_ingredient(ingredients, new_ingredient)
print(updated_list)  # Output: ["Flour", "Sugar", "Eggs", "Milk"]

ingredients = ["Flour", "Sugar", "Eggs", "Milk"]
ingredient_to_remove = "Sugar"
updated_list = remove_ingredient(ingredients, ingredient_to_remove)
print(updated_list)  # Output: ["Flour", "Eggs", "Milk"]

```

## Unit Tests
```python
import unittest
from main import add_ingredient, remove_ingredient

class TestIngredients(unittest.TestCase):
    def test_add_ingredient_simple(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs"], "Milk"), ["Flour", "Sugar", "Eggs", "Milk"])

    def test_add_ingredient_empty_list(self):
        self.assertEqual(add_ingredient([], "Milk"), ["Milk"])

    def test_add_ingredient_duplicate(self):
        self.assertEqual(add_ingredient(["Flour", "Sugar", "Eggs", "Milk"], "Milk"), ["Flour", "Sugar", "Eggs", "Milk", "Milk"])

    def test_remove_ingredient_simple(self):
        self.assertEqual(remove_ingredient(["Flour", "Sugar", "Eggs", "Milk"], "Sugar"), ["Flour", "Eggs", "Milk"])

    def test_remove_ingredient_last_element(self):
        self.assertEqual(remove_ingredient(["Flour", "Sugar", "Eggs", "Milk"], "Milk"), ["Flour", "Sugar", "Eggs"])

    def test_remove_ingredient_not_present(self):
        with self.assertRaises(ValueError):
            remove_ingredient(["Flour", "Sugar", "Eggs"], "Milk")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 449
