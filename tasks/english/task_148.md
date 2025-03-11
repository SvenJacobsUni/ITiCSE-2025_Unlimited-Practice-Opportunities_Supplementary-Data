# Input
- Programming Concept: String;Integer
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Mental Health

Write a function named `mood_analysis(mood)` that takes a mood as a string and returns an appropriate message. The mood can be either "happy", "sad", or "stressed".

- For "happy", the function should return "That's great! Keep it up!".
- For "sad", the function should return "It's okay to be sad. Talk to someone about it.".
- For "stressed", the function should return "Try to take a break and relax.".

Example calls:
- `mood_analysis("happy")` returns "That's great! Keep it up!".
- `mood_analysis("sad")` returns "It's okay to be sad. Talk to someone about it.".
- `mood_analysis("stressed")` returns "Try to take a break and relax.".

## Code Framework
```python
def mood_analysis(mood):
    ## Insert code here
```

## Model Solution
```python
def mood_analysis(mood):
    if mood == "happy":
        return "That's great! Keep it up!"
    elif mood == "sad":
        return "It's okay to be sad. Talk to someone about it."
    elif mood == "stressed":
        return "Try to take a break and relax."

print(mood_analysis("happy"))
print(mood_analysis("sad"))
print(mood_analysis("stressed"))
```

## Unit Tests
```python
import unittest
from main import mood_analysis

class TestMoodAnalysis(unittest.TestCase):
    def test_happy(self):
        self.assertEqual(mood_analysis("happy"), "That's great! Keep it up!")

    def test_sad(self):
        self.assertEqual(mood_analysis("sad"), "It's okay to be sad. Talk to someone about it.")

    def test_stressed(self):
        self.assertEqual(mood_analysis("stressed"), "Try to take a break and relax.")

    def test_unknown_mood(self):
        self.assertIsNone(mood_analysis("unknown"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 580
