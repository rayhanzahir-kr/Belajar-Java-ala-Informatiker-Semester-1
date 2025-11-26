# Turtle-Grafik – Erweiterte Version

## 1. Änderungen an `Turtle.java`

Ich habe die von der Veranstaltung bereitgestellte `Turtle.java` um zwei zusätzliche Funktionen erweitert:

### 1. **Farbunterstützung für Linien**
- Neues Feld `strokeColor` in der Klasse `Turtle`.
- Neue Methode:
  ```java
  Turtle color(String cssColor)
  ```
  Mit dieser Methode kann die Linienfarbe über einen CSS-/SVG-Farbnamen (z.B. "red") oder einen Hex-Code (z.B. "#ff0000") gesetzt werden.
- Die SVG-Ausgabe für Linien wurde so angepasst, dass sie jetzt die Attribute  
  `stroke="<Farbe>"` und `stroke-width="<Breite>"` verwendet.

### 2. **Methode `polygon(int n, double size)`**
- Zeichnet ein regelmäßiges n-Eck mit `n` Seiten und einer Seitenlänge von `size`.
- Die Implementierung erfolgt über eine Schleife:
  - `forward(size)` zeichnet eine Seite
  - `left(360.0 / n)` dreht die Turtle um den passenden Außenwinkel

## 2. Nutzung der neuen Features in `first.java`

In `first.java` nutze ich die erweiterten Funktionen, um eine **Mandala Polygon Flower** zu zeichnen:

### Verwendete Methoden:
- `color(...)` für Farbverlauf
- `polygon(...)` für regelmäßige Polygone
- `left(...)` zur Drehung

Beispiel:

```java
for (int i = 0; i < 36; i++) {
    t.color("hsl(" + (i * 10) + ", 80%, 50%)");
    t.polygon(6, 20);
    t.left(10);
}
```

## 3. Abgegebene Dateien

- `Turtle.java`
- `first.java`
- `output.svg`
- `README.md`
