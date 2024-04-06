# ER-Diagramm, Attribute, Beziehungen, Kardinalitäten, relerenzielle Integrität, Aktualisierungsweitergabe. Löschweitergabe, Primärschlüssel, Fremdschlüssel

### ER-Diagramme und Datenbankdesign

#### 1. Einführung in ER-Diagramme

- **Definition**: Ein Entity-Relationship-Diagramm (ER-Diagramm) bildet die strukturellen Beziehungen zwischen den Daten in einer Datenbank ab. Es hilft beim Design und der Visualisierung von Datenbankstrukturen.
- **Bestandteile**: Entitäten (Datenobjekte), Beziehungen (Verbindungen zwischen Entitäten), Attribute (Eigenschaften von Entitäten).

#### 2. Entitäten und Attribute

- **Entitäten**: Repräsentieren Objekte oder Konzepte mit Datenwert, z.B. "Student" oder "Kurs".
- **Attribute**: Charakteristika oder Eigenschaften einer Entität, z.B. Name, Alter eines Studenten. Primärschlüssel (einzigartiges Identifikationsmerkmal) sind hervorgehoben.

#### 3. Beziehungen und Kardinalitäten

- **Beziehungstypen**:
  - **Eins-zu-eins (1:1)**: Jede Entität A ist mit höchstens einer Entität B verbunden und umgekehrt.
  - **Eins-zu-viele (1:n)**: Eine Entität aus A kann mit mehreren Entitäten aus B verbunden sein, aber eine Entität aus B ist nur mit einer Entität aus A verbunden.
  - **Viele-zu-viele (n:m)**: Entitäten aus A können mit mehreren Entitäten aus B verbunden sein und umgekehrt.

#### 4. Referenzielle Integrität und Schlüsselkonzepte

- **Referenzielle Integrität**: Sicherstellung, dass jede Fremdschlüsselbeziehung in der Datenbank eine entsprechende Primärschlüsseleintragung hat.
- **Primärschlüssel**: Einzigartiges Attribut, das jede Entität in einer Entitätsmenge identifiziert.
- **Fremdschlüssel**: Attribut, das in einer anderen Entität als Primärschlüssel dient, um Beziehungen zu verknüpfen.

#### 5. Aktualisierungs- und Löschweitergabe

- **Aktualisierungsweitergabe**: Regeln, die definieren, was bei der Aktualisierung von Primärschlüsseln passiert.
- **Löschweitergabe**: Regeln, die bestimmen, wie mit den verknüpften Daten umgegangen wird, wenn eine Entität gelöscht wird.

<image src="https://www.herrmix.de/dokuwiki/lib/exe/fetch.php?media=datenbanken:relational:er-beispiel2.png" alt="ER-Diagramm">

Bildquelle - 06.04.24:
https://www.herrmix.de/dokuwiki/lib/exe/fetch.php?media=datenbanken:relational:er-beispiel2.png

Erklärvideo:
[Youtube](https://www.youtube.com/watch?v=fVbYB_34v-E)
