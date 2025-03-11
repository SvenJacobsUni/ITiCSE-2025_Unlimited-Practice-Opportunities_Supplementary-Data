# Input
- Programming Concept: Integer; String; Boolean and None
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pet Information

Write a function named `pet_info(name, age, species)`, that takes information about a pet and returns an appropriate message. 

- `name` is a string containing the name of the pet.
- `age` is an integer representing the pet's age in years.
- `species` is a string describing the type of pet (e.g., "Dog", "Cat").

The function should meet the following conditions:
1. If the name of the pet is not provided (None), the function should return "No name provided".
2. If the pet's age is less than 0, the function should return "Invalid age".
3. If the species of the pet is "Dog", the function should return "The pet is a dog named [Name] and is [Age] years old.".
4. If the species of the pet is "Cat", the function should return "The pet is a cat named [Name] and is [Age] years old.".
5. For all other species of pets, the function should return "The pet is a [Species] named [Name] and is [Age] years old.".

Example calls:
- `pet_info("Bello", 5, "Dog")` returns "The pet is a dog named Bello and is 5 years old.".
- `pet_info(None, 3, "Cat")` returns "No name provided".
- `pet_info("Mimi", -1, "Cat")` returns "Invalid age".

## Code Framework
```python
def pet_info(name, age, species):
    ## Insert code here
```

## Model Solution
```python
def pet_info(name, age, species):
    if name is None:
        return "No name provided"
    if age < 0:
        return "Invalid age"
    if species == "Dog":
        return f"The pet is a dog named {name} and is {age} years old."
    if species == "Cat":
        return f"The pet is a cat named {name} and is {age} years old."
    return f"The pet is a {species} named {name} and is {age} years old."

# Example calls
print(pet_info("Bello", 5, "Dog"))
print(pet_info(None, 3, "Cat"))
print(pet_info("Mimi", -1, "Cat"))
```

## Unit Tests
```python
import unittest
from main import pet_info

class TestPetInfo(unittest.TestCase):
    def test_dog(self):
        self.assertEqual(pet_info("Bello", 5, "Dog"), "The pet is a dog named Bello and is 5 years old.")

    def test_cat(self):
        self.assertEqual(pet_info("Mimi", 3, "Cat"), "The pet is a cat named Mimi and is 3 years old.")

    def test_no_name(self):
        self.assertEqual(pet_info(None, 3, "Cat"), "No name provided")

    def test_invalid_age(self):
        self.assertEqual(pet_info("Mimi", -1, "Cat"), "Invalid age")

    def test_other_species(self):
        self.assertEqual(pet_info("Tweety", 2, "Bird"), "The pet is a Bird named Tweety and is 2 years old.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 595
