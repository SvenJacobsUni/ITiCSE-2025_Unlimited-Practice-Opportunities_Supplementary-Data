# Input
- Programmierkonzept: Float;While-Schleifen
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Vergnügungspark - Fahrgeschäftsüberprüfung

Schreibe eine Funktion namens `fahrgeschaeft_ueberpruefung(fahrzeit)`, die die Funktionalität eines Fahrgeschäfts in einem Vergnügungspark überprüft. Die Funktion soll eine float-Zahl `fahrzeit` als Parameter erhalten, die die Dauer einer Fahrt in Minuten angibt. 

Die Funktion soll eine While-Schleife verwenden, um die Fahrzeit zu überprüfen. Wenn die Fahrzeit weniger als 2 Minuten beträgt, soll die Schleife die Fahrzeit um 0.5 Minuten erhöhen und eine Nachricht ausgeben, dass die Fahrzeit zu kurz ist. Sobald die Fahrzeit 2 Minuten oder mehr beträgt, soll die Schleife beendet werden und eine Nachricht ausgegeben werden, dass die Fahrzeit akzeptabel ist.

Beispielaufruf:
```python
fahrgeschaeft_ueberpruefung(1.0)
```

Erwartete Ausgabe:
```
Fahrzeit zu kurz: 1.0 Minuten
Fahrzeit zu kurz: 1.5 Minuten
Fahrzeit akzeptabel: 2.0 Minuten
```

## Codegerüst
```python
def fahrgeschaeft_ueberpruefung(fahrzeit):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fahrgeschaeft_ueberpruefung(fahrzeit):
    while fahrzeit < 2:
        print(f"Fahrzeit zu kurz: {fahrzeit} Minuten")
        fahrzeit += 0.5
    print(f"Fahrzeit akzeptabel: {fahrzeit} Minuten")

fahrgeschaeft_ueberpruefung(1.0)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import fahrgeschaeft_ueberpruefung

class TestFahrgeschaeftUeberpruefung(unittest.TestCase):
    def test_fahrzeit_zu_kurz(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        fahrgeschaeft_ueberpruefung(1.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Fahrzeit zu kurz: 1.0 Minuten\nFahrzeit zu kurz: 1.5 Minuten\nFahrzeit akzeptabel: 2.0 Minuten")

    def test_fahrzeit_akzeptabel(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        fahrgeschaeft_ueberpruefung(2.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Fahrzeit akzeptabel: 2.0 Minuten")

    def test_fahrzeit_ueber_akzeptabel(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        fahrgeschaeft_ueberpruefung(3.0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Fahrzeit akzeptabel: 3.0 Minuten")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 545
