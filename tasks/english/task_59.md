# Input
- Programming Concept: Recursion
- Context: Cooking

# Generated Task Components
## Task Description
### Practice Task: Recursive Preparation of Pancakes

Write a recursive function named `prepare_pancakes(count)`, which simulates the preparation of pancakes. The function should print a message for each pancake, indicating that a pancake is being prepared, and then call the function for the next pancake until there are no pancakes left.

Example call: `prepare_pancakes(3)` should produce the following outputs:
```
Pancake 1 is being prepared.
Pancake 2 is being prepared.
Pancake 3 is being prepared.
```

Implement the function so that it receives the number of pancakes as an argument and works recursively.

## Code Framework
```python
def prepare_pancakes(count):
    ## Insert code here
```

## Model Solution
```python
def prepare_pancakes(count, current=1):
    if current > count:
        return
    print(f'Pancake {current} is being prepared.')
    prepare_pancakes(count, current + 1)

prepare_pancakes(3)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import prepare_pancakes

class TestPreparePancakes(unittest.TestCase):
    def test_three_pancakes(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        prepare_pancakes(3)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pancake 1 is being prepared.\nPancake 2 is being prepared.\nPancake 3 is being prepared.")

    def test_no_pancakes(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        prepare_pancakes(0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

    def test_one_pancake(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        prepare_pancakes(1)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pancake 1 is being prepared.")

    def test_five_pancakes(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        prepare_pancakes(5)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pancake 1 is being prepared.\nPancake 2 is being prepared.\nPancake 3 is being prepared.\nPancake 4 is being prepared.\nPancake 5 is being prepared.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 477
