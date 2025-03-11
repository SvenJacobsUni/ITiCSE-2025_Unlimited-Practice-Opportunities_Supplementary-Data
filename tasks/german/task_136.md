# Input
- Programmierkonzept: String;Integer
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus

Schreibe eine Funktion namens `beziehungsstatus(name, jahre)`, die den Beziehungsstatus einer Person basierend auf der Anzahl der Jahre in der Beziehung ausgibt. Die Funktion soll zwei Parameter entgegennehmen: `name` (ein String) und `jahre` (ein Integer). 

Die Funktion soll folgende Nachrichten zurückgeben:
- Wenn `jahre` weniger als 1 ist: "`[Name] ist frisch verliebt!`"
- Wenn `jahre` zwischen 1 und 5 liegt: "`[Name] ist in einer stabilen Beziehung.`"
- Wenn `jahre` mehr als 5 ist: "`[Name] ist in einer langjährigen Beziehung.`"

Beispielaufruf:
```python
print(beziehungsstatus("Anna", 3))  # Ausgabe: "Anna ist in einer stabilen Beziehung."
```

## Codegerüst
```python
def beziehungsstatus(name, jahre):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(name, jahre):
    if jahre < 1:
        return f"{name} ist frisch verliebt!"
    elif 1 <= jahre <= 5:
        return f"{name} ist in einer stabilen Beziehung."
    else:
        return f"{name} ist in einer langjährigen Beziehung."

print(beziehungsstatus("Anna", 3))  # Beispielaufruf
```

## Unit Tests
```python
import unittest

from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_frisch_verliebt(self):
        self.assertEqual(beziehungsstatus("Anna", 0), "Anna ist frisch verliebt!")
        self.assertEqual(beziehungsstatus("Max", -1), "Max ist frisch verliebt!")

    def test_stabile_beziehung(self):
        self.assertEqual(beziehungsstatus("Anna", 1), "Anna ist in einer stabilen Beziehung.")
        self.assertEqual(beziehungsstatus("Max", 5), "Max ist in einer stabilen Beziehung.")
        self.assertEqual(beziehungsstatus("Chris", 3), "Chris ist in einer stabilen Beziehung.")

    def test_langjaehrige_beziehung(self):
        self.assertEqual(beziehungsstatus("Anna", 6), "Anna ist in einer langjährigen Beziehung.")
        self.assertEqual(beziehungsstatus("Max", 10), "Max ist in einer langjährigen Beziehung.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 568
