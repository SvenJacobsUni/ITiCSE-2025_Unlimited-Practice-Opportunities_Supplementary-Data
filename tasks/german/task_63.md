# Input
- Programmierkonzept: String
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Hashtag-Extraktion

Schreibe eine Funktion namens `extrahiere_hashtags(text)`, die alle Hashtags aus einem gegebenen Text extrahiert und als Liste zurückgibt. Ein Hashtag beginnt mit dem Zeichen `#` und endet mit einem Leerzeichen oder dem Ende des Textes. 

Beispielaufruf:
```python
extrahiere_hashtags("Loving the new features of our app! #excited #newrelease #tech")
```

sollte die Liste `["#excited", "#newrelease", "#tech"]` zurückgeben.

## Codegerüst
```python
def extrahiere_hashtags(text):
    ## Hier Code einfügen
```

## Musterlösung
```python
def extrahiere_hashtags(text):
    return [word for word in text.split() if word.startswith('#')]

print(extrahiere_hashtags("Loving the new features of our app! #excited #newrelease #tech"))
```

## Unit Tests
```python
import unittest

from main import extrahiere_hashtags

class TestExtrahiereHashtags(unittest.TestCase):
    def test_einfacher_text(self):
        self.assertEqual(extrahiere_hashtags("Loving the new features of our app! #excited #newrelease #tech"), ["#excited", "#newrelease", "#tech"])

    def test_text_ohne_hashtags(self):
        self.assertEqual(extrahiere_hashtags("This is a simple text without hashtags."), [])

    def test_text_mit_einem_hashtag(self):
        self.assertEqual(extrahiere_hashtags("Check out our new product! #innovation"), ["#innovation"])

    def test_text_mit_hashtags_am_anfang(self):
        self.assertEqual(extrahiere_hashtags("#start your day with a smile! #happy #positive"), ["#start", "#happy", "#positive"])

    def test_text_mit_hashtags_am_ende(self):
        self.assertEqual(extrahiere_hashtags("End your day with a good book. #reading #relaxing"), ["#reading", "#relaxing"])

    def test_text_mit_gemischten_zeichen(self):
        self.assertEqual(extrahiere_hashtags("Coding is fun! #100DaysOfCode #Python3 #AI&ML"), ["#100DaysOfCode", "#Python3", "#AI&ML"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 481
