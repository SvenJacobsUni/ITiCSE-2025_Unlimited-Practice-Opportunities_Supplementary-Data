# Input
- Programming Concept: Functions as variables
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Functions as Variables in the Context of Mental Health

Write a function `mental_health(days)` that takes a list of days of the week as input. Each day is a string representing the name of the day (e.g. "Monday", "Tuesday", etc.). The function should select and return a random activity to promote mental health for each day.

Define three separate functions:
1. `meditation()`: Returns the string "Meditation".
2. `walk()`: Returns the string "Walk in the park".
3. `read()`: Returns the string "Read a good book".

The function `mental_health(days)` should return a list of activities, where a random activity from the three is selected for each day.

Example call:
```python
print(mental_health(["Monday", "Tuesday", "Wednesday"]))
```

Possible output:
```python
["Meditation", "Walk in the park", "Read a good book"]

## Code Framework
```python
def meditation():
    ## Insert code here

def walk():
    ## Insert code here

def read():
    ## Insert code here

def mental_health(days):
    ## Insert code here
```

## Model Solution
```python
import random

def meditation():
    return "Meditation"

def walk():
    return "Walk in the park"

def read():
    return "Read a good book"

def mental_health(days):
    activities = [meditation, walk, read]
    return [random.choice(activities)() for day in days]

print(mental_health(["Monday", "Tuesday", "Wednesday"]))
```

## Unit Tests
```python
import unittest
from main import meditation, walk, read, mental_health

class TestMentalHealth(unittest.TestCase):
    def test_meditation(self):
        self.assertEqual(meditation(), "Meditation")

    def test_walk(self):
        self.assertEqual(walk(), "Walk in the park")

    def test_read(self):
        self.assertEqual(read(), "Read a good book")

    def test_mental_health(self):
        days = ["Monday", "Tuesday", "Wednesday"]
        result = mental_health(days)
        self.assertEqual(len(result), len(days))
        for activity in result:
            self.assertIn(activity, ["Meditation", "Walk in the park", "Read a good book"])

    def test_empty_list(self):
        self.assertEqual(mental_health([]), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 484
