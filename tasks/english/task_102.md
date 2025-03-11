# Input
- Programming Concept: Operations with numbers; For loops
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Calculate Average Running Time

Write a function called `average_running_time(times)` that receives a list of running times (in minutes) as an argument and computes and returns the average running time. The calculation should be performed using a for loop.

Example call:
```python
times = [30, 45, 50, 40, 35]
print(average_running_time(times))  # Output: 40.0
```

In this example, the running times from five runners are given in minutes. The function should calculate and return the average running time.

## Code Framework
```python
def average_running_time(times):
    ## Insert code here

```

## Model Solution
```python
def average_running_time(times):
    total = 0
    for time in times:
        total += time
    return total / len(times)

times = [30, 45, 50, 40, 35]
print(average_running_time(times))
```

## Unit Tests
```python
import unittest
from main import average_running_time

class TestAverageRunningTime(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(average_running_time([30, 45, 50, 40, 35]), 40.0)

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            average_running_time([])

    def test_single_element(self):
        self.assertEqual(average_running_time([25]), 25.0)

    def test_mixed_values(self):
        self.assertEqual(average_running_time([10, 20, 30, 40, 50]), 30.0)

    def test_same_values(self):
        self.assertEqual(average_running_time([20, 20, 20, 20, 20]), 20.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 534
