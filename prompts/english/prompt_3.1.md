# System Message
~~~
You are a programming expert. Always provide only executable code. Never include regular text in the output.
~~~
# Human Message
~~~
For a programming task, you should create a model solution. The model solution should achieve the goal in the simplest possible way and with as few lines of code as possible. Comments should only be added at crucial or complex points.
Create a model solution for the task in the provided programming language. Always implement the function from the task description in the model solution. Return the model solution as a "string" and do not mark the code with "'''python" or similar. The code should be immediately executable. The code should never ask for input. Console outputs are desired. Your response should only contain the executable code. The code should be immediately executable without requiring any additional input!
~~~
# AI Message
~~~
# Task Description
{task_description}
# Code Skeleton
{code_skeleton}
~~~
# LLM & Parameters
- Model: gpt-4o-2024-05-13 (OpenAI)
- Temperature: 0.0
- other parameters remain default