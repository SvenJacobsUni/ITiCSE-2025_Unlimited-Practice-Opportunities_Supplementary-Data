# Input
- Programming Concept: Functions as Variables
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Functions as Variables in Virtual Reality

In virtual reality (VR), various actions can be represented by functions. Write a function `execute_action(action)`, which takes an action as a parameter and executes that action. The action is represented by a function that has no parameters and returns a message.

Define two example actions:
1. `start_vr()`: Returns the message "VR started!".
2. `end_vr()`: Returns the message "VR ended!".

The function `execute_action(action)` should execute the given action and return the corresponding message.

Example calls:
```python
print(execute_action(start_vr))  # Output: "VR started!"
print(execute_action(end_vr))  # Output: "VR ended!"
```

## Code Framework
```python
def execute_action(action):
    ## Insert code here


def start_vr():
    ## Insert code here


def end_vr():
    ## Insert code here

```

## Model Solution
```python
def execute_action(action):
    return action()


def start_vr():
    return "VR started!"


def end_vr():
    return "VR ended!"


print(execute_action(start_vr))
print(execute_action(end_vr))
```

## Unit Tests
```python
import unittest
from main import execute_action, start_vr, end_vr


class TestExecuteAction(unittest.TestCase):
    def test_start_vr(self):
        self.assertEqual(execute_action(start_vr), "VR started!")


    def test_end_vr(self):
        self.assertEqual(execute_action(end_vr), "VR ended!")


if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 428
