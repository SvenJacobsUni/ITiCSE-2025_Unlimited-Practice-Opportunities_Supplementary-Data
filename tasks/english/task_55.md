# Input
- Programming Concept: Functions as variables
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Functions as Variables in the Context of Sports

Write a function `sport_selection(sport)` that returns another function as a variable. The returned function should output a message specific to the chosen sport.

Define at least three different sports and the corresponding functions that output a message for each sport.

Example call:
```python
soccer_function = sport_selection("Soccer")
soccer_function()  # Outputs a message for Soccer

basketball_function = sport_selection("Basketball")
basketball_function()  # Outputs a message for Basketball
```

Expected messages might be:
- For "Soccer": "You have chosen Soccer! An exciting game on the field."
- For "Basketball": "You have chosen Basketball! A dynamic game on the court."
- For "Tennis": "You have chosen Tennis! An intense match on the court."

Implement the function `sport_selection(sport)` and the corresponding functions for the sports.

## Code Framework
```python
def sport_selection(sport):
    ## Insert code here

def soccer():
    ## Insert code here

def basketball():
    ## Insert code here

def tennis():
    ## Insert code here

```

## Model Solution
```python
def sport_selection(sport):
    if sport == "Soccer":
        return soccer
    elif sport == "Basketball":
        return basketball
    elif sport == "Tennis":
        return tennis

def soccer():
    print("You have chosen Soccer! An exciting game on the field.")

def basketball():
    print("You have chosen Basketball! A dynamic game on the court.")

def tennis():
    print("You have chosen Tennis! An intense match on the court.")

# Example calls
soccer_function = sport_selection("Soccer")
soccer_function()

basketball_function = sport_selection("Basketball")
basketball_function()

tennis_function = sport_selection("Tennis")
tennis_function()

```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import sport_selection

class TestSportSelection(unittest.TestCase):
    def test_soccer(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_selection("Soccer")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "You have chosen Soccer! An exciting game on the field.")

    def test_basketball(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_selection("Basketball")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "You have chosen Basketball! A dynamic game on the court.")

    def test_tennis(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_selection("Tennis")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "You have chosen Tennis! An intense match on the court.")

    def test_unknown_sport(self):
        self.assertIsNone(sport_selection("Handball"))

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 473
