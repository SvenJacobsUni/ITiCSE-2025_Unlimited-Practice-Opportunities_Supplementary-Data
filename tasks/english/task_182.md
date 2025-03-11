# Input
- Programming Concept: String; Lists; Functions as variables
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Positive Affirmations

Positive affirmations can help to boost self-esteem and promote mental health. In this task, you are to implement a function that processes a list of positive affirmations and returns a random affirmation.

#### Task

Write a function `random_affirmation(affirmations)` that takes a list of positive affirmations as an argument and returns a random affirmation from this list. Use the `random.choice` function from the `random` module to make the random selection.

#### Example

```python
affirmations = [
    "I am strong and capable.",
    "I deserve love and respect.",
    "I am enough just as I am.",
    "I can achieve anything I set my mind to."
]

print(random_affirmation(affirmations))
```

The output could be one of the affirmations from the list, e.g. "I am strong and capable."

#### Hints

- Import the `random` module to use the `random.choice` function.
- The function should return one of the affirmations from the list.

Good luck!

## Code Framework
```python
def random_affirmation(affirmations):
    ## Insert code here
```

## Model Solution
```python
import random

def random_affirmation(affirmations):
    return random.choice(affirmations)

affirmations = [
    "I am strong and capable.",
    "I deserve love and respect.",
    "I am enough just as I am.",
    "I can achieve anything I set my mind to."
]

print(random_affirmation(affirmations))
```

## Unit Tests
```python
import unittest
from main import random_affirmation

class TestRandomAffirmation(unittest.TestCase):
    def test_selection_from_list(self):
        affirmations = [
            "I am strong and capable.",
            "I deserve love and respect.",
            "I am enough just as I am.",
            "I can achieve anything I set my mind to."
        ]
        result = random_affirmation(affirmations)
        self.assertIn(result, affirmations)

    def test_empty_list(self):
        affirmations = []
        with self.assertRaises(IndexError):
            random_affirmation(affirmations)

    def test_single_element(self):
        affirmations = ["I am strong and capable."]
        self.assertEqual(random_affirmation(affirmations), "I am strong and capable.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 614
