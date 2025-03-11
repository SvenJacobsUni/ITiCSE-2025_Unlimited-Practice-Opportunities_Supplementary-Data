# Input
- Programming Concept: Boolean and None;For loops
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Counting Animals

Write a function named `count_animals(animal_list)` that receives a list of animals as an argument. The function should count the number of animals in the list and return it. If the list is empty, the function should return `None`.

Example calls:

- `count_animals(["Dog", "Cat", "Bird"])` returns `3`.
- `count_animals([])` returns `None`.

Use a `for` loop to count the animals in the list.

## Code Framework
```python
def count_animals(animal_list):
    ## Insert code here
```

## Model Solution
```python
def count_animals(animal_list):
    if not animal_list:
        return None
    return len(animal_list)

print(count_animals(["Dog", "Cat", "Bird"]))  # Output: 3
print(count_animals([]))  # Output: None
```

## Unit Tests
```python
import unittest

from main import count_animals

class TestCountAnimals(unittest.TestCase):
    def test_multiple_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat", "Bird"]), 3)

    def test_empty_list(self):
        self.assertEqual(count_animals([]), None)

    def test_one_animal(self):
        self.assertEqual(count_animals(["Dog"]), 1)

    def test_two_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat"]), 2)

    def test_many_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat", "Bird", "Fish", "Mouse"]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 561
