# Input
- Programming Concept: Integer
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise: Streaming Services and Integer

Write a function named `calculate_monthly_costs(subscriptions)`, which receives a list of integers as an argument. Each integer in the list represents the monthly cost of a subscription from different streaming services in Euros. The function should calculate and return the total cost of all subscriptions.

Example call:
```python
subscriptions = [10, 15, 8, 12]
print(calculate_monthly_costs(subscriptions))  # Output: 45
```


## Code Framework
```python
def calculate_monthly_costs(subscriptions):
    ## Insert code here

```

## Model Solution
```python
def calculate_monthly_costs(subscriptions):
    return sum(subscriptions)

subscriptions = [10, 15, 8, 12]
print(calculate_monthly_costs(subscriptions))

```

## Unit Tests
```python
import unittest
from main import calculate_monthly_costs

class TestCalculateMonthlyCosts(unittest.TestCase):
    def test_multiple_subscriptions(self):
        self.assertEqual(calculate_monthly_costs([10, 15, 8, 12]), 45)

    def test_no_subscriptions(self):
        self.assertEqual(calculate_monthly_costs([]), 0)

    def test_single_subscription(self):
        self.assertEqual(calculate_monthly_costs([20]), 20)

    def test_mixed_subscriptions(self):
        self.assertEqual(calculate_monthly_costs([5, 10, 15, 20, 25]), 75)

    def test_negative_value(self):
        self.assertEqual(calculate_monthly_costs([10, -5, 15]), 20)

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 489
