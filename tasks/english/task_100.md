# Input
- Programming Concept: Recursion
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Recursive Animal Counting

Write a recursive function named `count_animals(animals)` that takes a list of animals as an argument and returns the number of animals in the list. The function should work recursively and not use loops.

Example call:
```python
animals = ["Dog", "Cat", "Bird", "Fish"]
print(count_animals(animals))  # Output: 4
```

Note: The list can also be empty.

## Code Framework
```python
def count_animals(animals):
    ## Insert code here
```

## Model Solution
```python
def count_animals(animals):
    if not animals:
        return 0
    return 1 + count_animals(animals[1:])

animals = ["Dog", "Cat", "Bird", "Fish"]
print(count_animals(animals))
```

## Unit Tests
```python
import unittest

from main import count_animals

class TestCountAnimals(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_animals([]), 0)

    def test_single_animal(self):
        self.assertEqual(count_animals(["Dog"]), 1)

    def test_multiple_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat", "Bird", "Fish"]), 4)

    def test_different_animals(self):
        self.assertEqual(count_animals(["Elephant", "Mouse", "Tiger", "Lion", "Giraffe"]), 5)

    def test_repeated_animals(self):
        self.assertEqual(count_animals(["Dog", "Dog", "Dog"]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 518
