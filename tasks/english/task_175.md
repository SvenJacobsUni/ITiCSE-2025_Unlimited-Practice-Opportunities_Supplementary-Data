# Input
- Programming Concept: Functions as variables; If-Else statements; Lists
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pet Filter

Write a function named `filter_pets(pets, criterion)`, which takes a list of pets and a criterion as parameters. The function should return a new list containing only the pets that match the criterion.

The pets are given as words in a list, e.g., `['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']`.

The criterion is a function that takes a pet as an argument and returns a Boolean value. For example, a criterion could be a function that checks if the pet's name starts with a specific letter.

Example call:
```python
pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
criterion = lambda pet: pet.startswith('H')
print(filter_pets(pets, criterion))  # Output: ['Dog', 'Hamster']
```

Implement the function `filter_pets(pets, criterion)` so that it fulfills the functionality described above.

## Code Framework
```python
def filter_pets(pets, criterion):
    ## Insert code here
```

## Model Solution
```python
def filter_pets(pets, criterion):
    return [pet for pet in pets if criterion(pet)]

pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
criterion = lambda pet: pet.startswith('H')
print(filter_pets(pets, criterion))  # Output: ['Dog', 'Hamster']
```

## Unit Tests
```python
import unittest
from main import filter_pets

class TestFilterPets(unittest.TestCase):
    def test_pets_with_h(self):
        pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
        criterion = lambda pet: pet.startswith('H')
        self.assertEqual(filter_pets(pets, criterion), ['Dog', 'Hamster'])

    def test_pets_with_k(self):
        pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
        criterion = lambda pet: pet.startswith('K')
        self.assertEqual(filter_pets(pets, criterion), ['Cat'])

    def test_pets_with_v(self):
        pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
        criterion = lambda pet: pet.startswith('V')
        self.assertEqual(filter_pets(pets, criterion), ['Bird'])

    def test_pets_with_f(self):
        pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
        criterion = lambda pet: pet.startswith('F')
        self.assertEqual(filter_pets(pets, criterion), ['Fish'])

    def test_empty_list(self):
        pets = []
        criterion = lambda pet: pet.startswith('H')
        self.assertEqual(filter_pets(pets, criterion), [])

    def test_no_pets_meet_criterion(self):
        pets = ['Dog', 'Cat', 'Hamster', 'Bird', 'Fish']
        criterion = lambda pet: pet.startswith('Z')
        self.assertEqual(filter_pets(pets, criterion), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 607
