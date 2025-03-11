# Input
- Programming Concept: If-Else statements;Boolean and None;Functions as variables
- Context: Restaurant

# Generated Task Components
## Task Description
### Exercise: Restaurant Order

Write a function called `take_order(order)`, which receives an order in a restaurant and returns an appropriate message. The function should check the following conditions:

1. If the order is "Pizza", the message "Your Pizza is being prepared." should be returned.
2. If the order is "Pasta", the message "Your Pasta is being prepared." should be returned.
3. If the order is "Salad", the message "Your Salad is being prepared." should be returned.
4. For all other orders, the message "Unfortunately, this order is not available." should be returned.

Example calls:
- `take_order("Pizza")` returns "Your Pizza is being prepared."
- `take_order("Burger")` returns "Unfortunately, this order is not available."

## Code Framework
```python
def take_order(order):
    ## Insert code here
```

## Model Solution
```python
def take_order(order):
    if order == "Pizza":
        return "Your Pizza is being prepared."
    elif order == "Pasta":
        return "Your Pasta is being prepared."
    elif order == "Salad":
        return "Your Salad is being prepared."
    else:
        return "Unfortunately, this order is not available."

# Example calls
print(take_order("Pizza"))
print(take_order("Burger"))
```

## Unit Tests
```python
import unittest
from main import take_order

class TestTakeOrder(unittest.TestCase):
    def test_pizza_order(self):
        self.assertEqual(take_order("Pizza"), "Your Pizza is being prepared.")

    def test_pasta_order(self):
        self.assertEqual(take_order("Pasta"), "Your Pasta is being prepared.")

    def test_salad_order(self):
        self.assertEqual(take_order("Salad"), "Your Salad is being prepared.")

    def test_unavailable_order(self):
        self.assertEqual(take_order("Burger"), "Unfortunately, this order is not available.")

    def test_empty_order(self):
        self.assertEqual(take_order(""), "Unfortunately, this order is not available.")

    def test_none_order(self):
        self.assertEqual(take_order(None), "Unfortunately, this order is not available.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 627
