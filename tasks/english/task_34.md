# Input
- Programming Concept: String
- Context: Sports

# Generated Task Components
## Task Description
### Practice Task: Filter Sports

Write a function called `filter_sports(sports_list, filter_letter)` that takes a list of sports and a letter as parameters. The function should return a new list that only contains the sports starting with the specified letter.

Example call:
```python
sports = ["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"]
result = filter_sports(sports, "B")
print(result)  # Output: ["Basketball", "Baseball", "Badminton"]
```

Implement the function so that it delivers the desired results.

## Code Framework
```python
def filter_sports(sports_list, filter_letter):
    ## Insert code here
```

## Model Solution
```python
def filter_sports(sports_list, filter_letter):
    return [sport for sport in sports_list if sport.startswith(filter_letter)]

sports = ["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"]
result = filter_sports(sports, "B")
print(result)  # Output: ["Basketball", "Baseball", "Badminton"]
```

## Unit Tests
```python
import unittest
from main import filter_sports

class TestFilterSports(unittest.TestCase):
    def test_filter_b(self):
        self.assertEqual(filter_sports(["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"], "B"), ["Basketball", "Baseball", "Badminton"])

    def test_filter_f(self):
        self.assertEqual(filter_sports(["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"], "F"), ["Soccer"])

    def test_filter_t(self):
        self.assertEqual(filter_sports(["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"], "T"), ["Tennis"])

    def test_filter_no_match(self):
        self.assertEqual(filter_sports(["Basketball", "Baseball", "Soccer", "Tennis", "Badminton"], "X"), [])

    def test_empty_list(self):
        self.assertEqual(filter_sports([], "B"), [])

    def test_case_sensitivity(self):
        self.assertEqual(filter_sports(["Basketball", "baseball", "Soccer", "Tennis", "badminton"], "b"), ["baseball", "badminton"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 452
