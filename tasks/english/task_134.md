# Input
- Programming Concept: Functions as variables; Boolean and None
- Context: Pets

# Generated Task Components
## Task Description
### Exercise Task: Pets and Functions

Write a function named `is_pet(name)`, that checks if the passed name belongs to a list of known pets. The list of known pets is: `['Dog', 'Cat', 'Hamster', 'Parrot', 'Goldfish']`. The function should return `True` if the name is in the list, and `False` if not.

Additionally, implement a function `is_pet_or_none(name)` that calls `is_pet(name)` and returns `None` if the name is not in the list of known pets.

Example Calls:
- `is_pet('Dog')` returns `True`.
- `is_pet('Elephant')` returns `False`.
- `is_pet_or_none('Cat')` returns `True`.
- `is_pet_or_none('Elephant')` returns `None`.

## Code Framework
```python
def is_pet(name):
    ## Insert code here



def is_pet_or_none(name):
    ## Insert code here

```

## Model Solution
```python
def is_pet(name):
    return name in ['Dog', 'Cat', 'Hamster', 'Parrot', 'Goldfish']


def is_pet_or_none(name):
    return is_pet(name) or None


# Example calls
print(is_pet('Dog'))  # True
print(is_pet('Elephant'))  # False
print(is_pet_or_none('Cat'))  # True
print(is_pet_or_none('Elephant'))  # None

```

## Unit Tests
```python
import unittest
from main import is_pet, is_pet_or_none


class TestIsPet(unittest.TestCase):
    def test_dog(self):
        self.assertTrue(is_pet('Dog'))


    def test_elephant(self):
        self.assertFalse(is_pet('Elephant'))


    def test_cat(self):
        self.assertTrue(is_pet('Cat'))


    def test_goldfish(self):
        self.assertTrue(is_pet('Goldfish'))


    def test_empty_string(self):
        self.assertFalse(is_pet(''))



class TestIsPetOrNone(unittest.TestCase):
    def test_dog(self):
        self.assertTrue(is_pet_or_none('Dog'))


    def test_elephant(self):
        self.assertIsNone(is_pet_or_none('Elephant'))


    def test_cat(self):
        self.assertTrue(is_pet_or_none('Cat'))


    def test_goldfish(self):
        self.assertTrue(is_pet_or_none('Goldfish'))


    def test_empty_string(self):
        self.assertIsNone(is_pet_or_none(''))



if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 566
