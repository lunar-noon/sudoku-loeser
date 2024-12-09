# Sudoku Löser

Das Ziel dieses Projekts ist die Entwicklung eines Programms, das Sudokus lösen kann. <br />

Das Programm greift dabei direkt auf die Webseite zu, extrahiert die Sudoku-Daten und überträgt diese automatisch in eine eigene Matrix, ohne dass der Benutzer manuelle Eingaben vornehmen muss. 
Die Daten des Sudokus werden durch die Java-Bibliothek **JSoup** aus dem HTML-Inhalt der Webseite extrahiert und automatisch in das entsprechende Format übertragen. Es wird dabei nur die Eingabe-Darstellung des Sudokus automatisch ausgefüllt – eine Lösung oder eine Berechnung des Rätsels findet nicht statt. <br />
Die Darstellung kann visuell erfolgen oder über andere Methoden erfolgen, je nachdem, wie das ausgefüllte Sudoku dargestellt oder überprüft werden soll. Das Ziel ist es, die extrahierten Informationen aus der Webseite zu übernehmen und sie automatisch in das Sudoku-Format einzufügen. 
Durch diesen Ansatz entfällt eine manuelle Eingabe oder Konfiguration durch den Benutzer. Stattdessen wird das Sudoku-Datenset direkt übernommen und aus dem Webseiten-Inhalt übertragen, wodurch der Prozess automatisiert und benutzerfreundlich gestaltet wird. <br />

Das Hauptziel und die Besonderheit des Programms liegen somit darin, die Sudokus automatisch von einer Webseite wie z.B. **usdoku.com** abzurufen, analysieren und lösen zu können. <br />

Eine grafische Benutzeroberfläche wird nicht benötigt; die Ergebnisse werden direkt in der Konsole ausgegeben. 


### Funktionsweise:
1. **Webdaten-Abruf:**
     - Das Programm greift automatisch auf die Webseite zu, lädt die HTML-Daten und extrahiert die Sudoku-Daten aus den relevanten Elementen.
     - Die extrahierten Zahlen werden in eine 9x9-Matrix umgewandelt, wobei leere Felder durch `0` repräsentiert werden.
2. **Algorithmus:**
     - Mithilfe eines Backtracking-Algorithmus wird das Sudoku gelöst. Dabei wird geprüft, ob Zahlen in Zeilen, Spalten und Blöcken korrekt sind, bevor sie eingesetzt werden.
     - Falls das Sudoku keine Lösung besitzt, gibt das Programm eine entsprechende Fehlermeldung aus.
3. **Ergebnisdarstellung:**
     - Nach der Berechnung wird die Lösung des Sudokus in einem lesbaren Format direkt in der Konsole angezeigt.

### Erweiterungsmöglichkeiten:
- **Streams**: Java-Streams können zur Verarbeitung der Matrix verwendet werden, z. B. zur Validierung der Zeilen und Spalten.
- **Parallelisierung**: Die Lösungsschritte könnten parallelisiert werden, um die Effizienz zu steigern.

### Verwendung von Java Streams
- **Komponenten mit Java Streams:**
    - **Validierung der Eingabe:** Streams zur Überprüfung, ob jede Zeile, Spalte und jeder Block die Sudoku-Regeln erfüllt.
    - **Ausgabe:** Streams zur formatgerechten Darstellung der gelösten Matrix.
    - **Optimierungen:** Streams zur parallelen Prüfung von Teilbereichen.

### Parallelisierung des Codes
- **Mögliche Parallelisierung:**
    - **Parallelisierung der Validierung:** Die Gültigkeitsprüfungen von Zeilen, Spalten und Blöcken können parallel laufen.
    - **Parallelisiertes Backtracking:** Verschiedene Startpunkte könnten parallel getestet werden, um die Lösung schneller zu finden.

### Start der Entwicklung
<ul>
<b>Phase 1:</b> Implementierung des Backtracking-Algorithmus. <br />
<b>Phase 2:</b> Hinzufügen der Validierungskomponente. <br />
<b>Phase 3:</b> Integration von Java Streams. <br />
<b>Phase 4:</b> Aufbau der GUI mit JavaFX. <br />
<b>Phase 5:</b> Testing und Optimierung. <br />
</ul>

