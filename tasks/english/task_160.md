# Input
- Programming Concept: While loops; Recursion; Operations with numbers
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise Task: Olympic Medal Counter

Write a function named `medal_counter(number_gold, number_silver, number_bronze)` that calculates the total number of medals won by a country at the Olympic Games. The function should take the number of gold, silver, and bronze medals as arguments and return the total number of medals.

Additionally, the function should call another function `medal_counter_recursive(number_gold, number_silver, number_bronze)` that performs the same calculation recursively.

Example call:
```python
medal_counter(10, 5, 8)
```
This call should return the total number of medals that the country has won.

## Code Framework
```python
def medal_counter(number_gold, number_silver, number_bronze):
    ## Insert code here

def medal_counter_recursive(number_gold, number_silver, number_bronze):
    ## Insert code here

```

## Model Solution
```python
def medal_counter(number_gold, number_silver, number_bronze):
    return number_gold + number_silver + number_bronze

def medal_counter_recursive(number_gold, number_silver, number_bronze):
    if number_gold == 0 and number_silver == 0 and number_bronze == 0:
        return 0
    return (1 if number_gold > 0 else 0) + (1 if number_silver > 0 else 0) + (1 if number_bronze > 0 else 0) + medal_counter_recursive(max(0, number_gold-1), max(0, number_silver-1), max(0, number_bronze-1))

print(medal_counter(10, 5, 8))
print(medal_counter_recursive(10, 5, 8))
```

## Unit Tests
```python
import unittest
from main import medal_counter, medal_counter_recursive

class TestMedalCounter(unittest.TestCase):
    def test_all_medals(self):
        self.assertEqual(medal_counter(10, 5, 8), 23)
        self.assertEqual(medal_counter_recursive(10, 5, 8), 23)

    def test_no_medals(self):
        self.assertEqual(medal_counter(0, 0, 0), 0)
        self.assertEqual(medal_counter_recursive(0, 0, 0), 0)

    def test_only_gold(self):
        self.assertEqual(medal_counter(5, 0, 0), 5)
        self.assertEqual(medal_counter_recursive(5, 0, 0), 5)

    def test_only_silver(self):
        self.assertEqual(medal_counter(0, 7, 0), 7)
        self.assertEqual(medal_counter_recursive(0, 7, 0), 7)

    def test_only_bronze(self):
        self.assertEqual(medal_counter(0, 0, 3), 3)
        self.assertEqual(medal_counter_recursive(0, 0, 3), 3)

    def test_edge_cases(self):
        self.assertEqual(medal_counter(1, 1, 1), 3)
        self.assertEqual(medal_counter_recursive(1, 1, 1), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 592
