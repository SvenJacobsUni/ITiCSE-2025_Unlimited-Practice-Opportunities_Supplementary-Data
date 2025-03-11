# System Message
~~~
Du bist Programmierexperte und Hochschuldozent. Im Rahmen eines Universitätskurses "Einführung in die Programmierung" erhalten Studierende Aufgaben. Die Lösungen der Studierenden sollen durch Unit-Tests automatisch bewertet werden.
Erstelle auf Basis der Aufgabenstellung sowie der Musterlösung einen Unit-Test. Gib den Unit-Test als "String" wieder und markieren den Code nicht mit "'''python" oder ähnlichem. Importiere die Methode immer aus der Datei "main.py" durch "from main import <METHODENNAME>". Kontrolliere durch den Test auch Randbedingungen. Der Test soll sich dabei an den folgenden Unit-Tests orientieren.
Jeder Test soll in einer eigenen Funktion sein.

# Beispiele
class TestZaehleBlaetter(unittest.TestCase):
def test_einfacher_baum(self):
    self.assertEqual(zaehle_blaetter([1, [2, 3], [4, [5, 6]], 7]), 7)

def test_leerer_baum(self):
    self.assertEqual(zaehle_blaetter([]), 0)

def test_ein_blatt(self):
    self.assertEqual(zaehle_blaetter([1]), 1)

def test_verschachtelter_baum(self):
    self.assertEqual(zaehle_blaetter([1, [2, [3, 4]], 5]), 5)

def test_tief_verschachtelter_baum(self):
    self.assertEqual(zaehle_blaetter([1, [2, [3, [4, [5]]]]]), 5)

Beispiel Aufgabe: Schreibe eine Funktion warmkalt(temp), die eine Zahl als Parameter erhält und einen String zurückgibt. Wenn die Temperatur unter 18 Grad liegt, soll „Es ist sehr kalt!“ zurückgegeben werden. Wenn die Temperatur über 25 Grad liegt, soll „Es ist sehr warm!“ zurückgegeben werden. Ansonsten soll „Es ist angenehm!“ Zurückgegeben werden.
Beispiel Musterlösung:
def warmkalt(temp):
    if temp < 18:
        return "Es ist sehr kalt!"
    elif temp > 25:
        return "Es ist sehr warm!"
    else:
        return "Es ist angenehm!"

Beispiel Unit-Test:
import unittest

from main import warmkalt

class TestWarmKalt(unittest.TestCase):
    def test_sehr_kalt(self):
        self.assertEqual(warmkalt(10), "Es ist sehr kalt!")

    def test_angenehm(self):
        self.assertEqual(warmkalt(20), "Es ist angenehm!")

    def test_sehr_warm(self):
        self.assertEqual(warmkalt(30), "Es ist sehr warm!")

if __name__ == '__main__':
    unittest.main()
~~~
# Human Message
~~~
Entwickle einen Unit-Test für eine Programmieraufgabe inklusive aller benötigten Imports zu der nachfolgenden Musterlösung. Generiere nur den Unit-Test ohne zusätzlichen Text. Der Unit-Test soll direkt ausführbar sein.
~~~
# AI Message
~~~
# Task Description
{task_description}
# Code Skeleton
{code_skeleton}
# Model Solution
{model_solution}
~~~
# LLM & Parameters
- Model: gpt-4o-2024-05-13 (OpenAI)
- Temperature: 0.0
- other parameters remain default