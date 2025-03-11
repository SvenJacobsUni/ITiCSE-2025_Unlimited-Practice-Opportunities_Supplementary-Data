# Input
- Programming Concept: For loops;If-Else statements;Operations with numbers
- Context: Pets

# Generated Task Components
## Task Description
### Exercise Task: Pet Food Calculation

Write a function named `calculate_food_requirement(pets)`, which takes a list of pets and their weights (in kilograms) as an argument. The function should calculate the daily food requirement for each pet and return a list with the results.

The daily food requirement is calculated as follows:
- For dogs: 5% of body weight
- For cats: 3% of body weight
- For other pets: 2% of body weight

The list of pets is passed as a list of tuples, where each tuple contains the pet's name and its weight. Example: `["Dog", 20), ("Cat", 5), ("Hamster", 0.5)]`

Example call:
```python
pets = [("Dog", 20), ("Cat", 5), ("Hamster", 0.5)]
print(calculate_food_requirement(pets))
```

Expected output:
```python
[1.0, 0.15, 0.01]
```

## Code Framework
```python
def calculate_food_requirement(pets):
    ## Insert code here
```

## Model Solution
```python
def calculate_food_requirement(pets):
    return [weight * (0.05 if pet == "Dog" else 0.03 if pet == "Cat" else 0.02) for pet, weight in pets]

pets = [("Dog", 20), ("Cat", 5), ("Hamster", 0.5)]
print(calculate_food_requirement(pets))
```

## Unit Tests
```python
import unittest
from main import calculate_food_requirement

class TestCalculateFoodRequirement(unittest.TestCase):
    def test_dogs_and_cats(self):
        self.assertEqual(calculate_food_requirement([("Dog", 20), ("Cat", 5)]), [1.0, 0.15])

    def test_hamster(self):
        self.assertEqual(calculate_food_requirement([("Hamster", 0.5)]), [0.01])

    def test_mixed_pets(self):
        self.assertEqual(calculate_food_requirement([("Dog", 20), ("Cat", 5), ("Hamster", 0.5)]), [1.0, 0.15, 0.01])

    def test_empty_list(self):
        self.assertEqual(calculate_food_requirement([]), [])

    def test_unknown_pet(self):
        self.assertEqual(calculate_food_requirement([("Parrot", 1)]), [0.02])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 585
