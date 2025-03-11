# Input
- Programming Concept: Lists
- Context: Pets

# Generated Task Components
## Task Description
### Exercise Task: Pet List

Write a function named `pet_list(pets)`, which receives a list of pet names as an argument. The function should count the number of pets in the list and return a message indicating the number of pets. If the list is empty, the message "No pets found." should be returned.

Example Calls:

- `pet_list(["Bella", "Charlie", "Luna"])` returns "You have 3 pets."
- `pet_list([])` returns "No pets found."

## Code Framework
```python
def pet_list(pets):
    ## Insert code here
```

## Model Solution
```python
def pet_list(pets):
    if not pets:
        return "No pets found."
    else:
        return f"You have {len(pets)} pets."

pet_list(["Bella", "Charlie", "Luna"])
pet_list([])
```

## Unit Tests
```python
import unittest
from main import pet_list

class TestPetList(unittest.TestCase):
    def test_multiple_pets(self):
        self.assertEqual(pet_list(["Bella", "Charlie", "Luna"]), "You have 3 pets.")

    def test_no_pets(self):
        self.assertEqual(pet_list([]), "No pets found.")

    def test_one_pet(self):
        self.assertEqual(pet_list(["Bella"]), "You have 1 pet.")

    def test_two_pets(self):
        self.assertEqual(pet_list(["Bella", "Charlie"]), "You have 2 pets.")

    def test_many_pets(self):
        self.assertEqual(pet_list(["Bella", "Charlie", "Luna", "Max", "Lucy", "Daisy", "Bailey", "Molly", "Coco", "Buddy"]), "You have 10 pets.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 433
