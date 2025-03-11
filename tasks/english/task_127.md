# Input
- Programming Concept: Tuples;Integer
- Context: Restaurant

# Generated Task Components
## Task Description
### Practice Task: Restaurant Order

Write a function named `take_order(order)` that receives a tuple with two elements as an argument. The first element is the name of the dish (string) and the second element is the number of portions ordered (integer). The function should return a message that summarizes the order.

Example call: `take_order(("Spaghetti Carbonara", 3))` returns `"You have ordered 3 portions of Spaghetti Carbonara."`

## Code Framework
```python
def take_order(order):
    ## Insert code here
```

## Model Solution
```python
def take_order(order):
    return f"You have ordered {order[1]} portions of {order[0]}."

print(take_order(("Spaghetti Carbonara", 3)))
```

## Unit Tests
```python
import unittest

from main import take_order

class TestTakeOrder(unittest.TestCase):
    def test_simple_order(self):
        self.assertEqual(take_order(("Spaghetti Carbonara", 3)), "You have ordered 3 portions of Spaghetti Carbonara.")

    def test_one_portion(self):
        self.assertEqual(take_order(("Pizza Margherita", 1)), "You have ordered 1 portion of Pizza Margherita.")

    def test_zero_portions(self):
        self.assertEqual(take_order(("Salad", 0)), "You have ordered 0 portions of Salad.")

    def test_large_order(self):
        self.assertEqual(take_order(("Burger", 100)), "You have ordered 100 portions of Burger.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 559
