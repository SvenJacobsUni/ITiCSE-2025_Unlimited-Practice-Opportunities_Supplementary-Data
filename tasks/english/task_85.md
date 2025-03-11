# Input
- Programming Concept: Integer
- Context: Aquarium

# Generated Task Components
## Task Description
### Exercise: Aquarium

Write a function named `count_fish(number_of_fish)` that checks the number of fish in an aquarium and returns an appropriate message.

- If the number of fish is less than 5, the message "The aquarium is quite empty." should be returned.
- If the number of fish is between 5 and 10 (inclusive), the message "The aquarium has a good number of fish." should be returned.
- If the number of fish is more than 10, the message "The aquarium is overcrowded!" should be returned.

Example calls:
- `count_fish(3)` returns "The aquarium is quite empty."
- `count_fish(7)` returns "The aquarium has a good number of fish."
- `count_fish(12)` returns "The aquarium is overcrowded!"

## Code Framework
```python
def count_fish(number_of_fish):
    ## Insert code here
```

## Model Solution
```python
def count_fish(number_of_fish):
    if number_of_fish < 5:
        return "The aquarium is quite empty."
    elif 5 <= number_of_fish <= 10:
        return "The aquarium has a good number of fish."
    else:
        return "The aquarium is overcrowded!"

# Example calls
print(count_fish(3))
print(count_fish(7))
print(count_fish(12))
```

## Unit Tests
```python
import unittest
from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_few_fish(self):
        self.assertEqual(count_fish(3), "The aquarium is quite empty.")

    def test_good_number_of_fish(self):
        self.assertEqual(count_fish(7), "The aquarium has a good number of fish.")

    def test_many_fish(self):
        self.assertEqual(count_fish(12), "The aquarium is overcrowded!")

    def test_lower_boundary(self):
        self.assertEqual(count_fish(5), "The aquarium has a good number of fish.")

    def test_upper_boundary(self):
        self.assertEqual(count_fish(10), "The aquarium has a good number of fish.")

    def test_no_fish(self):
        self.assertEqual(count_fish(0), "The aquarium is quite empty.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 503
