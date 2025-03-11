# Input
- Programming Concept: Lists
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise Task: Modern Gaming - Highscore List

Write a function named `update_highscore(list, new_score)` that takes a list of high scores and a new score as arguments. The function should insert the new score into the list and then sort the list in descending order. If the list contains more than 10 entries, the lowest score should be removed, so the list always contains only the top 10 scores. The function should return the updated highscore list.

Example call:
```python
highscores = [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550]
new_score = 920
print(update_highscore(highscores, new_score))
```

Expected output:
```
[1000, 950, 920, 900, 850, 800, 750, 700, 650, 600]
```

## Code Framework
```python
def update_highscore(list, new_score):
    ## Insert code here
```

## Model Solution
```python
def update_highscore(list, new_score):
    list.append(new_score)
    list.sort(reverse=True)
    return list[:10]

highscores = [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550]
new_score = 920
print(update_highscore(highscores, new_score))
```

## Unit Tests
```python
import unittest
from main import update_highscore

class TestUpdateHighscore(unittest.TestCase):
    def test_new_score_middle(self):
        self.assertEqual(update_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 920), [1000, 950, 920, 900, 850, 800, 750, 700, 650, 600])

    def test_new_score_highest(self):
        self.assertEqual(update_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 1050), [1050, 1000, 950, 900, 850, 800, 750, 700, 650, 600])

    def test_new_score_lowest(self):
        self.assertEqual(update_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 500), [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550])

    def test_new_score_tenth(self):
        self.assertEqual(update_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 550), [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550])

    def test_empty_list(self):
        self.assertEqual(update_highscore([], 500), [500])

    def test_less_than_ten_scores(self):
        self.assertEqual(update_highscore([1000, 950, 900], 850), [1000, 950, 900, 850])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 460
