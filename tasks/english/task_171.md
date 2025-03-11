# Input
- Programming Concept: If-Else statements;For loops;Tuples
- Context: Basketball

# Generated Task Components
## Task Description
### Exercise: Basketball Statistics

Write a function named `evaluate_player(player_statistics)` that takes a list of tuples as an argument. Each tuple contains a player's name and the number of points scored in a game. The function should evaluate the players and return an appropriate message.

- If a player scores more than 20 points, the message should be "Excellent, [Name]!"
- If a player scores between 10 and 20 points, the message should be "Well done, [Name]!"
- If a player scores less than 10 points, the message should be "Keep it up, [Name]!"

Example call:
```python
player_statistics = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
evaluate_player(player_statistics)
```

Expected output:
```
Excellent, Anna!
Well done, Ben!
Keep it up, Chris!
```

## Code Framework
```python
def evaluate_player(player_statistics):
    ## Insert code here

```

## Model Solution
```python
def evaluate_player(player_statistics):
    for name, points in player_statistics:
        if points > 20:
            print(f"Excellent, {name}!")
        elif 10 <= points <= 20:
            print(f"Well done, {name}!")
        else:
            print(f"Keep it up, {name}!")

player_statistics = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
evaluate_player(player_statistics)

```

## Unit Tests
```python
import unittest
from main import evaluate_player

class TestEvaluatePlayer(unittest.TestCase):
    def test_excellent(self):
        player_statistics = [("Anna", 25)]
        expected_output = "Excellent, Anna!\n"
        with self.assertLogs(level='INFO') as log:
            evaluate_player(player_statistics)
            self.assertEqual(log.output, [expected_output])

    def test_well_done(self):
        player_statistics = [("Ben", 15)]
        expected_output = "Well done, Ben!\n"
        with self.assertLogs(level='INFO') as log:
            evaluate_player(player_statistics)
            self.assertEqual(log.output, [expected_output])

    def test_keep_it_up(self):
        player_statistics = [("Chris", 8)]
        expected_output = "Keep it up, Chris!\n"
        with self.assertLogs(level='INFO') as log:
            evaluate_player(player_statistics)
            self.assertEqual(log.output, [expected_output])

    def test_mixed_evaluations(self):
        player_statistics = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
        expected_output = [
            "Excellent, Anna!\n",
            "Well done, Ben!\n",
            "Keep it up, Chris!\n"
        ]
        with self.assertLogs(level='INFO') as log:
            evaluate_player(player_statistics)
            self.assertEqual(log.output, expected_output)

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 603
