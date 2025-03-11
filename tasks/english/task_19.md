# Input
- Programming Concept: For loops
- Context: Amusement Park

# Generated Task Components
## Task Description
### Exercise: Amusement Park - Visitor Counting

Write a function named `count_visitors(visitor_list)` that receives a list of visitor names as an argument. The function should count the number of visitors in the amusement park and return this number. Use a for loop to iterate through the list and determine the number of visitors.

Example call:
```python
visitor_list = ["Anna", "Ben", "Clara", "David", "Eva"]
visitor_count = count_visitors(visitor_list)
print(visitor_count)  # Output: 5
```

In this example, the list `visitor_list` contains five names, so the function `count_visitors` should return the value `5`.

## Code Framework
```python
def count_visitors(visitor_list):
    ## Insert code here
```

## Model Solution
```python
def count_visitors(visitor_list):
    return len(visitor_list)

visitor_list = ["Anna", "Ben", "Clara", "David", "Eva"]
visitor_count = count_visitors(visitor_list)
print(visitor_count)  # Output: 5
```

## Unit Tests
```python
import unittest
from main import count_visitors

class TestCountVisitors(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_visitors([]), 0)

    def test_single_visitor(self):
        self.assertEqual(count_visitors(["Anna"]), 1)

    def test_multiple_visitors(self):
        self.assertEqual(count_visitors(["Anna", "Ben", "Clara", "David", "Eva"]), 5)

    def test_duplicate_visitors(self):
        self.assertEqual(count_visitors(["Anna", "Anna", "Ben", "Ben"]), 4)

    def test_mixed_visitors(self):
        self.assertEqual(count_visitors(["Anna", "Ben", "Clara", "David", "Eva", "Anna", "Ben"]), 7)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 437
