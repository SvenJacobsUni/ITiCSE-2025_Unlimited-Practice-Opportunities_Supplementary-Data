# Input
- Programming Concept: For loops; If-Else statements
- Context: Restaurant

# Generated Task Components
## Task Description
### Exercise: Restaurant Orders

Write a function named `check_order(orders)`, which takes a list of orders as an argument. Each order is a dictionary with the keys "dish" and "quantity". The function should iterate over the orders and check if the quantity of the ordered dishes is greater than 0. If the quantity is greater than 0, the function should print a message stating that the order has been accepted. Otherwise, the function should print a message stating that the order has been declined.

Example call:
```python
orders = [
    {"dish": "Pizza", "quantity": 2},
    {"dish": "Salad", "quantity": 0},
    {"dish": "Pasta", "quantity": 3}
]
check_order(orders)
```

Expected output:
```
Order for Pizza accepted.
Order for Salad declined.
Order for Pasta accepted.
```

## Code Framework
```python
def check_order(orders):
    ## Insert code here
```

## Model Solution
```python
def check_order(orders):
    for o in orders:
        if o["quantity"] > 0:
            print(f"Order for {o['dish']} accepted.")
        else:
            print(f"Order for {o['dish']} declined.")

orders = [
    {"dish": "Pizza", "quantity": 2},
    {"dish": "Salad", "quantity": 0},
    {"dish": "Pasta", "quantity": 3}
]
check_order(orders)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import check_order

class TestCheckOrder(unittest.TestCase):
    def test_all_orders_accepted(self):
        orders = [
            {"dish": "Pizza", "quantity": 2},
            {"dish": "Pasta", "quantity": 3}
        ]
        expected_output = "Order for Pizza accepted.\nOrder for Pasta accepted.\n"
        self._run_test(orders, expected_output)

    def test_all_orders_declined(self):
        orders = [
            {"dish": "Salad", "quantity": 0},
            {"dish": "Soup", "quantity": 0}
        ]
        expected_output = "Order for Salad declined.\nOrder for Soup declined.\n"
        self._run_test(orders, expected_output)

    def test_mixed_orders(self):
        orders = [
            {"dish": "Pizza", "quantity": 2},
            {"dish": "Salad", "quantity": 0},
            {"dish": "Pasta", "quantity": 3}
        ]
        expected_output = "Order for Pizza accepted.\nOrder for Salad declined.\nOrder for Pasta accepted.\n"
        self._run_test(orders, expected_output)

    def test_empty_order_list(self):
        orders = []
        expected_output = ""
        self._run_test(orders, expected_output)

    def _run_test(self, orders, expected_output):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_order(orders)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 563
