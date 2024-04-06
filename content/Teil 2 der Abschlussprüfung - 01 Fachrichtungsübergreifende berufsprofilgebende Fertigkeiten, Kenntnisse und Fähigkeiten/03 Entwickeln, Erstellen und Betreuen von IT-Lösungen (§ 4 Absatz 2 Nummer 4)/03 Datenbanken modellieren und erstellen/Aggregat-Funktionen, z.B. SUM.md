# Aggregat-Funktionen, z.B. SUM

Aggregatfunktionen in SQL sind mächtige Werkzeuge, die es ermöglichen, statistische Informationen aus Datensätzen zu berechnen. Sie werden typischerweise in Kombination mit der `GROUP BY`-Klausel verwendet, können aber auch ohne sie angewendet werden.

## SUM

- **Beschreibung**: Addiert die Werte einer Spalte.
- **Syntax**:
  ```sql
  SELECT SUM(spaltenname) FROM tabelle;
  ```
- **Beispiel**:
  ```sql
  SELECT SUM(gehalt) FROM mitarbeiter;
  ```
  Berechnet die Gesamtsumme der Gehälter aller Mitarbeiter.

## AVG

- **Beschreibung**: Berechnet den Durchschnittswert einer Spalte.
- **Syntax**:
  ```sql
  SELECT AVG(spaltenname) FROM tabelle;
  ```
- **Beispiel**:
  ```sql
  SELECT AVG(gehalt) FROM mitarbeiter;
  ```
  Ermittelt das durchschnittliche Gehalt der Mitarbeiter.

## COUNT

- **Beschreibung**: Zählt die Anzahl der Zeilen.
- **Syntax**:
  ```sql
  SELECT COUNT(spaltenname) FROM tabelle;
  ```
- **Beispiel**:
  ```sql
  SELECT COUNT(*) FROM mitarbeiter;
  ```
  Zählt die Anzahl aller Mitarbeiter in der Tabelle.

## MAX

- **Beschreibung**: Findet den höchsten Wert in einer Spalte.
- **Syntax**:
  ```sql
  SELECT MAX(spaltenname) FROM tabelle;
  ```
- **Beispiel**:
  ```sql
  SELECT MAX(gehalt) FROM mitarbeiter;
  ```
  Ermittelt das höchste Gehalt unter den Mitarbeitern.

## MIN

- **Beschreibung**: Findet den niedrigsten Wert in einer Spalte.
- **Syntax**:
  ```sql
  SELECT MIN(spaltenname) FROM tabelle;
  ```
- **Beispiel**:
  ```sql
  SELECT MIN(gehalt) FROM mitarbeiter;
  ```
  Ermittelt das niedrigste Gehalt unter den Mitarbeitern.

## GROUP BY

- **Beschreibung**: Wird verwendet, um Ergebnissets in Gruppen aufzuteilen, über die dann Aggregatfunktionen angewendet werden können.
- **Syntax**:
  ```sql
  SELECT spalte1, AGGREGATFUNKTION(spalte2)
  FROM tabelle
  GROUP BY spalte1;
  ```
- **Beispiel**:
  ```sql
  SELECT abteilung, SUM(gehalt)
  FROM mitarbeiter
  GROUP BY abteilung;
  ```
  Zeigt die Gesamtsumme der Gehälter je Abteilung.

## HAVING

- **Beschreibung**: Ermöglicht das Filtern von Gruppen basierend auf einem Kriterium, ähnlich der `WHERE`-Klausel, die jedoch auf einzelne Datensätze angewendet wird.
- **Syntax**:
  ```sql
  SELECT spalte1, AGGREGATFUNKTION(spalte2)
  FROM tabelle
  GROUP BY spalte1
  HAVING AGGREGATFUNKTION(spalte2) > Wert;
  ```
- **Beispiel**:
  ```sql
  SELECT abteilung, AVG(gehalt)
  FROM mitarbeiter
  GROUP BY abteilung
  HAVING AVG(gehalt) > 5000;
  ```
  Listet Abteilungen mit einem durchschnittlichen Gehalt von mehr als 5000.

## Wichtige Hinweise

- Aggregatfunktionen ignorieren `NULL`-Werte in der Berechnung, außer `COUNT(*)`.
- `COUNT(spaltenname)` zählt Einträge in der spezifizierten Spalte, die nicht `NULL` sind.
- Aggregatfunktionen können nicht nur auf numerische Daten angewendet werden. Zum Beispiel kann `MAX` oder `MIN` auch auf Datums- oder Textdaten angewendet werden, um den neuesten Zeitpunkt oder den alphabetisch ersten/letzten Wert zu finden.

## Fazit

Aggregatfunktionen sind unverzichtbare Werkzeuge in SQL für die Datenanalyse. Durch ihre Anwendung

können wichtige Einsichten in Datenmengen gewonnen werden, was für Berichterstattungen, Datenzusammenfassungen und Entscheidungsfindungen von entscheidender Bedeutung ist.
