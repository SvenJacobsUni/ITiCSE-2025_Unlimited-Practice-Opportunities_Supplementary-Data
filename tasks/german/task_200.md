# Input
- Programmierkonzept: Listen;Operationen mit Zahlen;If-Else-Anweisungen
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungen und Altersunterschiede

Schreibe eine Funktion namens `altersunterschiede(beziehungen)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel enthält zwei Namen und deren jeweiliges Alter. Die Funktion soll für jedes Paar den Altersunterschied berechnen und eine entsprechende Nachricht zurückgeben.

Die Nachrichten sollen wie folgt aussehen:
- Wenn der Altersunterschied weniger als 5 Jahre beträgt: "`[Name1] und [Name2] sind fast gleich alt.`"
- Wenn der Altersunterschied zwischen 5 und 10 Jahren liegt: "`[Name1] ist etwas älter/jünger als [Name2].`"
- Wenn der Altersunterschied mehr als 10 Jahre beträgt: "`[Name1] und [Name2] haben einen großen Altersunterschied.`"

Beispielaufruf:
```python
beziehungen = [("Anna", 25, "Ben", 30), ("Clara", 40, "David", 50), ("Eva", 20, "Frank", 35)]
altersunterschiede(beziehungen)
```

Erwartete Ausgabe:
```
Anna und Ben sind fast gleich alt.
Clara ist etwas älter als David.
Eva und Frank haben einen großen Altersunterschied.
```

## Codegerüst
```python
def altersunterschiede(beziehungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def altersunterschiede(beziehungen):
    for b in beziehungen:
        name1, age1, name2, age2 = b
        diff = abs(age1 - age2)
        if diff < 5:
            print(f"{name1} und {name2} sind fast gleich alt.")
        elif 5 <= diff <= 10:
            if age1 > age2:
                print(f"{name1} ist etwas älter als {name2}.")
            else:
                print(f"{name1} ist etwas jünger als {name2}.")
        else:
            print(f"{name1} und {name2} haben einen großen Altersunterschied.")

beziehungen = [("Anna", 25, "Ben", 30), ("Clara", 40, "David", 50), ("Eva", 20, "Frank", 35)]
altersunterschiede(beziehungen)
```

## Unit Tests
```python
import unittest
from main import altersunterschiede

class TestAltersunterschiede(unittest.TestCase):
    def test_fast_gleich_alt(self):
        beziehungen = [("Anna", 25, "Ben", 27)]
        expected_output = "Anna und Ben sind fast gleich alt.\n"
        with self.assertLogs(level='INFO') as log:
            altersunterschiede(beziehungen)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_etwas_aelter(self):
        beziehungen = [("Clara", 40, "David", 45)]
        expected_output = "Clara ist etwas älter als David.\n"
        with self.assertLogs(level='INFO') as log:
            altersunterschiede(beziehungen)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_grosser_altersunterschied(self):
        beziehungen = [("Eva", 20, "Frank", 35)]
        expected_output = "Eva und Frank haben einen großen Altersunterschied.\n"
        with self.assertLogs(level='INFO') as log:
            altersunterschiede(beziehungen)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_etwas_juenger(self):
        beziehungen = [("Gina", 30, "Hank", 35)]
        expected_output = "Gina ist etwas jünger als Hank.\n"
        with self.assertLogs(level='INFO') as log:
            altersunterschiede(beziehungen)
            self.assertIn(expected_output.strip(), log.output[0])

    def test_randbedingungen(self):
        beziehungen = [("Ivy", 18, "Jack", 18), ("Kate", 20, "Leo", 30), ("Mia", 25, "Nate", 35)]
        expected_outputs = [
            "Ivy und Jack sind fast gleich alt.\n",
            "Kate und Leo haben einen großen Altersunterschied.\n",
            "Mia und Nate haben einen großen Altersunterschied.\n"
        ]
        with self.assertLogs(level='INFO') as log:
            altersunterschiede(beziehungen)
            for expected_output in expected_outputs:
                self.assertIn(expected_output.strip(), log.output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 632
