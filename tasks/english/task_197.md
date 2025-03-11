# Input
- Programming Concept: Float;If-Else statements;Higher-order functions
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - Engagement Rate Calculation

Write a function named `calculate_engagement_rate(likes, comments, followers)` to calculate the engagement rate of a social media post. The engagement rate is determined as a percentage of the interactions (likes and comments) relative to the number of followers.

The function should execute the following steps:
1. Calculate the total number of interactions (likes + comments).
2. Calculate the engagement rate as a percentage of the interactions relative to the number of followers.
3. Return the engagement rate.

Additionally, the function should output a message evaluating the engagement rate:
- If the engagement rate is greater than or equal to 10%, output the message "High engagement rate!"
- If the engagement rate is between 5% and 10%, output the message "Average engagement rate"
- If the engagement rate is below 5%, output the message "Low engagement rate"

Example Call:
```python
calculate_engagement_rate(150, 30, 2000)
```

Expected Output:
```
Average engagement rate
```

Expected Return Value:
```python
9.0
```

## Code Framework
```python
def calculate_engagement_rate(likes, comments, followers):
    ## Insert code here
```

## Model Solution
```python
def calculate_engagement_rate(likes, comments, followers):
    interactions = likes + comments
    engagement_rate = (interactions / followers) * 100
    if engagement_rate >= 10:
        print("High engagement rate!")
    elif engagement_rate >= 5:
        print("Average engagement rate")
    else:
        print("Low engagement rate")
    return engagement_rate

# Example call
print(calculate_engagement_rate(150, 30, 2000))
```

## Unit Tests
```python
import unittest
from main import calculate_engagement_rate

class TestCalculateEngagementRate(unittest.TestCase):
    def test_high_engagement_rate(self):
        self.assertEqual(calculate_engagement_rate(200, 100, 2000), 15.0)

    def test_average_engagement_rate(self):
        self.assertEqual(calculate_engagement_rate(150, 30, 2000), 9.0)

    def test_low_engagement_rate(self):
        self.assertEqual(calculate_engagement_rate(50, 20, 2000), 3.5)

    def test_zero_followers(self):
        with self.assertRaises(ZeroDivisionError):
            calculate_engagement_rate(100, 50, 0)

    def test_no_interactions(self):
        self.assertEqual(calculate_engagement_rate(0, 0, 2000), 0.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 629
