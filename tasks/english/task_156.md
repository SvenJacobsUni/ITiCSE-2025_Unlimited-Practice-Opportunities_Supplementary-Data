# Input
- Programming Concept: If-Else statements; Higher-order functions; String
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Rugby Player Evaluation

Write a function named `evaluate_player(name, points)` that takes a rugby player's name and their scored points as arguments. The function should evaluate the player based on their points and return a corresponding message.

- If the player has scored more than 20 points, the message should be: "Excellent, [Name]! You are a star player!"
- If the player has scored between 10 and 20 points (including 10 and 20), the message should be: "Well done, [Name]! You played solidly."
- If the player has scored less than 10 points, the message should be: "Chin up, [Name]! Practice makes perfect."

Example call:
```python
evaluate_player("Max", 25)
```
should return the message "Excellent, Max! You are a star player!"

## Code Framework
```python
def evaluate_player(name, points):
    ## Insert code here

```

## Model Solution
```python
def evaluate_player(name, points):
    if points > 20:
        return f"Excellent, {name}! You are a star player!"
    elif 10 <= points <= 20:
        return f"Well done, {name}! You played solidly."
    else:
        return f"Chin up, {name}! Practice makes perfect."

# Example call
evaluate_player("Max", 25)
```

## Unit Tests
```python
import unittest
from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_excellent(self):
        self.assertEqual(evaluate_player("Max", 25), "Excellent, Max! You are a star player!")

    def test_well_done(self):
        self.assertEqual(evaluate_player("Anna", 15), "Well done, Anna! You played solidly.")

    def test_chin_up(self):
        self.assertEqual(evaluate_player("Tom", 5), "Chin up, Tom! Practice makes perfect.")

    def test_boundary_20(self):
        self.assertEqual(evaluate_player("Lena", 20), "Well done, Lena! You played solidly.")

    def test_boundary_10(self):
        self.assertEqual(evaluate_player("Paul", 10), "Well done, Paul! You played solidly.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 588
