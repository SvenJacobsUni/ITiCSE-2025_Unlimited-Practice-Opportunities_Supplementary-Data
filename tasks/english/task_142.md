# Input
- Programming Concept: While loops; If-Else statements
- Context: Film

# Generated Task Components
## Task Description
### Exercise: Film recommendation based on ratings

Write a function named `film_recommendation(ratings)` that takes a list of ratings (numbers from 1 to 5) as an argument. The function should calculate the average rating and provide a recommendation based on this rating.

- If the average rating is 4 or higher, the function should return "Highly recommended!"
- If the average rating is between 3 and 4, the function should return "Recommended"
- If the average rating is between 2 and 3, the function should return "Average"
- If the average rating is below 2, the function should return "Not recommended"

Example call:
```python
print(film_recommendation([5, 4, 3, 4, 5]))  # Output: "Highly recommended!"
```

## Code Framework
```python
def film_recommendation(ratings):
    ## Insert code here
```

## Model Solution
```python
def film_recommendation(ratings):
    avg = sum(ratings) / len(ratings)
    if avg >= 4:
        return "Highly recommended!"
    elif avg >= 3:
        return "Recommended"
    elif avg >= 2:
        return "Average"
    else:
        return "Not recommended"

print(film_recommendation([5, 4, 3, 4, 5]))
```

## Unit Tests
```python
import unittest
from main import film_recommendation

class TestFilmRecommendation(unittest.TestCase):
    def test_highly_recommended(self):
        self.assertEqual(film_recommendation([5, 4, 4, 5, 5]), "Highly recommended!")

    def test_recommended(self):
        self.assertEqual(film_recommendation([3, 3, 4, 3, 3]), "Recommended")

    def test_average(self):
        self.assertEqual(film_recommendation([2, 2, 3, 2, 2]), "Average")

    def test_not_recommended(self):
        self.assertEqual(film_recommendation([1, 1, 2, 1, 1]), "Not recommended")

    def test_empty_list(self):
        with self.assertRaises(ZeroDivisionError):
            film_recommendation([])

    def test_single_element(self):
        self.assertEqual(film_recommendation([5]), "Highly recommended!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 574
