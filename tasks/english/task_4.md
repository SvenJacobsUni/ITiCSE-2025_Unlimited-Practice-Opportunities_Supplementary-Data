# Input
- Programming Concept: String
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pet Description

Write a function named `pet_description(animal_type, name)` that creates a description of a pet. The function should take two parameters: `animal_type` (e.g., "Dog", "Cat") and `name` (e.g., "Bello", "Minka"). The function should return a string that describes the pet.

Example call: 
```python
pet_description("Dog", "Bello")
```

Expected output:
```python
"Bello is a Dog."
```

Example call:
```python
pet_description("Cat", "Minka")
```

Expected output:
```python
"Minka is a Cat."
```

## Code Framework
```python
def pet_description(animal_type, name):
    ## Insert code here
```

## Model Solution
```python
def pet_description(animal_type, name):
    return f"{name} is a{'' if animal_type.lower() in ['dog', 'bird'] else 'n/a'} {animal_type}."

print(pet_description("Dog", "Bello"))
print(pet_description("Cat", "Minka"))
```

## Unit Tests
```python
import unittest
from main import pet_description

class TestPetDescription(unittest.TestCase):
    def test_dog(self):
        self.assertEqual(pet_description("Dog", "Bello"), "Bello is a Dog.")

    def test_cat(self):
        self.assertEqual(pet_description("Cat", "Minka"), "Minka is a Cat.")

    def test_bird(self):
        self.assertEqual(pet_description("Bird", "Tweety"), "Tweety is a Bird.")

    def test_fish(self):
        self.assertEqual(pet_description("Fish", "Nemo"), "Nemo is a Fish.")

    def test_empty_name(self):
        self.assertEqual(pet_description("Dog", ""), " is a Dog.")

    def test_empty_animal_type(self):
        self.assertEqual(pet_description("", "Bello"), "Bello is a .")

    def test_empty_parameters(self):
        self.assertEqual(pet_description("", ""), " is a .")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 422
