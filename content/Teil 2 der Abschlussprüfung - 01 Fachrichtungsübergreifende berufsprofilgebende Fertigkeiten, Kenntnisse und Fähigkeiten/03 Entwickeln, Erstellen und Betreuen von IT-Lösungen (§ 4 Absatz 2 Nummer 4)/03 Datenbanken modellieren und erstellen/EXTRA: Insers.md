# SQL INSERT INTO Anweisung

## Einleitung

Die SQL-Anweisung `INSERT INTO` wird verwendet, um neue Zeilen von Daten in eine Tabelle in der Datenbank hinzuzufügen. Fast alle relationalen Datenbankmanagementsysteme (RDBMS) bieten diese SQL-Abfrage an, um Datensätze in Datenbanktabellen hinzuzufügen.

Jeder Wert in den Datensätzen, die wir mit dieser Anweisung in eine Tabelle einfügen, sollte denselben Datentyp wie die jeweilige Spalte haben und die Beschränkungen der Spalte (falls vorhanden) erfüllen. Die mittels einer `INSERT`-Anweisung übergebenen Werte sollten der Anzahl der Spalten in der Tabelle entsprechen oder der Anzahl der in der aktuellen Abfrage erwähnten Spalten. Wenn eine dieser Bedingungen nicht erfüllt ist, erzeugt diese Anweisung einen Fehler.

## Syntax

Es gibt zwei grundlegende Syntaxformen der `INSERT INTO`-Anweisung, die nachfolgend dargestellt sind:

### Einfügen in spezifizierte Spalten

```sql
INSERT INTO TABELLENNAME (spalte1, spalte2...spalteN)
VALUES (wert1, wert2...wertN);
```

Hier sind `spalte1, spalte2, ...spalteN` die Namen der Spalten in der Tabelle, in die du Daten einfügen möchtest.

### Einfügen ohne Angabe der Spaltennamen

Es gibt auch eine Syntax für `INSERT INTO`, bei der nur die Werte ohne Spaltennamen angegeben werden. Dabei muss sichergestellt werden, dass die Reihenfolge der Werte der Reihenfolge der Spalten in der Tabelle entspricht.

```sql
INSERT INTO TABELLENNAME
VALUES (wert1, wert2...wertN);
```

## Beispiel

Um ein Beispiel zu sehen, erstellen wir eine Tabelle namens `KUNDEN` in der MySQL-Datenbank mit dem `CREATE TABLE`-Befehl wie folgt:

```sql
CREATE TABLE KUNDEN(
   ID   INT              NOT NULL,
   NAME VARCHAR (20)     NOT NULL,
   ALTER INT             NOT NULL,
   ADRESSE  CHAR (25),
   GEHALT   DECIMAL (18, 2),
   PRIMARY KEY (ID)
);
```

Die folgenden `INSERT INTO`-Anweisungen erstellen drei Datensätze in der leeren `KUNDEN`-Tabelle:

```sql
INSERT INTO KUNDEN (ID, NAME, ALTER, ADRESSE, GEHALT)
VALUES (1, 'Ramesh', 32, 'Ahmedabad', 2000.00);

INSERT INTO KUNDEN (ID, NAME, ALTER, ADRESSE, GEHALT)
VALUES (2, 'Khilan', 25, 'Delhi', 1500.00);

INSERT INTO KUNDEN (ID, NAME, ALTER, ADRESSE, GEHALT)
VALUES (3, 'Kaushik', 23, 'Kota', 2000.00);
```

Wir können auch mehrere Zeilen gleichzeitig einfügen:

```sql
INSERT INTO KUNDEN (ID, NAME, ALTER, ADRESSE, GEHALT) VALUES
(4, 'Chaitali', 25, 'Mumbai', 6500.00),
(5, 'Hardik', 27, 'Bhopal', 8500.00),
(6, 'Komal', 22, 'Hyderabad', 4500.00);
```

Um zu überprüfen, ob die Datensätze erfolgreich in die `KUNDEN`-Tabelle eingefügt wurden, verwenden wir die `SELECT`-Abfrage:

```sql
SELECT * FROM KUNDEN;
```

Die Tabelle wird angezeigt mit allen eingefügten Datensätzen.

Quelle:
[Quelle](https://www.tutorialspoint.com/sql/sql-insert-query.htm)
