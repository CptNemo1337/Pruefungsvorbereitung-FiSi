---
title: "Abbildung der Kontrollstrukturen mittels Struktogramm, PAP oder Pseudocode als didaktisches Hillsmittel"
date: 2024-04-07
draft: false
type: docs
description: "Abbildung der Kontrollstrukturen mittels Struktogramm PAP oder Pseudocode als didaktisches Hillsmittel"
---

# Programmablaufplan

## Programmablaufplan – Definition

Ein Programmablaufplan (Synonym: Programmstrukturdiagramm) ist eine Art Flussdiagramm, das den Ablauf eines Computerprogramms oder eines Algorithmus darstellt. Der Programmablaufplan (PAP) ist gemäß DIN 66001 genormt. Er ist eine grafische Vorlage für die Software-Implementierung oder dient der Systemdokumentation. Wesentliche Bestandteile eines Programmablaufplans bestehen aus Ein- und Ausgaben sowie zentralen Rechenoperationen des Computerprogramms. Der Programmablaufplan verwendet eine Reihe von Standardsymbolen. Neben einer Vorgabe für die Implementierung und einer Systemdokumentation besteht ein Anwendungszweck des Programmablaufplans in der Verbesserung der Effizienz von Computerprogrammen, Systemen bzw. Algorithmen.

Ein Programmablaufplan (kurz: PAP, englisch: program flow chart) ist eine spezifische Ausprägung eines Flussdiagramms. Flussdiagramme kommen in vielen Unternehmen als PAPs zum Einsatz, um standardisierte Abläufe zu veranschaulichen. Ein Ablaufdiagramm ohne Normierung (z.B. in Bezug auf die Art der Symbole) dient allgemein zur Darstellung von Prozessen, Algorithmen, Entscheidungen etc.

## Programmablaufplan – Elemente

Ein Programmablaufplan enthält sechs Grundelemente, womit das Diagramm modelliert werden kann. Die Beschreibung von den Elementen wird im Folgenden und die Darstellung der Symbole wird zum Ende des Kapitels vorgenommen.

1. **Grenzstelle**\
   Ein Grenzstelle kann der Anfang oder das Ende eines Geschäftsprozesses sein. Die Stelle wird durch ein rundes Rechteck dargestellt.

2. **Prozess**\
   Als Prozesselement wird jeder Prozess bezeichnet, der Eingabedaten erhält, diese verwendet und dadurch eine Ausgabe erzeugt. Ein solcher Prozess kann Berechnungen durchführen, Daten mithilfe von Logiken sortieren oder den Programmfluss anhand von Geschäftsregeln steuern. Zur Beschreibung eines solchen Prozesses wird eine kurze Bezeichnung verwendet, z. B. „Auftrag ausfüllen“ oder „Betrag berechnen“. Ein Prozess-Element wird durch ein Rechteck dargestellt.

3. **Entscheidung**\
   Eine Entscheidung stellt einen Punkt in dem Diagramm dar, an dem genau eine oder mehrere interne oder externe Entscheidungen getroffen werden. Dieses Element besteht aus einer Verzweigung und wird als Diamant dargestellt.

4. **Fluss**\
   Der Fluss zeigt die Übertragung von Informationen von einem Element des Systems zu einem Anderen. Der Fluss wird als Pfeillinie dargestellt. Der Fluss sollte einen Namen (kurze Beschreibung) haben, der angibt, welche Information bewegt wird. Ausnahmen sind Flüsse, bei denen klar ist, welche Informationen durch die Entitäten, die mit diesen Flüssen verbunden sind, übertragen werden. Beispielsweise werden neben Informationen auch reale Warenströme wie Materialverschiebungen in Systemen modelliert. Der Fluss sollte eine Art von Information übertragen. Der Pfeil zeigt die Flussrichtung an (er kann auch bidirektional sein, wenn Informationen von der Entität logisch abhängig sind – z. B. Frage und Antwort). Flüsse verbinden Prozesse, Datenspeicher und Terminatoren. Beispielsweise kann ein Datenfluss Rechnungen oder Anmeldedaten sein.

5. **Ein-/Ausgabe**\
   Die Aktivitäten eines Programmablaufplans benötigen häufig eine Eingabe als Information und die Aktivitäten produzieren wichtige Informationen als Ausgabe, der für die weiteren Prozessschritte benötigt wird. Die Ein- oder Ausgabe werden mit den jeweiligen Aktivitäten verknüpft, um den Algorithmus zu visualisieren. Diese Elemente werden durch ein Parallelogramm dargestellt.

6. **Unterprogramm**\
   Ein Unterprogramm wird modelliert, um innerhalb eines Prozesses einen inhaltlich zusammengehörenden Abschnitt zusammenzufassen. Subprozesse bilden den Vorteil einer guten Übersicht über den Gesamtprozess. Dadurch kann ein komplizierter Algorithmus einfach und klar dargestellt werden.

<image src="https://project-base.org/wp-content/uploads/2022/01/Programmablaufplan-Elemente-200x316.png.webp" alt="PAP">

## Programmablaufplan erstellen

Mit dem folgenden Leitfaden kannst du deinen Programmablaufplan einfach erstellen. Folge dazu den angegebenen Schritten. Zusätzlich wird jeder Schritt anhand eines Beispiels erläutert.

1. Zuerst wird das genaue Problem identifiziert. Welcher Prozess soll modelliert werden?

   In diesem Beispiel gehen wir von der Berechnung der Fakultät einer Zahl „n“ aus.

2. Im nächsten Schritt erstellst du eine vollständige Liste aller möglichen Prozesse, Unterprogramme, Grenzstellen und Entscheidungen.

   An dieser Stelle wird noch keine Reihenfolge von den Elementen geplant.

   | Prozess                    | Grenzstelle | Entscheidung |
   | -------------------------- | ----------- | ------------ |
   | Eingabe „n“ einlesen       | Start       | n ∈ N        |
   | Fehler ausgeben            | Ende        | n > 1        |
   | fakultaet = 1              |             |              |
   | fakultaet = fakultaet \* n |             |              |
   | n = n – 1                  |             |              |
   | fakultaet ausgeben         |             |              |

3. Im nächsten Schritt legst du Anfang und Ende deines Prozesses fest.

   Im Kernkonzept müssen der Anfang und das Ende ein Terminator (externe Entität) sein.

   | Anfang               | Ende                                |
   | -------------------- | ----------------------------------- |
   | Eingabe „n“ einlesen | Fehler ausgeben/ fakultaet ausgeben |

4. Entscheidest du die benötigte Ein- und Ausgabe zur Prozessen und Unterprogramme und ordnest du die zu.

   | Prozess              | Ein-/ Ausgabe |
   | -------------------- | ------------- |
   | Eingabe „n“ einlesen | Nummer „n“    |

5. Lege die Reihenfolge der Prozessen, Grenzstelle und Entscheidungen fest.

   | Grenzstelle | Prozess              | Entscheidung                            |
   | ----------- | -------------------- | --------------------------------------- |
   | Start       |                      |                                         |
   |             | Eingabe „n“ einlesen |                                         |
   |             |                      | n ∈ N                                   |
   |             |                      | (wenn n ∈ N) Fehler ausgeben            |
   | Ende        |                      |                                         |
   |             |                      | (wenn n !∈ N) fakultaet = 1             |
   |             |                      | n > 1                                   |
   |             |                      | (wenn n > 1) fakultaet = fakultaet \* n |
   |             |                      | n = n – 1                               |
   |             |                      | (wenn n !> 1) fakultaet ausgeben        |
   | Ende        |                      |                                         |

Quelle - 06.04.24:
https://project-base.org/flussdiagramm/programmablaufplan/

Erklärvideo:
[Youtube](https://www.youtube.com/watch?v=9LFPdqUMBqo&t=1s)

# Struktogramm (Nassi-Shneiderman-Diagramm)

Bei Struktogrammen, auch bekannt als Nassi-Shneiderman-Diagramme, werden die Programmkonstrukte "Sequenz", "Auswahl", und "Wiederholung" durch spezifische Symbole dargestellt. Diese Konstrukte können umfangreich modifiziert werden, um sie an die spezifischen Problemstellungen des Anwenders anzupassen. Ein Struktogramm wird stets von oben nach unten durchlaufen, wobei die Blöcke beliebig oft geschachtelt oder aufeinanderfolgend angeordnet werden können. Ein Block wird immer von oben betreten und unten verlassen.

### Sequenz

Eine Sequenz kann eine beliebige Anzahl von Programmanweisungen beinhalten, die nacheinander abgearbeitet werden.
<image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/sequenz.png" alt="struktogramm">

### Auswahl

Eine Auswahl beschreibt eine Verzweigung aufgrund einer eindeutigen Bedingung. Es gibt mehrere Möglichkeiten, den Auswahl-Typ zu erweitern:
<image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/auswahl.png" alt="struktogramm">

- Mehrfachverzweigung
  <image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/auswahlA.png" alt="struktogramm">
- Mehrfachverzweigung mit alternativer Verarbeitung
  <image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/auswahlB.png" alt="struktogramm">

### Wiederholung

Dieser Block führt aufgrund einer Bedingung eine bestimmte Anzahl von Durchläufen aus. Die Bedingung wird am Anfang des Blocks überprüft (Ausführungsbedingung). Ist die Bedingung erfüllt, wird der Anweisungsblock durchlaufen, andernfalls der nachfolgende Programmabschnitt.
<image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/wiederholung.png" alt="struktogramm">

**Abwandlungen des Wiederholungsblocks:**

- Wiederholung mit Abbruchbedingung: Die Bedingung wird am Ende der Schleife überprüft.
  <image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/abbruchbedingung.png" alt="struktogramm">

- Wiederholung mit unendlicher Schleife (loop): Eingangs- und Abbruchbedingung werden nicht explizit abgefragt. Dies funktioniert nur, wenn innerhalb des Blocks mindestens eine Abbruchbedingung vorgesehen ist.
  <image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/endlosschleife.png" alt="struktogramm">

### Analogismus in MATLAB

- **Sequenz**: Jede Zuweisung wie `v = [1 3 4]`
- **Auswahl**: `if-else-Block`
- **Mehrfachverzweigung**: `if-ifelse-Block` oder `switch-Block`
- **Wiederholung**: `for-Block` oder `while-Block`
- **Wiederholung mit unendlicher Schleife**: `while(true)-Block` mit Abbruchbedingung

### Beispiel

Ein Struktogramm illustriert die Voraussetzung zum Bestehen der IKT-Prüfung, einschließlich der Anmeldung zur Klausur, der Überprüfung der Note, und der Möglichkeit zur Notenverbesserung. Die Prüfung gilt als bestanden, wenn die Note besser als 5,0 ist. Bei einer besseren PST-Note kann eine Notenverbesserung vorgenommen werden.
<image src="https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/Struktogramm_bsp.1.png" alt="struktogramm">

Quelle - 06.04.24:
https://www.iim.maschinenbau.tu-darmstadt.de/kursunterlagen_archiv/ikt_ws1415/03/Theorie/nassishneidermandiagramm.html

Erklärvideo:
[Youtube](https://www.youtube.com/watch?v=uQa4DBrqF-g)
