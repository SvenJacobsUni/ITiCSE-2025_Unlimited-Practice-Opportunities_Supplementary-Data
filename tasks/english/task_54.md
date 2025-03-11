# Input
- Programming Concept: For loops
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Practice Task: Introduction to For Loops in the context of Modern Gaming

Write a function named `level_up(score_list)` that takes a list of scores (integers) as an argument. The function should iterate through the list and check for each score if it is greater than or equal to 1000. If so, the function should output the message "Level Up!", otherwise "Keep Going!".

Example call:
```python
level_up([500, 1500, 800, 1200])
```

Expected output:
```
Keep Going!
Level Up!
Keep Going!
Level Up!
```

## Code Framework
```python
def level_up(score_list):
    ## Insert code here
```

## Model Solution
```python
def level_up(score_list):
    for score in score_list:
        if score >= 1000:
            print("Level Up!")
        else:
            print("Keep Going!")

level_up([500, 1500, 800, 1200])
```

## Unit Tests
```python
import unittest
from main import level_up
from io import StringIO
import sys

class TestLevelUp(unittest.TestCase):
    def test_mixed_scores(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([500, 1500, 800, 1200])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Keep Going!\nLevel Up!\nKeep Going!\nLevel Up!")

    def test_all_below_threshold(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([100, 200, 300])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Keep Going!\nKeep Going!\nKeep Going!")

    def test_all_above_threshold(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([1000, 2000, 3000])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Level Up!\nLevel Up!\nLevel Up!")

    def test_empty_list(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 472
