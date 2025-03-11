# Input
- Programming Concept: For loops; While loops
- Context: Amusement Park

# Generated Task Components
## Task Description
### Exercise: Amusement Park - Count Rides

Write a function named `count_rides(rides)`, which receives a list of rides at an amusement park as an argument. The function should count and return the number of rides that perform a certain minimum number of rides per day. Use a for loop or while loop to iterate through the rides and perform the counting.

The list `rides` contains tuples, where each tuple includes the name of the ride and the number of rides per day. The minimum number of rides per day is 10.

Example call:
```python
rides = [("Roller Coaster", 15), ("Ferris Wheel", 8), ("Carousel", 12)]
print(count_rides(rides))  # Output: 2
```

In this example, there are two rides that perform at least 10 rides per day: "Roller Coaster" and "Carousel".

## Code Framework
```python
def count_rides(rides):
    ## Insert code here
```

## Model Solution
```python
def count_rides(rides):
    return sum(1 for _, num_rides in rides if num_rides >= 10)

rides = [("Roller Coaster", 15), ("Ferris Wheel", 8), ("Carousel", 12)]
print(count_rides(rides))  # Output: 2
```

## Unit Tests
```python
import unittest
from main import count_rides

class TestCountRides(unittest.TestCase):
    def test_count_all_rides(self):
        self.assertEqual(count_rides([("Roller Coaster", 15), ("Ferris Wheel", 8), ("Carousel", 12)]), 2)

    def test_no_rides(self):
        self.assertEqual(count_rides([]), 0)

    def test_all_below_minimum(self):
        self.assertEqual(count_rides([("Roller Coaster", 5), ("Ferris Wheel", 3), ("Carousel", 2)]), 0)

    def test_all_above_minimum(self):
        self.assertEqual(count_rides([("Roller Coaster", 15), ("Ferris Wheel", 18), ("Carousel", 12)]), 3)

    def test_exactly_minimum(self):
        self.assertEqual(count_rides([("Roller Coaster", 10), ("Ferris Wheel", 10), ("Carousel", 10)]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 554
