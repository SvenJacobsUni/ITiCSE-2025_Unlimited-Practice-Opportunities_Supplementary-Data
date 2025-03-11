# Input
- Programming Concept: Functions as variables; Integer
- Context: Animals

# Generated Task Components
## Task Description
### Practice Task: Animal Age in Human Years

Write a function called `animal_age_in_human_years(animal, age)`, which calculates the age of an animal in human years. The function should take two parameters: `animal` (a string indicating the type of animal, e.g., "Dog" or "Cat") and `age` (an integer representing the age of the animal in years).

The conversion should be as follows:
- For Dogs: 1 animal year equals 7 human years.
- For Cats: 1 animal year equals 5 human years.

The function should return the calculated age in human years.

Example calls:
- `animal_age_in_human_years("Dog", 3)` should return 21.
- `animal_age_in_human_years("Cat", 4)` should return 20.

## Code Framework
```python
def animal_age_in_human_years(animal, age):
    ## Insert code here
```

## Model Solution
```python
def animal_age_in_human_years(animal, age):
    multiplier = 7 if animal == "Dog" else 5 if animal == "Cat" else 1
    return age * multiplier

print(animal_age_in_human_years("Dog", 3))  # 21
print(animal_age_in_human_years("Cat", 4))  # 20
```

## Unit Tests
```python
import unittest

from main import animal_age_in_human_years

class TestAnimalAgeInHumanYears(unittest.TestCase):
    def test_dog_age(self):
        self.assertEqual(animal_age_in_human_years("Dog", 3), 21)

    def test_cat_age(self):
        self.assertEqual(animal_age_in_human_years("Cat", 4), 20)

    def test_dog_age_boundary(self):
        self.assertEqual(animal_age_in_human_years("Dog", 0), 0)

    def test_cat_age_boundary(self):
        self.assertEqual(animal_age_in_human_years("Cat", 0), 0)

    def test_unknown_animal(self):
        self.assertEqual(animal_age_in_human_years("Bird", 3), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 536
