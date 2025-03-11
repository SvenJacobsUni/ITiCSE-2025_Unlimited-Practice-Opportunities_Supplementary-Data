# Input
- Programming Concept: For loops
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Highscore List in Modern Gaming

Write a function named `highscore_list(scores)` that receives a list of player scores as an argument. The function should sort the player scores in descending order and return the top 5 scores. If there are fewer than 5 scores, all available scores should be returned.

Example call:
```python
highscore_list([1500, 3000, 2500, 5000, 1000, 2000])
```

Expected return:
```python
[5000, 3000, 2500, 2000, 1500]
```

## Code Framework
```python
def highscore_list(scores):
    ## Insert code here
```

## Model Solution
```python
def highscore_list(scores):
    return sorted(scores, reverse=True)[:5]

print(highscore_list([1500, 3000, 2500, 5000, 1000, 2000]))
```

## Unit Tests
```python
import unittest
from main import highscore_list

class TestHighscoreList(unittest.TestCase):
    def test_more_than_five_scores(self):
        self.assertEqual(highscore_list([1500, 3000, 2500, 5000, 1000, 2000]), [5000, 3000, 2500, 2000, 1500])

    def test_exactly_five_scores(self):
        self.assertEqual(highscore_list([1500, 3000, 2500, 5000, 1000]), [5000, 3000, 2500, 1500, 1000])

    def test_less_than_five_scores(self):
        self.assertEqual(highscore_list([1500, 3000, 2500]), [3000, 2500, 1500])

    def test_empty_list(self):
        self.assertEqual(highscore_list([]), [])

    def test_all_scores_equal(self):
        self.assertEqual(highscore_list([1000, 1000, 1000, 1000, 1000, 1000]), [1000, 1000, 1000, 1000, 1000])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 419
