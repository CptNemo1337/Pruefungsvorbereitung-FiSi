---
title: "Tabellenstruktur, Indexierung, Manipulation, Projektion, Selektion, Sortieren und Gruppieren"
date: 2024-04-07
draft: false
type: docs
description: "Tabellenstruktur Indexierung Manipulation Projektion Selektion Sortieren und Gruppieren"
---

# SQL-Befehlskategorien + Struktur und Indexierung

Hier könnte Ihr Text stehen

Tabellenstruktur, Index, Manipulation, Projektion, Selektion, , Sortieren, Gruppieren

Hier ist dein Lernzettel zu SQL, strukturiert in Markdown, der einen Überblick über SQL-Befehle und ihre Einteilung in verschiedene Kategorien bietet:

---

# Kurzer Überblick über SQL

SQL (Structured Query Language) ist eine standardisierte Programmiersprache, die für die Verwaltung und Manipulation relationaler Datenbanken verwendet wird. SQL ermöglicht es, Datenbanken zu erstellen, Daten zu manipulieren, abzufragen und die Zugriffskontrolle zu verwalten. Die Sprache umfasst verschiedene Arten von Befehlen, darunter:

- **DDL (Data Definition Language)**: Zum Definieren der Struktur von Datenbankobjekten.
- **DQL (Data Query Language)**: Zum Abfragen von Daten.
- **DML (Data Manipulation Language)**: Zum Manipulieren von Daten.
- **DCL (Data Control Language)**: Zur Verwaltung von Zugriffsrechten und Berechtigungen.
- **TCL (Transaction Control Language)**: Zur Verwaltung von Datenbanktransaktionen.

### Tabellenstruktur und Index

- **CREATE TABLE**: Definiert eine neue Tabelle und ihre Struktur.
  ```sql
  CREATE TABLE mitarbeiter (
      id INT PRIMARY KEY,
      name VARCHAR(100),
      abteilung VARCHAR(50)
  );
  ```
- **Index**: Verbessert Abfragegeschwindigkeiten durch schnelleres Auffinden von Datensätzen.
  ```sql
  CREATE INDEX idx_name ON mitarbeiter (name);
  ```

## SQL-Befehle

### DDL (Datendefinitionssprache)

DDL-Befehle definieren das Schema einer Datenbank und werden zum Erstellen, Ändern und Löschen von Datenbankstrukturen verwendet.

- **CREATE**: Erstellt eine Datenbank oder ihre Objekte (z.B. Tabellen, Indizes).
  ```sql
  CREATE TABLE mitarbeiter (id INT, name VARCHAR(100));
  ```
- **DROP**: Löscht Objekte aus der Datenbank.
  ```sql
  DROP TABLE mitarbeiter;
  ```
- **ALTER**: Ändert die Struktur einer Datenbank.
  ```sql
  ALTER TABLE mitarbeiter ADD geburtsdatum DATE;
  ```
- **TRUNCATE**: Entfernt alle Datensätze aus einer Tabelle, ohne die Tabelle selbst zu löschen.
  ```sql
  TRUNCATE TABLE mitarbeiter;
  ```
- **COMMENT**: Fügt Kommentare zum Datenwörterbuch hinzu.
- **RENAME**: Benennt ein Objekt in der Datenbank um.
  ```sql
  RENAME TABLE mitarbeiter TO angestellte;
  ```

### DQL (Datenabfragesprache)

DQL besteht hauptsächlich aus dem SELECT-Befehl zum Abfragen von Daten.

- **SELECT**: Abrufen von Daten aus der Datenbank.
  ```sql
  SELECT * FROM mitarbeiter;
  ```

### DML (Datenmanipulationssprache)

DML-Befehle werden verwendet, um Daten innerhalb der Datenbank zu manipulieren.

- **INSERT**: Fügt Daten in Tabellen ein.
  ```sql
  INSERT INTO mitarbeiter (id, name) VALUES (1, 'Max Mustermann');
  ```
- **UPDATE**: Aktualisiert vorhandene Daten.
  ```sql
  UPDATE mitarbeiter SET name = 'John Doe' WHERE id = 1;
  ```
- **DELETE**: Entfernt Daten aus der Datenbank.
  ```sql
  DELETE FROM mitarbeiter WHERE id = 1;
  ```
- **LOCK**: Steuert die Parallelität der Tabellen.
- **CALL**: Ruft ein PL/SQL- oder JAVA-Unterprogramm auf.
- **EXPLAIN PLAN**: Beschreibt den Zugriffspfad zu den Daten.

### DCL (Datenkontrollsprache)

DCL befasst sich mit Berechtigungen und Zugriffsrechten.

- **GRANT**: Gewährt Zugriffsrechte an Benutzer.
  ```sql
  GRANT SELECT, UPDATE ON my_table TO some_user;
  ```
- **REVOKE**: Entzieht Zugriffsrechte von Benutzern.
  ```sql
  REVOKE SELECT, UPDATE ON my_table FROM user1;
  ```

### TCL (Transaktionskontrollsprache)

TCL-Befehle verwalten Transaktionen innerhalb der Datenbank.

- **BEGIN**: Startet eine Transaktion.
- **COMMIT**: Bestätigt eine Transaktion.
  ```sql
  COMMIT;
  ```
- **ROLLBACK**: Macht Änderungen einer Transaktion rückgängig.
  ```sql
  ROLLBACK;
  ```
- **SAVEPOINT**: Setzt einen Speicherpunkt innerhalb einer Transaktion.
  ```sql
  SAVEPOINT savepoint_name;
  ```
  Quelle:
  [Quelle](https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/)

Erklärvideo:
[Youtube](https://www.youtube.com)
