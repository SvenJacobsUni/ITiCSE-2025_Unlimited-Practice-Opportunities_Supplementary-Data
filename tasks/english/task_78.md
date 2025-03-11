# Input
- Programming Concept: Functions as variables
- Context: Pets

# Generated Task Components
## Task Description
### Exercise Task: Functions as Variables

Write a function `pet_action(pet, action)`, which performs an action for a specific pet. The function should accept two parameters: `pet` (a string that specifies the name of the pet) and `action` (a function that describes an action to be performed with the pet).

Example call:
```python
def petting(pet):
    return f"{pet} is being petted."

def feeding(pet):
    return f"{pet} is being fed."

pet_action("Bello", petting)  # should return "Bello is being petted."
pet_action("Mieze", feeding)    # should return "Mieze is being fed."
```

Implement the function `pet_action(pet, action)` so that it performs the corresponding action for the given pet and returns the result.

## Code Framework
```python
def pet_action(pet, action):
    ## Insert code here
```

## Model Solution
```python
def pet_action(pet, action):
    return action(pet)

def petting(pet):
    return f"{pet} is being petted."

def feeding(pet):
    return f"{pet} is being fed."

pet_action("Bello", petting)
pet_action("Mieze", feeding)
```

## Unit Tests
```python
import unittest


def petting(pet):
    return f"{pet} is being petted."

def feeding(pet):
    return f"{pet} is being fed."

class TestPetAction(unittest.TestCase):
    def test_petting(self):
        self.assertEqual(pet_action("Bello", petting), "Bello is being petted.")

    def test_feeding(self):
        self.assertEqual(pet_action("Mieze", feeding), "Mieze is being fed.")

    def test_empty_name(self):
        self.assertEqual(pet_action("", petting), " is being petted.")

    def test_other_action(self):
        def bathing(pet):
            return f"{pet} is being bathed."
        self.assertEqual(pet_action("Rex", bathing), "Rex is being bathed.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 496
