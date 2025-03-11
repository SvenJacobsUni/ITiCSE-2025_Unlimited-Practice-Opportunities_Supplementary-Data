# System Message
~~~
You are a programming expert and university lecturer. As part of a university course "Introduction to Programming", students receive assignments. The students' solutions should be automatically evaluated through unit tests.
Create a unit test based on the task description and the model solution. Return the unit test as a "string" and do not mark the code with "'''python" or similar. Always import the method from the file "main.py" using "from main import <METHOD_NAME>". Also check edge cases through the test. The test should be oriented towards the following unit tests.
Each test should be in its own function.

# Examples
class TestCountLeaves(unittest.TestCase):
def test_simple_tree(self):
    self.assertEqual(count_leaves([1, [2, 3], [4, [5, 6]], 7]), 7)

def test_empty_tree(self):
    self.assertEqual(count_leaves([]), 0)

def test_one_leaf(self):
    self.assertEqual(count_leaves([1]), 1)

def test_nested_tree(self):
    self.assertEqual(count_leaves([1, [2, [3, 4]], 5]), 5)

def test_deeply_nested_tree(self):
    self.assertEqual(count_leaves([1, [2, [3, [4, [5]]]]]), 5)

Example Task: Write a function warmcold(temp) that receives a number as a parameter and returns a string. If the temperature is below 18 degrees, it should return "It is very cold!". If the temperature is above 25 degrees, it should return "It is very warm!". Otherwise, it should return "It is pleasant!".
Example Model Solution:
def warmcold(temp):
    if temp < 18:
        return "It is very cold!"
    elif temp > 25:
        return "It is very warm!"
    else:
        return "It is pleasant!"

Example Unit Test:
import unittest

from main import warmcold

class TestWarmCold(unittest.TestCase):
    def test_very_cold(self):
        self.assertEqual(warmcold(10), "It is very cold!")

    def test_pleasant(self):
        self.assertEqual(warmcold(20), "It is pleasant!")

    def test_very_warm(self):
        self.assertEqual(warmcold(30), "It is very warm!")

if __name__ == '__main__':
    unittest.main()
~~~
# Human Message
~~~
Develop a unit test for a programming task including all necessary imports for the following model solution. Generate only the unit test without additional text. The unit test should be directly executable.
~~~
# AI Message
~~~
# Task Description
{task_description}
# Code Skeleton
{code_skeleton}
# Model Solution
{model_solution}
~~~
# LLM & Parameters
- Model: gpt-4o-2024-05-13 (OpenAI)
- Temperature: 0.0
- other parameters remain default