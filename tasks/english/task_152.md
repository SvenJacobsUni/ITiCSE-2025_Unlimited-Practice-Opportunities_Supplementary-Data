# Input
- Programming Concept: Operations with numbers; String; Float
- Context: Olympics

# Generated Task Components
## Task Description
### Practice Task: Olympic Medal Calculator

Write a function named `medal_calculator(gold, silver, bronze)` that calculates the total score of a country in the Olympic Games. The points distribution is as follows:

- Gold medal: 3 points
- Silver medal: 2 points
- Bronze medal: 1 point

The function should calculate the total score and return it as a floating-point number (float).

Example call:
```python
medal_calculator(5, 3, 2)
```
This call should calculate and return the total score for 5 gold, 3 silver, and 2 bronze medals.

## Code Framework
```python
def medal_calculator(gold, silver, bronze):
    ## Insert code here
```

## Model Solution
```python
def medal_calculator(gold, silver, bronze):
    return float(3 * gold + 2 * silver + 1 * bronze)

print(medal_calculator(5, 3, 2))
```

## Unit Tests
```python
import unittest
from main import medal_calculator

class TestMedalCalculator(unittest.TestCase):
    def test_all_medals(self):
        self.assertEqual(medal_calculator(5, 3, 2), 5*3 + 3*2 + 2*1)

    def test_no_medals(self):
        self.assertEqual(medal_calculator(0, 0, 0), 0.0)

    def test_only_gold(self):
        self.assertEqual(medal_calculator(10, 0, 0), 10*3)

    def test_only_silver(self):
        self.assertEqual(medal_calculator(0, 10, 0), 10*2)

    def test_only_bronze(self):
        self.assertEqual(medal_calculator(0, 0, 10), 10*1)

    def test_mixed_medals(self):
        self.assertEqual(medal_calculator(1, 1, 1), 3 + 2 + 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 584
