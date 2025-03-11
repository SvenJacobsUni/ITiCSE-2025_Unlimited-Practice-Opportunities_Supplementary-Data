# Input
- Programming Concept: While loops
- Context: Sports

# Generated Task Components
## Task Description
### Exercise Task: Sports Repetitions

Write a function named `training_plan(repetitions)`, which uses a while loop to count and print a specific number of repetitions of an exercise. The function should take the number of repetitions as an argument and for each repetition, output a message in the form of "Repetition X", where X is the current repetition number.

Example call: `training_plan(5)` should produce the following outputs:
```
Repetition 1
Repetition 2
Repetition 3
Repetition 4
Repetition 5
```

## Code Framework
```python
def training_plan(repetitions):
    ## Insert code here

```

## Model Solution
```python
def training_plan(repetitions):
    i = 1
    while i <= repetitions:
        print(f"Repetition {i}")
        i += 1

training_plan(5)

```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import training_plan

class TestTrainingPlan(unittest.TestCase):
    def test_five_repetitions(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        training_plan(5)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Repetition 1\nRepetition 2\nRepetition 3\nRepetition 4\nRepetition 5")

    def test_no_repetitions(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        training_plan(0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

    def test_one_repetition(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        training_plan(1)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Repetition 1")

    def test_ten_repetitions(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        training_plan(10)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Repetition 1\nRepetition 2\nRepetition 3\nRepetition 4\nRepetition 5\nRepetition 6\nRepetition 7\nRepetition 8\nRepetition 9\nRepetition 10")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 430
