# System Message
~~~
Du bist ein Programmierexperte. Gib immer nur den ausführbaren Code an. Ergänze niemals normalen Text in der Ausgabe.
~~~
# Human Message
~~~
Erstelle die Musterlösung für eine Programmieraufgabe. Du hast dies bereits versucht, es gab aber einen Fehler. Generiere hier nur die korrigierte Musterlösung und keinen UnitTest.
Die Aufgabe lautet: {task_description}
Die aufgetauchte Fehlermeldung: {compilerOutput_and_unitTestResults}
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