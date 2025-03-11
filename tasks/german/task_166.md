# Input
- Programmierkonzept: Integer;For-Schleifen;Funktionen höherer Ordnung
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beliebteste Filme auf Streaming-Diensten

Schreibe eine Funktion namens `beliebteste_filme(filme, bewertungen)`, die eine Liste von Filmen und eine Liste von Bewertungen als Argumente erhält. Jeder Film in der Liste `filme` hat eine entsprechende Bewertung in der Liste `bewertungen` an der gleichen Position. Die Funktion soll die Filme zurückgeben, die eine Bewertung von 8 oder höher haben.

Verwende eine For-Schleife, um durch die Listen zu iterieren, und eine Funktion höherer Ordnung, um die gefilterten Filme zurückzugeben.

Beispielaufruf:
```python
filme = ["Film A", "Film B", "Film C", "Film D"]
bewertungen = [7, 9, 8, 6]
print(beliebteste_filme(filme, bewertungen))
```

Erwartete Ausgabe:
```
['Film B', 'Film C']
```

## Codegerüst
```python
def beliebteste_filme(filme, bewertungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beliebteste_filme(filme, bewertungen):
    return [film for film, bewertung in zip(filme, bewertungen) if bewertung >= 8]

filme = ["Film A", "Film B", "Film C", "Film D"]
bewertungen = [7, 9, 8, 6]
print(beliebteste_filme(filme, bewertungen))
```

## Unit Tests
```python
import unittest
from main import beliebteste_filme

class TestBeliebtesteFilme(unittest.TestCase):
    def test_alle_filme_beliebt(self):
        filme = ["Film A", "Film B", "Film C"]
        bewertungen = [8, 9, 10]
        self.assertEqual(beliebteste_filme(filme, bewertungen), ["Film A", "Film B", "Film C"])

    def test_keine_filme_beliebt(self):
        filme = ["Film A", "Film B", "Film C"]
        bewertungen = [7, 6, 5]
        self.assertEqual(beliebteste_filme(filme, bewertungen), [])

    def test_gemischte_bewertungen(self):
        filme = ["Film A", "Film B", "Film C", "Film D"]
        bewertungen = [7, 9, 8, 6]
        self.assertEqual(beliebteste_filme(filme, bewertungen), ["Film B", "Film C"])

    def test_leere_liste(self):
        filme = []
        bewertungen = []
        self.assertEqual(beliebteste_filme(filme, bewertungen), [])

    def test_grenzwert_bewertung(self):
        filme = ["Film A", "Film B", "Film C"]
        bewertungen = [8, 7, 8]
        self.assertEqual(beliebteste_filme(filme, bewertungen), ["Film A", "Film C"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 598
