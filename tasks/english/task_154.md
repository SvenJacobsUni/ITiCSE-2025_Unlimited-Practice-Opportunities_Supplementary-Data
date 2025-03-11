# Input
- Programming Concept: If-Else statements; Functions as variables; Boolean and None
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Sporting Activity

Write a function named `sport_activity(activity)` that takes a sporting activity as a string and returns an appropriate message. The function should check the following conditions:

- If the activity is "Running", it should return the message "Running is a great way to stay fit!".
- If the activity is "Swimming", it should return the message "Swimming exercises the entire body!".
- If the activity is "Cycling", it should return the message "Cycling is good for endurance!".
- For all other activities, it should return the message "That's a great sport too!".

Example calls:
- `sport_activity("Running")` returns "Running is a great way to stay fit!".
- `sport_activity("Swimming")` returns "Swimming exercises the entire body!".
- `sport_activity("Basketball")` returns "That's a great sport too!".

## Code Framework
```python
def sport_activity(activity):
    ## Insert code here
```

## Model Solution
```python
def sport_activity(activity):
    if activity == "Running":
        return "Running is a great way to stay fit!"
    elif activity == "Swimming":
        return "Swimming exercises the entire body!"
    elif activity == "Cycling":
        return "Cycling is good for endurance!"
    else:
        return "That's a great sport too!"

# Example calls
print(sport_activity("Running"))
print(sport_activity("Swimming"))
print(sport_activity("Basketball"))
```

## Unit Tests
```python
import unittest
from main import sport_activity

class TestSportActivity(unittest.TestCase):
    def test_running(self):
        self.assertEqual(sport_activity("Running"), "Running is a great way to stay fit!")

    def test_swimming(self):
        self.assertEqual(sport_activity("Swimming"), "Swimming exercises the entire body!")

    def test_cycling(self):
        self.assertEqual(sport_activity("Cycling"), "Cycling is good for endurance!")

    def test_other_activity(self):
        self.assertEqual(sport_activity("Basketball"), "That's a great sport too!")
        self.assertEqual(sport_activity("Yoga"), "That's a great sport too!")
        self.assertEqual(sport_activity("Tennis"), "That's a great sport too!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 586
