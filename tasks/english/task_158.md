# Input
- Programming Concept: Operations with numbers;String;Boolean and None
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise: Olympic Medal Table

Write a function named `medal_table(gold, silver, bronze)`, which takes the number of medals won by a country at the Olympic Games and returns an appropriate message.

- If the country has not won any medals (all values are 0), the function should return "No medals won."
- If the country has won at least one gold medal, the function should return "Gold medals: [number]"
- If the country has won at least one silver medal, the function should return "Silver medals: [number]"
- If the country has won at least one bronze medal, the function should return "Bronze medals: [number]"

Example calls:
- `medal_table(0, 0, 0)` returns "No medals won."
- `medal_table(1, 0, 0)` returns "Gold medals: 1"
- `medal_table(0, 2, 0)` returns "Silver medals: 2"
- `medal_table(0, 0, 3)` returns "Bronze medals: 3"
- `medal_table(1, 2, 3)` returns "Gold medals: 1\nSilver medals: 2\nBronze medals: 3"

## Code Framework
```python
def medal_table(gold, silver, bronze):
    ## Insert code here
```

## Model Solution
```python
def medal_table(gold, silver, bronze):
    if gold == silver == bronze == 0:
        return "No medals won."
    result = []
    if gold > 0:
        result.append(f"Gold medals: {gold}")
    if silver > 0:
        result.append(f"Silver medals: {silver}")
    if bronze > 0:
        result.append(f"Bronze medals: {bronze}")
    return "\n".join(result)

# Example calls
print(medal_table(0, 0, 0))
print(medal_table(1, 0, 0))
print(medal_table(0, 2, 0))
print(medal_table(0, 0, 3))
print(medal_table(1, 2, 3))
```

## Unit Tests
```python
import unittest
from main import medal_table

class TestMedalTable(unittest.TestCase):
    def test_no_medals(self):
        self.assertEqual(medal_table(0, 0, 0), "No medals won.")

    def test_only_gold(self):
        self.assertEqual(medal_table(1, 0, 0), "Gold medals: 1")

    def test_only_silver(self):
        self.assertEqual(medal_table(0, 2, 0), "Silver medals: 2")

    def test_only_bronze(self):
        self.assertEqual(medal_table(0, 0, 3), "Bronze medals: 3")

    def test_gold_silver_bronze(self):
        self.assertEqual(medal_table(1, 2, 3), "Gold medals: 1\nSilver medals: 2\nBronze medals: 3")

    def test_gold_and_silver(self):
        self.assertEqual(medal_table(1, 2, 0), "Gold medals: 1\nSilver medals: 2")

    def test_gold_and_bronze(self):
        self.assertEqual(medal_table(1, 0, 3), "Gold medals: 1\nBronze medals: 3")

    def test_silver_and_bronze(self):
        self.assertEqual(medal_table(0, 2, 3), "Silver medals: 2\nBronze medals: 3")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 590
