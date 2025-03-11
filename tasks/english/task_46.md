# Input
- Programming Concept: Integer
- Context: Film

# Generated Task Components
## Task Description
### Exercise: Movie Rating

Write a function named `rate_movie(rating)` that takes a rating for a movie and returns a corresponding message. The rating is an integer value between 1 and 10.

- If the rating is between 1 and 3, it should return the message "The movie was bad."
- If the rating is between 4 and 6, it should return the message "The movie was average."
- If the rating is between 7 and 10, it should return the message "The movie was great!"

Example calls:
- `rate_movie(2)` returns "The movie was bad."
- `rate_movie(5)` returns "The movie was average."
- `rate_movie(9)` returns "The movie was great!"

## Code Framework
```python
def rate_movie(rating):
    ## Insert code here

```

## Model Solution
```python
def rate_movie(rating):
    if 1 <= rating <= 3:
        return "The movie was bad."
    elif 4 <= rating <= 6:
        return "The movie was average."
    elif 7 <= rating <= 10:
        return "The movie was great!"

# Example calls
print(rate_movie(2))
print(rate_movie(5))
print(rate_movie(9))
```

## Unit Tests
```python
import unittest
from main import rate_movie

class TestRateMovie(unittest.TestCase):
    def test_bad(self):
        self.assertEqual(rate_movie(2), "The movie was bad.")

    def test_average(self):
        self.assertEqual(rate_movie(5), "The movie was average.")

    def test_great(self):
        self.assertEqual(rate_movie(9), "The movie was great!")

    def test_lower_boundary(self):
        self.assertEqual(rate_movie(1), "The movie was bad.")

    def test_upper_boundary(self):
        self.assertEqual(rate_movie(10), "The movie was great!")

    def test_boundary_bad_average(self):
        self.assertEqual(rate_movie(3), "The movie was bad.")
        self.assertEqual(rate_movie(4), "The movie was average.")

    def test_boundary_average_great(self):
        self.assertEqual(rate_movie(6), "The movie was average.")
        self.assertEqual(rate_movie(7), "The movie was great.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 464
