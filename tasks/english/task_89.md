# Input
- Programming Concept: For loops
- Context: Restaurant

# Generated Task Components
## Task Description
### Practice Task: Restaurant Orders

Write a function named `record_orders(orders)` that receives a list of orders as an argument. Each order is a string containing the name of a dish. The function should count the number of orders for each dish and return the result as a dictionary.

Example call:
```python
orders = ["Pizza", "Burger", "Salad", "Pizza", "Burger", "Pizza"]
print(record_orders(orders))
```

Expected output:
```python
{'Pizza': 3, 'Burger': 2, 'Salad': 1}
```

## Code Framework
```python
def record_orders(orders):
    ## Insert code here
```

## Model Solution
```python
def record_orders(orders):
    result = {}
    for dish in orders:
        if dish in result:
            result[dish] += 1
        else:
            result[dish] = 1
    return result

orders = ["Pizza", "Burger", "Salad", "Pizza", "Burger", "Pizza"]
print(record_orders(orders))
```

## Unit Tests
```python
import unittest
from main import record_orders

class TestRecordOrders(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(record_orders(["Pizza", "Burger", "Salad", "Pizza", "Burger", "Pizza"]), {'Pizza': 3, 'Burger': 2, 'Salad': 1})

    def test_empty_list(self):
        self.assertEqual(record_orders([]), {})

    def test_single_order(self):
        self.assertEqual(record_orders(["Pizza"]), {'Pizza': 1})

    def test_multiple_different_orders(self):
        self.assertEqual(record_orders(["Pizza", "Burger", "Salad", "Noodles", "Pizza", "Burger", "Pizza", "Noodles"]), {'Pizza': 3, 'Burger': 2, 'Salad': 1, 'Noodles': 2})

    def test_all_same_orders(self):
        self.assertEqual(record_orders(["Pizza", "Pizza", "Pizza", "Pizza"]), {'Pizza': 4})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 507
