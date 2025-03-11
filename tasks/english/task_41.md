# Input
- Programming Concept: Recursion
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise: Recursive Medal Counting

Write a recursive function called `count_medals(medals)`, that calculates the total number of medals a country has won at the Olympic Games. The medals are passed in a list, with each medal represented as a string ("Gold", "Silver", or "Bronze").

Example call:
```python
medals = ["Gold", "Silver", "Bronze", "Gold", "Silver"]
print(count_medals(medals))  # Output: 5
```

Implement the function so that it works recursively.

## Code Framework
```python
def count_medals(medals):
    ## Insert code here
```

## Model Solution
```python
def count_medals(medals):
    if not medals:
        return 0
    return 1 + count_medals(medals[1:])

medals = ["Gold", "Silver", "Bronze", "Gold", "Silver"]
print(count_medals(medals))  # Output: 5
```

## Unit Tests
```python
import unittest
from main import count_medals

class TestCountMedals(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_medals([]), 0)

    def test_single_medal(self):
        self.assertEqual(count_medals(["Gold"]), 1)

    def test_multiple_medals(self):
        self.assertEqual(count_medals(["Gold", "Silver", "Bronze", "Gold", "Silver"]), 5)

    def test_only_gold(self):
        self.assertEqual(count_medals(["Gold", "Gold", "Gold"]), 3)

    def test_only_silver(self):
        self.assertEqual(count_medals(["Silver", "Silver"]), 2)

    def test_only_bronze(self):
        self.assertEqual(count_medals(["Bronze"]), 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 459
