# Input
- Programming Concept: String
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise Task: Social Media - Hashtag Extraction

Write a function named `extract_hashtags(text)` that extracts all hashtags from a given text and returns them as a list. A hashtag starts with the character `#` and ends with a space or the end of the text. 

Sample call:
```python
extract_hashtags("Loving the new features of our app! #excited #newrelease #tech")
```

should return the list `["#excited", "#newrelease", "#tech"]`.

## Code Framework
```python
def extract_hashtags(text):
    ## Insert code here
```

## Model Solution
```python
def extract_hashtags(text):
    return [word for word in text.split() if word.startswith('#')]

print(extract_hashtags("Loving the new features of our app! #excited #newrelease #tech"))
```

## Unit Tests
```python
import unittest

from main import extract_hashtags

class TestExtractHashtags(unittest.TestCase):
    def test_simple_text(self):
        self.assertEqual(extract_hashtags("Loving the new features of our app! #excited #newrelease #tech"), ["#excited", "#newrelease", "#tech"])

    def test_text_without_hashtags(self):
        self.assertEqual(extract_hashtags("This is a simple text without hashtags."), [])

    def test_text_with_one_hashtag(self):
        self.assertEqual(extract_hashtags("Check out our new product! #innovation"), ["#innovation"])

    def test_text_with_hashtags_at_start(self):
        self.assertEqual(extract_hashtags("#start your day with a smile! #happy #positive"), ["#start", "#happy", "#positive"])

    def test_text_with_hashtags_at_end(self):
        self.assertEqual(extract_hashtags("End your day with a good book. #reading #relaxing"), ["#reading", "#relaxing"])

    def test_text_with_mixed_characters(self):
        self.assertEqual(extract_hashtags("Coding is fun! #100DaysOfCode #Python3 #AI&ML"), ["#100DaysOfCode", "#Python3", "#AI&ML"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 481
