# Input
- Programmierkonzept: For-Schleifen
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungen und For-Schleifen

Schreibe eine Funktion namens `beziehungsstatus(liste)`, die eine Liste von Namen als Argument erhält. Die Funktion soll für jeden Namen in der Liste eine Nachricht ausgeben, die den Beziehungsstatus der Person beschreibt. Verwende eine For-Schleife, um durch die Liste zu iterieren und die Nachrichten zu generieren.

Beispielaufruf:
```python
beziehungsstatus(["Anna", "Ben", "Clara"])
```

Beispielausgabe:
```
Anna ist Single.
Ben ist in einer Beziehung.
Clara ist verheiratet.
```

Hinweis: Die Nachrichten können für jeden Namen gleich sein, es geht darum, die For-Schleife zu üben.

## Codegerüst
```python
def beziehungsstatus(liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(liste):
    for name in liste:
        print(f"{name} ist Single.")

beziehungsstatus(["Anna", "Ben", "Clara"])
```

## Unit Tests
```python
import unittest
from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(beziehungsstatus([]), [])

    def test_ein_name(self):
        self.assertEqual(beziehungsstatus(["Anna"]), ["Anna ist Single."])

    def test_mehrere_namen(self):
        self.assertEqual(beziehungsstatus(["Anna", "Ben", "Clara"]), ["Anna ist Single.", "Ben ist Single.", "Clara ist Single."])

    def test_namen_mit_leerzeichen(self):
        self.assertEqual(beziehungsstatus([" Anna ", " Ben ", " Clara "]), [" Anna  ist Single.", " Ben  ist Single.", " Clara  ist Single."])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 421
