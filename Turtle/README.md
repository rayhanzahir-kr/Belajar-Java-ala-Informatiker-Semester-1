# Turtle-Grafik – Erweiterte Version

## 1. Änderungen an `Turtle.java`

Ich habe die von der Veranstaltung bereitgestellte `Turtle.java` um folgende Funktionen erweitert:

1. **Farbunterstützung für Linien**
   - Neues Feld `strokeColor` in der Klasse `Turtle`.
   - Neue Methode  
     ```java
     Turtle color(String cssColor)
     ```  
     mit der die Linienfarbe über einen CSS-/SVG-Farbnamen (z.B. `"red"`) oder einen Hex-Code (z.B. `"#ff0000"`) gesetzt werden kann.
   - Die SVG-Ausgabe (`<path ...>`) wurde so angepasst, dass sie jetzt die Attribute  
     `stroke="<Farbe>"` und `stroke-width="<Breite>"` verwendet.

2. **Methode `polygon(int n, double size)`**
   - Zeichnet ein regelmäßiges n-Eck mit `n` Seiten und einer Seitenlänge von `size`.
   - Implementiert über eine Schleife mit `forward(size)` und `left(360.0 / n)`.


## 2. Nutzung der neuen Features in `first.java`

In `first.java` verwende ich die neuen Methoden wie folgt:

- Mit `color(...)` setze ich die Linienfarbe (z.B. orange, blau, grün), um die Grafik visuell ansprechender zu machen.
- Mit `polygon(int n, double size)` erzeuge ich eine Art „Blume“ aus regelmäßigen Vielecken (z.B. Hexagone), indem ich das Polygon mehrfach zeichne und die Turtle jedes Mal drehe.

## 3. Abgegebene Dateien

- `Turtle.java` – erweiterte Turtle-Klasse mit Farbunterstützung `color(String color)`, `polygon(...)` 
- `first.java` – Hauptprogramm, das die Turtle-Grafik erzeugt und die neuen Features nutzt.
- `output.svg` – Resultierende Turtle-Grafik im SVG-Format.
- `README.md` – Diese Dokumentation der Änderungen und der verwendeten Features.

