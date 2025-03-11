# Input
- Programming Concept: If-Else statements
- Context: Olympics

# Generated Task Components
## Task Description
### Exercise: Olympic Medals

Write a function named `medal_evaluation(number_of_gold, number_of_silver, number_of_bronze)` that evaluates the number of medals won by a country at the Olympic Games and returns an appropriate message.

- If the country has won at least 10 gold medals, the message "Outstanding performance!" should be returned.
- If the country has won at least 5 gold medals and at least 5 silver medals, the message "Very good performance!" should be returned.
- If the country has won at least 3 gold medals, 3 silver medals, and 3 bronze medals, the message "Good performance!" should be returned.
- In all other cases, the message "Participation is everything!" should be returned.

Example call:
```python
print(medal_evaluation(12, 4, 3))  # Output: Outstanding performance!
print(medal_evaluation(6, 5, 2))   # Output: Very good performance!
print(medal_evaluation(3, 3, 3))   # Output: Good performance!
print(medal_evaluation(1, 2, 1))   # Output: Participation is everything!
```

## Code Framework
```python
def medal_evaluation(number_of_gold, number_of_silver, number_of_bronze):
    ## Insert code here
```

## Model Solution
```python
def medal_evaluation(number_of_gold, number_of_silver, number_of_bronze):
    if number_of_gold >= 10:
        return "Outstanding performance!"
    elif number_of_gold >= 5 and number_of_silver >= 5:
        return "Very good performance!"
    elif number_of_gold >= 3 and number_of_silver >= 3 and number_of_bronze >= 3:
        return "Good performance!"
    else:
        return "Participation is everything!"

print(medal_evaluation(12, 4, 3))
print(medal_evaluation(6, 5, 2))
print(medal_evaluation(3, 3, 3))
print(medal_evaluation(1, 2, 1))
```

## Unit Tests
```python
import unittest
from main import medal_evaluation

class TestMedalEvaluation(unittest.TestCase):
    def test_outstanding_performance(self):
        self.assertEqual(medal_evaluation(12, 4, 3), "Outstanding performance!")

    def test_very_good_performance(self):
        self.assertEqual(medal_evaluation(6, 5, 2), "Very good performance!")

    def test_good_performance(self):
        self.assertEqual(medal_evaluation(3, 3, 3), "Good performance!")

    def test_participation_is_everything(self):
        self.assertEqual(medal_evaluation(1, 2, 1), "Participation is everything!")

    def test_edge_case_outstanding_performance(self):
        self.assertEqual(medal_evaluation(10, 0, 0), "Outstanding performance!")

    def test_edge_case_very_good_performance(self):
        self.assertEqual(medal_evaluation(5, 5, 0), "Very good performance!")

    def test_edge_case_good_performance(self):
        self.assertEqual(medal_evaluation(3, 3, 3), "Good performance!")

    def test_edge_case_participation_is_everything(self):
        self.assertEqual(medal_evaluation(2, 2, 2), "Participation is everything!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 457
