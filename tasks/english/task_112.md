# Input
- Programming Concept: Tuples; Functions as variables
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise Task: Mental Health - Mood Analysis

Write a function named `mood_analysis(mood)` that takes a mood as a tuple and returns a corresponding message. The tuple consists of two elements: a string that describes the mood (e.g. 'happy', 'sad', 'stressed'), and an integer that indicates the intensity of the mood on a scale from 1 to 10.

The function should return a message that describes the mood and its intensity. Use a second function named `generate_message` that creates the message based on the given values.

Example call:
```python
mood_analysis(('happy', 8))
```

Example output:
```python
'You feel very happy with an intensity of 8.'
```

## Code Framework
```python
def mood_analysis(mood):
    ## Insert code here


def generate_message(mood, intensity):
    ## Insert code here

```

## Model Solution
```python
def mood_analysis(mood):
    print(generate_message(mood[0], mood[1]))


def generate_message(mood, intensity):
    return f'You feel very {mood} with an intensity of {intensity}.'


mood_analysis(('happy', 8))

```

## Unit Tests
```python
import unittest
from main import mood_analysis, generate_message


class TestMoodAnalysis(unittest.TestCase):
    def test_happy(self):
        self.assertEqual(generate_message('happy', 8), 'You feel very happy with an intensity of 8.')

    def test_sad(self):
        self.assertEqual(generate_message('sad', 3), 'You feel very sad with an intensity of 3.')

    def test_stressed(self):
        self.assertEqual(generate_message('stressed', 10), 'You feel very stressed with an intensity of 10.')

    def test_neutral(self):
        self.assertEqual(generate_message('neutral', 5), 'You feel very neutral with an intensity of 5.')


if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 544
