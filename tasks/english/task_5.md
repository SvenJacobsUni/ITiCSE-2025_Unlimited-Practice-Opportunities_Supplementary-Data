# Input
- Programming Concept: Recursion
- Context: Cooking

# Generated Task Components
## Task Description
### Exercise: Recursive Recipe Instructions

Write a recursive function named `cook_recipe(steps, index)` that takes a list of cooking steps and an index as arguments. The function should output the cooking steps in sequence, starting from the given index, and do so recursively. The function should stop when the index reaches the end of the list.

Example call:
```python
cooking_steps = ["Slice the onions.", "Heat the oil in the pan.", "Fry the onions.", "Add the tomatoes.", "Let everything simmer for 10 minutes."]
cook_recipe(cooking_steps, 0)
```

Expected output:
```
Slice the onions.
Heat the oil in the pan.
Fry the onions.
Add the tomatoes.
Let everything simmer for 10 minutes.
```

## Code Framework
```python
def cook_recipe(steps, index):
    ## Insert code here

```

## Model Solution
```python
def cook_recipe(steps, index):
    if index < len(steps):
        print(steps[index])
        cook_recipe(steps, index + 1)

cooking_steps = ["Slice the onions.", "Heat the oil in the pan.", "Fry the onions.", "Add the tomatoes.", "Let everything simmer for 10 minutes."]
cook_recipe(cooking_steps, 0)

```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import cook_recipe

class TestCookRecipe(unittest.TestCase):
    def setUp(self):
        self.cooking_steps = ["Slice the onions.", "Heat the oil in the pan.", "Fry the onions.", "Add the tomatoes.", "Let everything simmer for 10 minutes."]
        self.saved_stdout = sys.stdout
        self.output = StringIO()
        sys.stdout = self.output

    def tearDown(self):
        sys.stdout = self.saved_stdout

    def test_cook_recipe_complete(self):
        cook_recipe(self.cooking_steps, 0)
        self.assertEqual(self.output.getvalue().strip(), "\n".join(self.cooking_steps))

    def test_cook_recipe_from_middle(self):
        cook_recipe(self.cooking_steps, 2)
        self.assertEqual(self.output.getvalue().strip(), "\n".join(self.cooking_steps[2:]))

    def test_cook_recipe_last_step(self):
        cook_recipe(self.cooking_steps, 4)
        self.assertEqual(self.output.getvalue().strip(), self.cooking_steps[4])

    def test_cook_recipe_beyond_index(self):
        cook_recipe(self.cooking_steps, 5)
        self.assertEqual(self.output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 423
