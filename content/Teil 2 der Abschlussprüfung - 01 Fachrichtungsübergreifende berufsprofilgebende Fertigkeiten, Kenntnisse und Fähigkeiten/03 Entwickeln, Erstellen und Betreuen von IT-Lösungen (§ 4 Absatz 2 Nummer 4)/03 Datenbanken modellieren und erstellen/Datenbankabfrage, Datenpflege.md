# Datenbankabfrage, Datenpflege

## Grundlagen

## SELECT-Befehl

Der **SELECT**-Befehl wird verwendet, um Daten aus einer oder mehreren Tabellen zu lesen.

### Syntax

```sql
SELECT spaltenname1, spaltenname2, ...
FROM tabellenname;
```

- **SELECT** gibt an, welche Spalten angezeigt werden sollen.
- **FROM** spezifiziert, aus welcher Tabelle die Daten abgefragt werden.

### Beispiel

```sql
SELECT name, alter FROM personen;
```

## WHERE-Klausel

Die **WHERE**-Klausel wird verwendet, um die Datensätze zu filtern und nur die Datensätze zurückzugeben, die eine bestimmte Bedingung erfüllen.

### Syntax

```sql
SELECT spaltenname1, spaltenname2, ...
FROM tabellenname
WHERE bedingung;
```

### Beispiel

```sql
SELECT name, alter FROM personen WHERE alter > 18;
```

## JOIN

**JOIN** wird verwendet, um Zeilen aus zwei oder mehr Tabellen basierend auf einer verwandten Spalte zwischen ihnen zu kombinieren.

### Arten von JOINs

- **INNER JOIN**: Gibt Datensätze zurück, die in beiden Tabellen eine Übereinstimmung haben.
- **LEFT JOIN** (oder **LEFT OUTER JOIN**): Gibt alle Datensätze aus der linken Tabelle und die übereinstimmenden Datensätze aus der rechten Tabelle zurück.
- **RIGHT JOIN** (oder **RIGHT OUTER JOIN**): Gibt alle Datensätze aus der rechten Tabelle und die übereinstimmenden Datensätze aus der linken Tabelle zurück.
- **FULL JOIN** (oder **FULL OUTER JOIN**): Gibt alle Datensätze zurück, wenn es eine Übereinstimmung in einer der Tabellen gibt.

### Beispiel

```sql
SELECT personen.name, bestellungen.produkt
FROM personen
INNER JOIN bestellungen ON personen.id = bestellungen.person_id;
```

## GROUP BY

**GROUP BY** wird verwendet, um ähnliche Datensätze in Gruppen zusammenzufassen.

### Syntax

```sql
SELECT spalte1, AGGREGATFUNKTION(spalte2)
FROM tabelle
WHERE bedingung
GROUP BY spalte1;
```

### Beispiel

```sql
SELECT alter, COUNT(name)
FROM personen
GROUP BY alter;
```

## HAVING

**HAVING** wird verwendet, um Bedingungen an die Gruppierungsergebnisse anzuhängen, ähnlich wie WHERE, aber für Gruppen.

### Syntax

```sql
SELECT spalte1, AGGREGATFUNKTION(spalte2)
FROM tabelle
WHERE bedingung
GROUP BY spalte1
HAVING bedingung_fuer_gruppe;
```

### Beispiel

```sql
SELECT alter, COUNT(name)
FROM personen
GROUP BY alter
HAVING COUNT(name) > 2;
```

## ORDER BY

**ORDER BY** wird verwendet, um die Ergebnisse einer Abfrage in aufsteigender oder absteigender Reihenfolge zu sortieren.

### Syntax

```sql
SELECT spaltenname1, spaltenname2, ...
FROM tabellenname
ORDER BY spaltenname1 [ASC|DESC];
```

### Beispiel

```sql
SELECT name, alter FROM personen
ORDER BY alter DESC;
```
