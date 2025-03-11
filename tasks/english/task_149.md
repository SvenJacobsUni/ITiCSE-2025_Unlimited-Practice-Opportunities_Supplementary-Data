# Input
- Programming Concept: String;Operations with numbers
- Context: Olympics

# Generated Task Components
## Task Description
### Practice Task: Olympic Medal Count

Write a function named `medal_count(country, gold, silver, bronze)`, which calculates the number of medals won by a country at the Olympic Games and returns a corresponding message.

The function should have the following parameters:
- `country` (String): The name of the country.
- `gold` (int): The number of gold medals won.
- `silver` (int): The number of silver medals won.
- `bronze` (int): The number of bronze medals won.

The function should calculate the total number of medals and return a message in the following format:
```
[Country] has won a total of [Total Number] medals: [Gold] Gold, [Silver] Silver, [Bronze] Bronze.
```

Example call:
```python
print(medal_count("Germany", 10, 5, 7))
```

Example output:
```
Germany has won a total of 22 medals: 10 Gold, 5 Silver, 7 Bronze.
```

## Code Framework
```python
def medal_count(country, gold, silver, bronze):
    ## Insert code here
```

## Model Solution
```python
def medal_count(country, gold, silver, bronze):
    total = gold + silver + bronze
    return f"{country} has won a total of {total} medals: {gold} Gold, {silver} Silver, {bronze} Bronze."

print(medal_count("Germany", 10, 5, 7))
```

## Unit Tests
```python
import unittest
from main import medal_count

class TestMedalCount(unittest.TestCase):
    def test_germany(self):
        self.assertEqual(medal_count("Germany", 10, 5, 7), "Germany has won a total of 22 medals: 10 Gold, 5 Silver, 7 Bronze.")

    def test_usa(self):
        self.assertEqual(medal_count("USA", 15, 10, 5), "USA has won a total of 30 medals: 15 Gold, 10 Silver, 5 Bronze.")

    def test_china(self):
        self.assertEqual(medal_count("China", 8, 12, 6), "China has won a total of 26 medals: 8 Gold, 12 Silver, 6 Bronze.")

    def test_no_medals(self):
        self.assertEqual(medal_count("Nowhereland", 0, 0, 0), "Nowhereland has won a total of 0 medals: 0 Gold, 0 Silver, 0 Bronze.")

    def test_edge_case(self):
        self.assertEqual(medal_count("Testland", 1, 0, 0), "Testland has won a total of 1 medal: 1 Gold, 0 Silver, 0 Bronze.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 581
