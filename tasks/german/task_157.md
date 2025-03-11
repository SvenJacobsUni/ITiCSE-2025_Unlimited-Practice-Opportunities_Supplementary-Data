# Input
- Programmierkonzept: Funktionen als Variablen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Listen
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Virtuelle Realität - Benutzerverwaltung

In einem virtuellen Realitätssystem sollen Benutzer verwaltet werden. Jeder Benutzer hat einen Namen und ein Alter. Schreibe eine Funktion `benutzer_verwalten(benutzer_liste)`, die eine Liste von Benutzernamen und deren Alter als Eingabe erhält und folgende Aufgaben erfüllt:

1. **Erstelle eine Liste der Benutzer, die älter als 18 Jahre sind.**
2. **Erstelle eine Liste der Benutzer, die jünger oder gleich 18 Jahre alt sind.**
3. **Gib die Anzahl der Benutzer in jeder Liste zurück.**

Die Funktion soll ein Dictionary zurückgeben, das die Anzahl der Benutzer in den beiden Listen enthält. Das Dictionary soll die folgenden Schlüssel haben: `"erwachsene"` und `"minderjaehrige"`.

Beispielaufruf:
```python
benutzer_liste = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
ergebnis = benutzer_verwalten(benutzer_liste)
print(ergebnis)  # Ausgabe: {"erwachsene": 2, "minderjaehrige": 2}
```

Implementiere die Funktion `benutzer_verwalten(benutzer_liste)`, um die oben genannten Anforderungen zu erfüllen.

## Codegerüst
```python
def benutzer_verwalten(benutzer_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def benutzer_verwalten(benutzer_liste):
    erwachsene = [b for b in benutzer_liste if b[1] > 18]
    minderjaehrige = [b for b in benutzer_liste if b[1] <= 18]
    return {"erwachsene": len(erwachsene), "minderjaehrige": len(minderjaehrige)}

benutzer_liste = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
ergebnis = benutzer_verwalten(benutzer_liste)
print(ergebnis)
```

## Unit Tests
```python
import unittest
from main import benutzer_verwalten

class TestBenutzerVerwalten(unittest.TestCase):
    def test_gemischte_benutzer(self):
        benutzer_liste = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
        self.assertEqual(benutzer_verwalten(benutzer_liste), {"erwachsene": 2, "minderjaehrige": 2})

    def test_nur_erwachsene(self):
        benutzer_liste = [("Alice", 22), ("Charlie", 19)]
        self.assertEqual(benutzer_verwalten(benutzer_liste), {"erwachsene": 2, "minderjaehrige": 0})

    def test_nur_minderjaehrige(self):
        benutzer_liste = [("Bob", 17), ("Diana", 15)]
        self.assertEqual(benutzer_verwalten(benutzer_liste), {"erwachsene": 0, "minderjaehrige": 2})

    def test_leere_liste(self):
        benutzer_liste = []
        self.assertEqual(benutzer_verwalten(benutzer_liste), {"erwachsene": 0, "minderjaehrige": 0})

    def test_grenzwert_18(self):
        benutzer_liste = [("Alice", 18), ("Bob", 18)]
        self.assertEqual(benutzer_verwalten(benutzer_liste), {"erwachsene": 0, "minderjaehrige": 2})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 589
