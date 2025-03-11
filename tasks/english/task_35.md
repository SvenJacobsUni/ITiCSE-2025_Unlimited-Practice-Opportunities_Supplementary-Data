# Input
- Programming Concept: If-Else statements; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise: Olympic Medal Comparison

Write a function named `compare_medals(country1_gold, country1_silver, country1_bronze, country2_gold, country2_silver, country2_bronze)` that compares the number of medals won by two countries in the Olympic Games and returns an appropriate message.

The function should take the number of gold, silver, and bronze medals of the two countries as arguments and perform the following comparisons:

1. If one country has more gold medals than the other, the function should return a message indicating which country won more gold medals.
2. If both countries have the same number of gold medals, the function should compare the number of silver medals and return an appropriate message.
3. If the number of silver medals is also the same, the function should compare the number of bronze medals and return an appropriate message.
4. If both countries have the same number of medals in all categories, the function should return a message stating that both countries won the same number of medals.

Example call:
```python
compare_medals(10, 5, 3, 8, 7, 2)
```

Expected output:
```
Country 1 won more gold medals.
```

## Code Framework
```python
def compare_medals(country1_gold, country1_silver, country1_bronze, country2_gold, country2_silver, country2_bronze):
    ## Insert code here
```

## Model Solution
```python
def compare_medals(country1_gold, country1_silver, country1_bronze, country2_gold, country2_silver, country2_bronze):
    if country1_gold > country2_gold:
        print("Country 1 won more gold medals.")
    elif country1_gold < country2_gold:
        print("Country 2 won more gold medals.")
    elif country1_silver > country2_silver:
        print("Country 1 won more silver medals.")
    elif country1_silver < country2_silver:
        print("Country 2 won more silver medals.")
    elif country1_bronze > country2_bronze:
        print("Country 1 won more bronze medals.")
    elif country1_bronze < country2_bronze:
        print("Country 2 won more bronze medals.")
    else:
        print("Both countries won the same number of medals.")

compare_medals(10, 5, 3, 8, 7, 2)
```

## Unit Tests
```python
import unittest

from main import compare_medals

class TestCompareMedals(unittest.TestCase):
    def test_country1_more_gold(self):
        self.assertEqual(compare_medals(10, 5, 3, 8, 7, 2), "Country 1 won more gold medals.")

    def test_country2_more_gold(self):
        self.assertEqual(compare_medals(8, 5, 3, 10, 7, 2), "Country 2 won more gold medals.")

    def test_country1_more_silver(self):
        self.assertEqual(compare_medals(10, 7, 3, 10, 5, 2), "Country 1 won more silver medals.")

    def test_country2_more_silver(self):
        self.assertEqual(compare_medals(10, 5, 3, 10, 7, 2), "Country 2 won more silver medals.")

    def test_country1_more_bronze(self):
        self.assertEqual(compare_medals(10, 5, 4, 10, 5, 3), "Country 1 won more bronze medals.")

    def test_country2_more_bronze(self):
        self.assertEqual(compare_medals(10, 5, 3, 10, 5, 4), "Country 2 won more bronze medals.")

    def test_same_number_medals(self):
        self.assertEqual(compare_medals(10, 5, 3, 10, 5, 3), "Both countries won the same number of medals.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 453
