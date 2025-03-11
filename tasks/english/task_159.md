# Input
- Programming Concept: If-Else statements; Float; While loops
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - Post Rating

Write a function named `rate_post(likes, dislikes)` that calculates the rating of a post on a social media platform. The rating should be returned as a float value between -1.0 and 1.0, where:

- A rating of 1.0 means the post has only likes and no dislikes.
- A rating of -1.0 means the post has only dislikes and no likes.
- A rating of 0.0 means the post has an equal number of likes and dislikes.

The function should follow these steps:

1. Calculate the total number of ratings (likes + dislikes).
2. Calculate the rating value as `(likes - dislikes) / total number of ratings`.
3. Return the rating value.

If the total number of ratings is 0, the function should return a rating of 0.0.

Example calls:
- `rate_post(100, 50)` returns `0.3333333333333333`.
- `rate_post(0, 0)` returns `0.0`.
- `rate_post(20, 80)` returns `-0.6`.

## Code Framework
```python
def rate_post(likes, dislikes):
    ## Insert code here
```

## Model Solution
```python
def rate_post(likes, dislikes):
    total = likes + dislikes
    return (likes - dislikes) / total if total != 0 else 0.0

# Example calls
print(rate_post(100, 50))
print(rate_post(0, 0))
print(rate_post(20, 80))
```

## Unit Tests
```python
import unittest

from main import rate_post

class TestRatePost(unittest.TestCase):
    def test_only_likes(self):
        self.assertEqual(rate_post(100, 0), 1.0)

    def test_only_dislikes(self):
        self.assertEqual(rate_post(0, 100), -1.0)

    def test_equal_number(self):
        self.assertEqual(rate_post(50, 50), 0.0)

    def test_more_likes(self):
        self.assertAlmostEqual(rate_post(75, 25), 0.5)

    def test_more_dislikes(self):
        self.assertAlmostEqual(rate_post(25, 75), -0.5)

    def test_no_ratings(self):
        self.assertEqual(rate_post(0, 0), 0.0)

    def test_mixed_ratings(self):
        self.assertAlmostEqual(rate_post(100, 50), 0.3333333333333333)
        self.assertAlmostEqual(rate_post(20, 80), -0.6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 591
