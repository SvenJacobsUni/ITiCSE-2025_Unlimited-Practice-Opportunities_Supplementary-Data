# Input
- Programming Concept: Tuples
- Context: Restaurant

# Generated Task Components
## Task Description
### Exercise: Restaurant Menu

Write a function named `create_menu()` that returns a tuple with the names of three different dishes from a restaurant menu. Each dish should be included as a string in the tuple. Example call: `create_menu()` might return a tuple like `("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")`.

```python
def create_menu():
    # Your implementation here
    pass
```

Also create a function `print_menu(menu)` that iterates through the passed menu tuple and outputs each dish on a new line. Example call: `print_menu(("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu"))` should output the dishes each on a new line.

```python
def print_menu(menu):
    # Your implementation here
    pass
```

Use the `create_menu()` function and pass the returned tuple to the `print_menu()` function to print the menu to the console.

## Code Framework
```python
def create_menu():
    ## Insert code here
    pass

def print_menu(menu):
    ## Insert code here
    pass
```

## Model Solution
```python
def create_menu():
    return ("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")

def print_menu(menu):
    for dish in menu:
        print(dish)

menu = create_menu()
print_menu(menu)
```

## Unit Tests
```python
import unittest
from main import create_menu, print_menu
from io import StringIO
import sys

class TestRestaurantMenu(unittest.TestCase):
    def test_create_menu(self):
        menu = create_menu()
        self.assertIsInstance(menu, tuple)
        self.assertEqual(len(menu), 3)
        for dish in menu:
            self.assertIsInstance(dish, str)

    def test_print_menu(self):
        menu = ("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")
        expected_output = "Pizza Margherita\nSpaghetti Carbonara\nTiramisu\n"
        
        captured_output = StringIO()
        sys.stdout = captured_output
        print_menu(menu)
        sys.stdout = sys.__stdout__
        
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 451
