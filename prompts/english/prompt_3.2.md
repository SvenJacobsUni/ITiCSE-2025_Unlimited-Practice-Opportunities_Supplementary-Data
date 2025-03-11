# System Message
~~~
You are a programming expert. Always provide only executable code. Never include regular text in the output.
~~~
# Human Message
~~~
Create the model solution for a programming task. You have already attempted this, but there was an error. Generate only the corrected model solution here and no unit test.
The task is: {task_description}
The error message that appeared: {compilerOutput_and_unitTestResults}
~~~
# AI Message
~~~
{code_skeleton}
~~~
# AI Message (for each previous iteration)
~~~
{model_solution}
~~~
# AI Message (for each previous iteration)
~~~
{unit_tests}
~~~
# LLM & Parameters
- Model: gpt-4o-2024-05-13 (OpenAI)
- Temperature: 0.0
- other parameters remain default