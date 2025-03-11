# Input
- Programmierkonzept: Funktionen als Variablen;Float;For-Schleifen
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Berechnung des durchschnittlichen Stresslevels

In dieser Aufgabe sollst du eine Funktion implementieren, die das durchschnittliche Stresslevel einer Person über eine Woche berechnet. Das Stresslevel wird als Liste von Fließkommazahlen (Float) für jeden Tag der Woche angegeben.

Schreibe eine Funktion namens `durchschnittliches_stresslevel(stresslevel_liste)`, die eine Liste von Fließkommazahlen als Argument nimmt und das durchschnittliche Stresslevel berechnet und zurückgibt. 

Beispielaufruf:
```python
stresslevel = [3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]
print(durchschnittliches_stresslevel(stresslevel))  # Erwartete Ausgabe: 3.9714285714285715
```

### Anforderungen:
1. Die Funktion soll eine Liste von Fließkommazahlen als Eingabe akzeptieren.
2. Die Funktion soll das durchschnittliche Stresslevel als Fließkommazahl zurückgeben.
3. Verwende eine `for`-Schleife, um die Summe der Stresslevel zu berechnen.
4. Berechne den Durchschnitt, indem du die Summe durch die Anzahl der Tage teilst.

### Kontext:
Das Stresslevel einer Person kann stark variieren und ist ein wichtiger Indikator für die psychische Gesundheit. Durch die Berechnung des durchschnittlichen Stresslevels über eine Woche hinweg kann man besser verstehen, wie gestresst eine Person im Durchschnitt ist und ob Maßnahmen zur Stressbewältigung notwendig sind.

## Codegerüst
```python
def durchschnittliches_stresslevel(stresslevel_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def durchschnittliches_stresslevel(stresslevel_liste):
    return sum(stresslevel_liste) / len(stresslevel_liste)

stresslevel = [3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]
print(durchschnittliches_stresslevel(stresslevel))
```

## Unit Tests
```python
import unittest
from main import durchschnittliches_stresslevel

class TestDurchschnittlichesStresslevel(unittest.TestCase):
    def test_durchschnitt(self):
        self.assertAlmostEqual(durchschnittliches_stresslevel([3.5, 4.0, 2.8, 5.1, 3.3, 4.2, 3.9]), 3.9714285714285715)

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittliches_stresslevel([])

    def test_ein_element(self):
        self.assertEqual(durchschnittliches_stresslevel([4.0]), 4.0)

    def test_negative_werte(self):
        self.assertAlmostEqual(durchschnittliches_stresslevel([-1.0, -2.0, -3.0]), -2.0)

    def test_gemischte_werte(self):
        self.assertAlmostEqual(durchschnittliches_stresslevel([1.0, -1.0, 1.0, -1.0]), 0.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 606
