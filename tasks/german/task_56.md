# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Kontext psychischer Gesundheit

Schreibe eine Funktion `filter_positive_thoughts(thoughts, filter_function)`, die eine Liste von Gedanken (`thoughts`) und eine Filterfunktion (`filter_function`) als Argumente nimmt. Die Funktion soll die `filter_function` auf jeden Gedanken anwenden und nur die positiven Gedanken zurückgeben.

Ein Gedanke wird als positiv betrachtet, wenn die `filter_function` für diesen Gedanken `True` zurückgibt.

Beispielaufruf:
```python
def is_positive(thought):
    positive_keywords = ["glücklich", "zufrieden", "erfolgreich", "geliebt"]
    return any(keyword in thought for keyword in positive_keywords)

gedanken = ["Ich fühle mich glücklich", "Heute war ein anstrengender Tag", "Ich bin zufrieden mit meiner Arbeit", "Ich fühle mich geliebt"]
positive_gedanken = filter_positive_thoughts(gedanken, is_positive)
print(positive_gedanken)
```

Erwartete Ausgabe:
```
["Ich fühle mich glücklich", "Ich bin zufrieden mit meiner Arbeit", "Ich fühle mich geliebt"]
```

Implementiere die Funktion `filter_positive_thoughts(thoughts, filter_function)`.

## Codegerüst
```python
def filter_positive_thoughts(thoughts, filter_function):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_positive_thoughts(thoughts, filter_function):
    return [thought for thought in thoughts if filter_function(thought)]

def is_positive(thought):
    positive_keywords = ["glücklich", "zufrieden", "erfolgreich", "geliebt"]
    return any(keyword in thought for keyword in positive_keywords)

gedanken = ["Ich fühle mich glücklich", "Heute war ein anstrengender Tag", "Ich bin zufrieden mit meiner Arbeit", "Ich fühle mich geliebt"]
positive_gedanken = filter_positive_thoughts(gedanken, is_positive)
print(positive_gedanken)
```

## Unit Tests
```python
import unittest
from main import filter_positive_thoughts

def is_positive(thought):
    positive_keywords = ["glücklich", "zufrieden", "erfolgreich", "geliebt"]
    return any(keyword in thought for keyword in positive_keywords)

class TestFilterPositiveThoughts(unittest.TestCase):
    def test_all_positive(self):
        thoughts = ["Ich fühle mich glücklich", "Ich bin zufrieden", "Ich fühle mich geliebt"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), thoughts)

    def test_no_positive(self):
        thoughts = ["Heute war ein anstrengender Tag", "Ich bin müde", "Es war ein schlechter Tag"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), [])

    def test_mixed_thoughts(self):
        thoughts = ["Ich fühle mich glücklich", "Heute war ein anstrengender Tag", "Ich bin zufrieden mit meiner Arbeit", "Ich fühle mich geliebt"]
        expected = ["Ich fühle mich glücklich", "Ich bin zufrieden mit meiner Arbeit", "Ich fühle mich geliebt"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), expected)

    def test_empty_list(self):
        self.assertEqual(filter_positive_thoughts([], is_positive), [])

    def test_no_keywords(self):
        thoughts = ["Ich fühle mich okay", "Es war ein Tag", "Nichts besonderes"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 474
