# Input
- Programming Concept: Operations with numbers
- Context: Restaurant

# Generated Task Components
## Task Description
### Practice Task: Calculate Restaurant Bill

Write a function called `calculate_bill(prices, tip_percent)` that calculates the total bill for a restaurant. The function should accept a list of prices (`prices`) and a percentage for the tip (`tip_percent`) as arguments. The function should calculate the total sum of the prices, add the tip based on the percentage, and return the total bill.

Example call:
```python
prices = [10.50, 20.75, 8.99]
tip_percent = 15
print(calculate_bill(prices, tip_percent))  # Expected output: 45.29
```

In this example, the prices of the ordered dishes are 10.50, 20.75, and 8.99. The tip is 15% of the total sum of the prices. The function should calculate and return the total bill.

## Code Framework
```python
def calculate_bill(prices, tip_percent):
    ## Insert code here

```

## Model Solution
```python
def calculate_bill(prices, tip_percent):
    total = sum(prices)
    tip = total * (tip_percent / 100)
    return round(total + tip, 2)

prices = [10.50, 20.75, 8.99]
tip_percent = 15
print(calculate_bill(prices, tip_percent))
```

## Unit Tests
```python
import unittest
from main import calculate_bill

class TestCalculateBill(unittest.TestCase):
    def test_simple_bill(self):
        prices = [10.50, 20.75, 8.99]
        tip_percent = 15
        self.assertEqual(calculate_bill(prices, tip_percent), 45.29)

    def test_no_prices(self):
        prices = []
        tip_percent = 15
        self.assertEqual(calculate_bill(prices, tip_percent), 0.00)

    def test_no_tip(self):
        prices = [10.50, 20.75, 8.99]
        tip_percent = 0
        self.assertEqual(calculate_bill(prices, tip_percent), 40.24)

    def test_high_tip(self):
        prices = [10.50, 20.75, 8.99]
        tip_percent = 100
        self.assertEqual(calculate_bill(prices, tip_percent), 80.48)

    def test_rounding(self):
        prices = [10.333, 20.666, 8.999]
        tip_percent = 10
        self.assertEqual(calculate_bill(prices, tip_percent), 43.22)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 455
