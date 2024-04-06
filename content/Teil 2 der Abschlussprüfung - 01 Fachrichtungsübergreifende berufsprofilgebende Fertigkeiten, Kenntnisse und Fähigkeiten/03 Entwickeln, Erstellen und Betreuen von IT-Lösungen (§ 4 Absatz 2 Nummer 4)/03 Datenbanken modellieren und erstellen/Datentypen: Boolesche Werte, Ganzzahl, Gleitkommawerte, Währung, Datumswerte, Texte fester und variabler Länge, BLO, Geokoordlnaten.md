# Datentypen: Boolesche Werte, Ganzzahl, Gleitkommawerte, Währung, Datumswerte, Texte fester und variabler Länge, BLO, Geokoordlnaten

## Erklärung zu SQL Datentypen

SQL-Datentypen definieren die Art von Daten, die in einer Spalte eines Tabellen oder in Ausdrücken und Variablen gespeichert werden können. Die Auswahl des richtigen Datentyps für eine Spalte ist entscheidend, da sie die Integrität der Daten sicherstellt und die Performance der Datenbank beeinflussen kann. Hier eine kurze Erläuterung der Schlüsselaspekte:

## Ganzzahltypen (`TINYINT`, `SMALLINT`, `MEDIUMINT`, `INT`, `BIGINT`)

- **Verwendung**: Ideal für numerische Daten, die nur ganze Zahlen sind (positiv oder negativ).
- **Speicher**: Der Speicherplatz variiert je nach Typ von 1 Byte bis 8 Bytes, was beeinflusst, wie große Zahlen gespeichert werden können.
- **UNSIGNED**: Eine Option, die negative Zahlen ausschließt, wodurch der positive Wertebereich verdoppelt wird.

## Fließkommazahlen und Dezimaltypen (`FLOAT`, `DOUBLE`, `DECIMAL`)

- **Verwendung**: Geeignet für numerische Daten mit Dezimalstellen. `FLOAT` und `DOUBLE` sind für Approximationen, während `DECIMAL` für exakte Werte verwendet wird (z.B. Währung).
- **Speicher und Genauigkeit**: `FLOAT` und `DOUBLE` verwenden weniger Speicher, können aber zu Präzisionsverlust führen. `DECIMAL` verwendet mehr Speicher, bietet jedoch volle Präzision.

## Datums- und Zeitdatentypen (`DATE`, `TIME`, `DATETIME`, `TIMESTAMP`)

- **Verwendung**: Zur Speicherung von Datums- und Zeitwerten. Der Unterschied liegt im Format und im unterstützten Zeitbereich.
- **Spezialfall `TIMESTAMP`**: Wird oft für Aufzeichnungen der letzten Änderung verwendet, da er sich automatisch mit der aktuellen Zeit aktualisiert.

## Zeichenketten (`CHAR`, `VARCHAR`, `TEXT`, `BLOB`)

- **`CHAR` vs. `VARCHAR`**: `CHAR` wird für Zeichenketten fester Länge verwendet und füllt kürzere Strings mit Leerzeichen auf. `VARCHAR` ist flexibler und speichert Zeichenketten variabler Länge effizienter.
- **`TEXT` und `BLOB`**: Für große Text- oder Binärdaten. Die Unterscheidung liegt hauptsächlich in der Behandlung durch die Datenbank (Text wird auf Zeichensatz und Sortierung angewendet, BLOB nicht).

## Spezialtypen (`ENUM`, `SET`)

- **`ENUM`**: Erlaubt die Definition einer Liste von vordefinierten Werten. Jeder Eintrag in einer `ENUM`-Spalte muss einer dieser Werte sein.
- **`SET`**: Ähnlich wie `ENUM`, aber erlaubt die Speicherung von mehreren Werten aus der definierten Liste in einer Spalte.

Die Wahl des Datentyps hat direkte Auswirkungen auf die Datenintegrität, Speicheranforderungen und Leistung der Datenbankabfragen. Es ist wichtig, den Datentyp basierend auf den erwarteten Daten und der Anwendung, die diese Daten verwendet, sorgfältig auszuwählen.

## SQL Datentypen Tabelle

| Datentyp    | Optionen              | Speicherplatz  | Beschreibung                                                                                                                                       |
| ----------- | --------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `TINYINT`   | `[(M)] [U] [Z]`       | 1 Byte         | Ganzzahlen von 0 bis 255 oder von -128 bis +127                                                                                                    |
| `SMALLINT`  | `[(M)] [U] [Z]`       | 2 Bytes        | Ganzzahlen von 0 bis 65.535 oder von -32.768 bis +32.767                                                                                           |
| `MEDIUMINT` | `[(M)] [U] [Z]`       | 3 Bytes        | Ganzzahlen von 0 bis 16.777.215 oder von -8.388.608 bis +8.388.607                                                                                 |
| `INT`       | `[(M)] [U] [Z]`       | 4 Bytes        | Ganzzahlen von 0 bis ~4,3 Milliarden oder von -2.147.483.648 bis +2.147.483.647                                                                    |
| `INTEGER`   | `[(M)] [U] [Z]`       | 4 Bytes        | Alias für INT                                                                                                                                      |
| `BIGINT`    | `[(M)] [U] [Z]`       | 8 Bytes        | Ganzzahlen von 0 bis 2^64-1 oder von -(2^63) bis (2^63)-1                                                                                          |
| `FLOAT`     | `[(M,D)] [U] [Z]`     | 4 Bytes        | Fließkommazahl, vorzeichenbehaftet. Wertebereich von -3,402823466^38 bis -1,175494351^38, 0 und 1,175494351^38 bis 3,402823466^38                  |
| `DOUBLE`    | `[(M,D)] [U] [Z]`     | 8 Bytes        | Fließkommazahl, vorzeichenbehaftet. Wertebereich von ~ -1,798^308 bis ~ -2,225^-308, 0 und ~ 2,225^-308 bis ~ 1,798^308                            |
| `REAL`      | `[(M,D)] [U] [Z]`     | 8 Bytes        | Alias für DOUBLE                                                                                                                                   |
| `DECIMAL`   | `[(M,D)] [U] [Z]`     | M + x Bytes    | Fließkommazahl, vorzeichenbehaftet. Speicherbedarf: x=1 wenn D=0, sonst x=2                                                                        |
| `NUMERIC`   | `[(M,D)] [U] [Z]`     | M + x Bytes    | Alias für DECIMAL. Speicherbedarf: x=1 wenn D=0, sonst x=2                                                                                         |
| `DATE`      | -                     | 3 Bytes        | Datum im Format 'YYYY-MM-DD'. Wertebereich von 01.01.1000 bis 31.12.9999                                                                           |
| `DATETIME`  | -                     | 8 Bytes        | Datumsangabe im Format 'YYYY-MM-DD hh:mm:ss'. Wertebereich entspricht DATE                                                                         |
| `TIMESTAMP` | `[(M)]`               | 4 Bytes        | Zeitstempel. Wertebereich: 1.1.1970 bis 2037. Anzahl Stellen (M): 6, 8, 12, 14                                                                     |
| `TIME`      | -                     | 3 Bytes        | Zeit zwischen -838:59:59 und +839:59:59. Ausgabe: 'hh:mm:ss'                                                                                       |
| `YEAR`      | `[(2\|4)]`            | 1 Byte         | Jahr zwischen 1901 bis 2155 bei (4) und zwischen 1970 bis 2069 bei (2)                                                                             |
| `CHAR`      | `(M) [BINARY]`        | M Byte(s)      | Zeichenkette fester Länge M. Wertebereich für M: 0 bis 255                                                                                         |
| `VARCHAR`   | `(M) [BINARY]`        | L+1 Bytes      | Zeichenkette variabler Länge, Maximum ist M. Wertebereich für M: 0 bis 255                                                                         |
| `BLOB`      | -                     | L+2 Bytes      | Binäres Objekt mit variablen Daten. Weitere Typen: TINYBLOB, MEDIUMBLOB und LONGBLOB                                                               |
| `TEXT`      | -                     | L+2 Bytes      | Identisch mit BLOB. Berücksichtigt beim Sortieren & Vergleichen die Groß- und Kleinschreibung nicht. Weitere Typen: TINYTEXT, MEDIUMTEXT, LONGTEXT |
| `ENUM`      | `('val1','val2' ...)` | 1 oder 2 Bytes | Liste von Werten (val1, val2 ...). Maximal 65.535 eineindeutige Elemente sind möglich                                                              |
| `SET`       | `('val1','val2' ...)` | x Bytes        | String-Objekt mit verschiedenen Variablen. Maximal 64 'Mitglieder' sind möglich. Speicherbedarf: x ist 1, 2, 3, 4 oder 8                           |

## Legende

- `^` = Potenzzeichen
- `[ ]` = optionaler Parameter
- `BINARY` = Attribut für die Sortierung
- `D` = Anzahl der Kommastellen bei einer Dezimalzahl
- `L` = Stringlänge (Berechnung Speicherbedarf)
- `M` = maximale Anzahl der gezeigten Stellen
- `Mill.` = Milliarden
- `U` = UNSIGNED (Zahl ohne Vorzeichen)
- `Z` = Zerofill

Quelle:
[Quelle](https://elearn.inf.tu-dresden.de/sqlkurs/lektionXY/03_mySQL%20datentypen.html#leg)

Erklärvideo:
[Youtube](https://www.youtube.com/watch?v=caMVrHP-SIs)
