# Input
- Programming Concept: Tuple
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Mental Health and Well-Being

Write a function named `mental_health(data)`, which takes a tuple containing information about a person's mental health and returns an appropriate message. The tuple contains the following information in this order:

1. Name of the person (String)
2. Number of hours of sleep per night (Integer)
3. Number of hours of physical activity per week (Integer)
4. Number of hours spent on relaxation activities per week (Integer)

The function should return a message that includes the person's name and an assessment of their mental health based on the given data. Example call:

```python
mental_health(("Max", 7, 5, 3))
```

The function might return a message like:

```python
"Max, your mental health seems to be in good condition!"
```

or

```python
"Max, it might be helpful to plan more time for relaxation."
```

## Code Framework
```python
def mental_health(data):
    ## Insert code here
```

## Model Solution
```python
def mental_health(data):
    name, sleep, activity, relaxation = data
    if sleep >= 7 and activity >= 5 and relaxation >= 3:
        return f"{name}, your mental health seems to be in good condition!"
    else:
        return f"{name}, it might be helpful to plan more time for relaxation."

print(mental_health(("Max", 7, 5, 3)))
print(mental_health(("Anna", 6, 4, 2)))
```

## Unit Tests
```python
import unittest

class TestMentalHealth(unittest.TestCase):
    def test_good_condition(self):
        self.assertEqual(mental_health(("Max", 7, 5, 3)), "Max, your mental health seems to be in good condition!")

    def test_more_relaxation_needed(self):
        self.assertEqual(mental_health(("Anna", 6, 4, 2)), "Anna, it might be helpful to plan more time for relaxation.")

    def test_more_sleep_needed(self):
        self.assertEqual(mental_health(("Tom", 6, 5, 3)), "Tom, it might be helpful to plan more time for relaxation.")

    def test_more_activity_needed(self):
        self.assertEqual(mental_health(("Lisa", 7, 4, 3)), "Lisa, it might be helpful to plan more time for relaxation.")

    def test_more_relaxation_and_activity_needed(self):
        self.assertEqual(mental_health(("John", 7, 4, 2)), "John, it might be helpful to plan more time for relaxation.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 475
