# Abfrage über mehrere Tabellen (JOIN)

## Einleitung

**JOINs** in SQL werden verwendet, um Zeilen aus zwei oder mehr Tabellen zu kombinieren, basierend auf einer verwandten Spalte zwischen ihnen. Das Verständnis von JOINs ist entscheidend, um komplexe Abfragen zu erstellen und relationale Datenbanken effektiv zu nutzen.

## Grundtypen von JOINs

### INNER JOIN

- **Beschreibung**: Gibt Datensätze zurück, die in beiden Tabellen eine Übereinstimmung haben.
- **Syntax**:
  ```sql
  SELECT spalten
  FROM tabelle1
  INNER JOIN tabelle2 ON tabelle1.gemeinsame_spalte = tabelle2.gemeinsame_spalte;
  ```
- **Beispiel**:
  ```sql
  SELECT Mitarbeiter.Name, Abteilung.Bezeichnung
  FROM Mitarbeiter
  INNER JOIN Abteilung ON Mitarbeiter.AbteilungsID = Abteilung.ID;
  ```

### LEFT JOIN (oder LEFT OUTER JOIN)

- **Beschreibung**: Gibt alle Datensätze aus der linken Tabelle und die übereinstimmenden Datensätze aus der rechten Tabelle zurück.
- **Syntax**:
  ```sql
  SELECT spalten
  FROM tabelle1
  LEFT JOIN tabelle2 ON tabelle1.gemeinsame_spalte = tabelle2.gemeinsame_spalte;
  ```
- **Beispiel**:
  ```sql
  SELECT Mitarbeiter.Name, Abteilung.Bezeichnung
  FROM Mitarbeiter
  LEFT JOIN Abteilung ON Mitarbeiter.AbteilungsID = Abteilung.ID;
  ```

### RIGHT JOIN (oder RIGHT OUTER JOIN)

- **Beschreibung**: Gibt alle Datensätze aus der rechten Tabelle und die übereinstimmenden Datensätze aus der linken Tabelle zurück.
- **Syntax**:
  ```sql
  SELECT spalten
  FROM tabelle1
  RIGHT JOIN tabelle2 ON tabelle1.gemeinsame_spalte = tabelle2.gemeinsame_spalte;
  ```
- **Beispiel**:
  ```sql
  SELECT Mitarbeiter.Name, Abteilung.Bezeichnung
  FROM Mitarbeiter
  RIGHT JOIN Abteilung ON Mitarbeiter.AbteilungsID = Abteilung.ID;
  ```

### FULL JOIN (oder FULL OUTER JOIN)

- **Beschreibung**: Gibt alle Datensätze zurück, wenn es eine Übereinstimmung in einer der Tabellen gibt.
- **Syntax**:
  ```sql
  SELECT spalten
  FROM tabelle1
  FULL JOIN tabelle2 ON tabelle1.gemeinsame_spalte = tabelle2.gemeinsame_spalte;
  ```
- **Beispiel**:
  ```sql
  SELECT Mitarbeiter.Name, Abteilung.Bezeichnung
  FROM Mitarbeiter
  FULL JOIN Abteilung ON Mitarbeiter.AbteilungsID = Abteilung.ID;
  ```

## Spezialfälle von JOINs

### Selbst-JOIN

- **Beschreibung**: Ein Selbst-JOIN wird verwendet, um eine Tabelle mit sich selbst zu verbinden, als ob sie zwei separate Tabellen wären.
- **Anwendungsfall**: Geeignet, um relationale Daten innerhalb derselben Tabelle zu vergleichen oder zu verknüpfen.

### Kreuz-JOIN (CROSS JOIN)

- **Beschreibung**: Erzeugt ein kartesisches Produkt der beiden Tabellen, d.h., jede Zeile der ersten Tabelle wird mit jeder Zeile der zweiten Tabelle kombiniert.
- **Anwendungsfall**: Nützlich in speziellen Situationen, wo jede Kombination von Datensätzen benötigt wird.

## Best Practices

- **Indexierung**: Stelle sicher, dass die Spalten, die für JOINs verwendet werden, indexiert sind, um die Abfrageleistung zu verbessern.
- **Vermeide unnötige Spalten**: Wähle nur die Spalten aus, die du tatsächlich benötigst, um die Effizienz der Abfrage zu erhöhen.
- **Klare Aliase**: Verwende Aliase für Tabellennamen, um deine SQL-Statements klarer und leichter lesbar zu machen.

## Fazit

JOINs sind ein mächtiges Werkzeug in SQL, um komplexe Datenabfragen über mehrere Tabellen hinweg zu ermöglichen. Durch das Verständnis der verschiedenen Arten von JOINs und deren Anwendung kannst du umfangreiche Datenrelation
