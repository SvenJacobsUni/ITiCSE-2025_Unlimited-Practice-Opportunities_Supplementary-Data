# Input
- Programming Concept: Float;While loops
- Context: Amusement Park

# Generated Task Components
## Task Description
Exercise Task: Amusement Park - Ride Check

Write a function named `ride_check(ride_duration)`, which checks the functionality of a ride in an amusement park. The function should receive a float number `ride_duration` as a parameter, which indicates the duration of a ride in minutes.

The function should use a while loop to verify the ride duration. If the ride duration is less than 2 minutes, the loop should increase the ride duration by 0.5 minutes and output a message that the ride duration is too short. Once the ride duration is 2 minutes or more, the loop should terminate, and a message should be output stating that the ride duration is acceptable.

Example call:
```python
ride_check(1.0)
```

Expected output:
```
Ride duration too short: 1.0 minutes
Ride duration too short: 1.5 minutes
Ride duration acceptable: 2.0 minutes
```

## Code Framework
```python
def ride_check(ride_duration):
    ## Insert code here
```

## Model Solution
```python
def ride_check(ride_duration):
    while ride_duration < 2:
        print(f"Ride duration too short: {ride_duration} minutes")
        ride_duration += 0.5
    print(f"Ride duration acceptable: {ride_duration} minutes")

ride_check(1.0)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import ride_check

class TestRideCheck(unittest.TestCase):
    def test_ride_duration_too_short(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        ride_check(1.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Ride duration too short: 1.0 minutes\nRide duration too short: 1.5 minutes\nRide duration acceptable: 2.0 minutes")

    def test_ride_duration_acceptable(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        ride_check(2.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Ride duration acceptable: 2.0 minutes")

    def test_ride_duration_over_acceptable(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        ride_check(3.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Ride duration acceptable: 3.0 minutes")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 545
