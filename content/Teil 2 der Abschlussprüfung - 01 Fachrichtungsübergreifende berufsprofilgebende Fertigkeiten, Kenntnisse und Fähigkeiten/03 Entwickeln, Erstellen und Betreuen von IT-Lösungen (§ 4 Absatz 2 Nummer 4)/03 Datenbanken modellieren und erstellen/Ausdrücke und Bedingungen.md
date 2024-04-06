# Ausdrücke und Bedingungen (Operatoren)

Ausdrücke und Bedingungen in SQL werden verwendet, um spezifische Datensätze zu filtern, Daten zu modifizieren oder Berechnungen durchzuführen. Sie sind entscheidend für die Erstellung effektiver und effizienter SQL-Abfragen.

## Grundlegende Vergleichsoperatoren

- **=** (gleich)
- **<>** oder **!=** (ungleich)
- **<** (kleiner als)
- **>** (größer als)
- **<=** (kleiner gleich)
- **>=** (größer gleich)

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE alter >= 30;
```

Wählt alle Mitarbeiter aus, die 30 Jahre oder älter sind.

## Logische Operatoren

Logische Operatoren werden verwendet, um mehrere Bedingungen in einer SQL-Abfrage zu kombinieren.

- **AND**: Gibt `TRUE` zurück, wenn beide Bedingungen wahr sind.
- **OR**: Gibt `TRUE` zurück, wenn mindestens eine der Bedingungen wahr ist.
- **NOT**: Kehrt das Ergebnis einer Bedingung um.

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE alter >= 30 AND geschlecht = 'M';
```

Wählt alle männlichen Mitarbeiter aus, die 30 Jahre oder älter sind.

## BETWEEN

Der `BETWEEN`-Operator wird verwendet, um Werte innerhalb eines bestimmten Bereichs auszuwählen. Er umfasst beide Endwerte.

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE gehalt BETWEEN 2000 AND 3000;
```

Wählt Mitarbeiter aus, deren Gehalt zwischen 2000 und 3000 liegt.

## IN

Der `IN`-Operator ermöglicht die Auswahl von Datensätzen, deren Wert einer in einer Liste angegebenen Wert entspricht.

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE abteilung_id IN (3, 5, 7);
```

Wählt Mitarbeiter aus, die in den Abteilungen mit den IDs 3, 5 oder 7 arbeiten.

## LIKE

Der `LIKE`-Operator wird für die Suche nach einem spezifizierten Muster in einer Spalte verwendet.

- `%` repräsentiert null, einen oder mehrere Zeichen.
- `_` repräsentiert genau ein Zeichen.

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE name LIKE 'Ma%';
```

Wählt Mitarbeiter aus, deren Name mit "Ma" beginnt.

## IS NULL

Mit `IS NULL` können Zeilen ausgewählt werden, in denen keine Daten in einer Spalte vorhanden sind.

### Beispiel

```sql
SELECT * FROM mitarbeiter WHERE adresse IS NULL;
```

Wählt Mitarbeiter aus, deren Adresse nicht angegeben ist.

## CASE

`CASE` wird verwendet, um bedingte Anweisungen in SQL-Abfragen zu ermöglichen, ähnlich wie if-else-Anweisungen in anderen Programmiersprachen.

### Beispiel

```sql
SELECT name,
       CASE
           WHEN gehalt <= 2000 THEN 'Niedrig'
           WHEN gehalt BETWEEN 2001 AND 5000 THEN 'Mittel'
           ELSE 'Hoch'
       END AS Gehaltsklasse
FROM mitarbeiter;
```

Ordnet Mitarbeiter basierend auf ihrem Gehalt in Kategorien ein (Niedrig, Mittel, Hoch).

## Fazit

Ausdrücke und Bedingungen in SQL sind mächtige Werkzeuge zur Datenmanipulation und -abfrage. Durch ihre effektive Nutzung können komplexe Datenabfragen erstellt, Daten gefiltert und spezifische Berechnungen durchgeführt werden.
