# Input
- Programmierkonzept: While-Schleifen;Boolean und None
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Streaming-Dienste und Abonnement-Status

Schreibe eine Funktion namens `check_abonnement_status(user_status)`, die den Abonnement-Status eines Benutzers in einem Streaming-Dienst überprüft. Die Funktion soll eine While-Schleife verwenden, um den Status zu überprüfen, bis der Benutzer entweder ein aktives Abonnement hat oder der Status `None` ist. 

- Wenn der Status `True` ist, soll die Funktion "Abonnement aktiv" ausgeben.
- Wenn der Status `False` ist, soll die Funktion "Abonnement inaktiv" ausgeben.
- Wenn der Status `None` ist, soll die Funktion "Status unbekannt" ausgeben und die Schleife beenden.

Beispielaufruf:
```python
check_abonnement_status([False, False, True, None])
```

Erwartete Ausgabe:
```
Abonnement inaktiv
Abonnement inaktiv
Abonnement aktiv
```

## Codegerüst
```python
def check_abonnement_status(user_status):
    ## Hier Code einfügen
```

## Musterlösung
```python
def check_abonnement_status(user_status):
    i = 0
    while i < len(user_status):
        status = user_status[i]
        if status is True:
            print("Abonnement aktiv")
            break
        elif status is False:
            print("Abonnement inaktiv")
        elif status is None:
            print("Status unbekannt")
            break
        i += 1

check_abonnement_status([False, False, True, None])
```

## Unit Tests
```python
import unittest
from main import check_abonnement_status
from io import StringIO
import sys

class TestCheckAbonnementStatus(unittest.TestCase):
    def test_abonnement_aktiv(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_abonnement_status([False, False, True, None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Abonnement inaktiv\nAbonnement inaktiv\nAbonnement aktiv")

    def test_abonnement_inaktiv(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_abonnement_status([False, None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Abonnement inaktiv\nStatus unbekannt")

    def test_status_unbekannt(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_abonnement_status([None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Status unbekannt")

    def test_leere_liste(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_abonnement_status([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 551
