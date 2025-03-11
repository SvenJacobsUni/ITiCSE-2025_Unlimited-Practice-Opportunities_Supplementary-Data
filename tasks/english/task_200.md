# Input
- Programming Concept: Lists; Operations with numbers; If-Else statements
- Context: Relationships

# Generated Task Components
## Task Description
### Exercise: Relationships and Age Differences

Write a function named `age_differences(relationships)`, which takes a list of tuples as argument. Each tuple contains two names and their respective ages. The function should calculate the age difference for each pair and return an appropriate message.

The messages should be as follows:
- If the age difference is less than 5 years: "`[Name1] and [Name2] are almost the same age.`"
- If the age difference is between 5 and 10 years: "`[Name1] is slightly older/younger than [Name2].`"
- If the age difference is more than 10 years: "`[Name1] and [Name2] have a large age difference.`"

Example call:
```python
relationships = [("Anna", 25, "Ben", 30), ("Clara", 40, "David", 50), ("Eva", 20, "Frank", 35)]
age_differences(relationships)
```

Expected output:
```
Anna and Ben are almost the same age.
Clara is slightly older than David.
Eva and Frank have a large age difference.
```

## Code Framework
```python
def age_differences(relationships):
    ## Insert code here
```

## Model Solution
```python
def age_differences(relationships):
    for r in relationships:
        name1, age1, name2, age2 = r
        diff = abs(age1 - age2)
        if diff < 5:
            print(f"{name1} and {name2} are almost the same age.")
        elif 5 <= diff <= 10:
            if age1 > age2:
                print(f"{name1} is slightly older than {name2}.")
            else:
                print(f"{name1} is slightly younger than {name2}.")
        else:
            print(f"{name1} and {name2} have a large age difference.")

relationships = [("Anna", 25, "Ben", 30), ("Clara", 40, "David", 50), ("Eva", 20, "Frank", 35)]
age_differences(relationships)
```

## Unit Tests
```python
import unittest
from main import age_differences

class TestAgeDifferences(unittest.TestCase):
    def test_almost_same_age(self):
        relationships = [("Anna", 25, "Ben", 27)]
        expected_output = "Anna and Ben are almost the same age.\n"
        with self.assertLogs(level='INFO') as log:
            age_differences(relationships)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_slightly_older(self):
        relationships = [("Clara", 40, "David", 45)]
        expected_output = "Clara is slightly older than David.\n"
        with self.assertLogs(level='INFO') as log:
            age_differences(relationships)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_large_age_difference(self):
        relationships = [("Eva", 20, "Frank", 35)]
        expected_output = "Eva and Frank have a large age difference.\n"
        with self.assertLogs(level='INFO') as log:
            age_differences(relationships)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_slightly_younger(self):
        relationships = [("Gina", 30, "Hank", 35)]
        expected_output = "Gina is slightly younger than Hank.\n"
        with self.assertLogs(level='INFO') as log:
            age_differences(relationships)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_edge_cases(self):
        relationships = [("Ivy", 18, "Jack", 18), ("Kate", 20, "Leo", 30), ("Mia", 25, "Nate", 35)]
        expected_outputs = [
            "Ivy and Jack are almost the same age.\n",
            "Kate and Leo have a large age difference.\n",
            "Mia and Nate have a large age difference.\n"
        ]
        with self.assertLogs(level='INFO') as log:
            age_differences(relationships)
            for expected_output in expected_outputs:
                self.assertIn(expected_output.strip(), log.output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 632
