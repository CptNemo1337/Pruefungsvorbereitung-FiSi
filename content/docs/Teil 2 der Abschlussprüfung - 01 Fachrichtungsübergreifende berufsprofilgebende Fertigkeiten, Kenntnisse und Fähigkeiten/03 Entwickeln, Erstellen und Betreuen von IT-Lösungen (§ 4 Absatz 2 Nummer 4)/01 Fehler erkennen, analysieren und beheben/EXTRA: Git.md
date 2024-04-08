---
title: "EXTRA: Git Grundlagen und Best Practises"
date: 2024-04-07
draft: false
type: docs
description: "EXTRA: Git"
---

Git ist ein verteiltes Versionskontrollsystem, das von Linus Torvalds erstellt wurde. Es wird verwendet, um die Entwicklungsverläufe von Dateien, insbesondere von Quellcode in Softwareprojekten, zu verfolgen. Die Hauptvorteile von Git sind seine Geschwindigkeit, Datenintegrität und Unterstützung für verteilte, nicht-lineare Arbeitsabläufe. Hier wird erklärt, wie Git funktioniert, einschließlich seiner Funktionalität, Befehle und Workflow-Prozesse.

## Systemarchitektur von Git

- **Repository (Repo):** Ein Git-Repository ist ein virtueller Speicherort Ihres Projekts. Es ermöglicht Ihnen, die Versionen der Dateien zu verfolgen, Branches zu erstellen, zu mergen und vieles mehr.
- **Commit:** Eine Änderung im Repository, die die aktuelle Version der Dateien zu einem bestimmten Zeitpunkt speichert.
- **Branch:** Eine unabhängige Linie der Entwicklung, die genutzt wird, um an verschiedenen Features oder Versionen eines Projekts gleichzeitig zu arbeiten.
- **Merge:** Das Zusammenführen von Änderungen aus verschiedenen Branches in einen einzigen Branch.
- **Remote:** Ein verlinktes Repository, das typischerweise online gehostet wird und zur Synchronisierung von Änderungen mit anderen Entwicklern verwendet wird.

## Grundlegende Befehle

1. **git init**: Initialisiert ein neues Git-Repository.
2. **git clone [URL]**: Klont ein Repository von einer URL.
3. **git add [Dateiname]**: Fügt Dateien dem Staging-Bereich hinzu.
4. **git commit -m "Nachricht"**: Erstellt einen neuen Commit mit einer Nachricht.
5. **git status**: Zeigt den Status der geänderten Dateien.
6. **git push [Remote-Name] [Branch-Name]**: Schickt Commits zum Remote-Repository.
7. **git pull [Remote-Name] [Branch-Name]**: Holt Commits vom Remote-Repository und führt sie mit dem lokalen Repository zusammen.
8. **git branch [Branch-Name]**: Erstellt einen neuen Branch.
9. **git checkout [Branch-Name]**: Wechselt zu einem anderen Branch.
10. **git merge [Branch-Name]**: Führt einen anderen Branch in den aktuellen Branch zusammen.

## Branching und Merging

- **Branching** erlaubt es Entwicklern, unabhängig voneinander an verschiedenen Features zu arbeiten, ohne den Hauptentwicklungszweig (master/main) zu beeinflussen.
- **Merging** wird verwendet, um Änderungen aus einem Branch in einen anderen (z.B. main) zu integrieren. Konflikte können auftreten, wenn die gleichen Zeilen des Codes in beiden Branches geändert wurden. Diese müssen manuell gelöst werden.

## Best Practices

1. **Commit-Nachrichten sollten klar und beschreibend sein.**
2. **Regelmäßige Commits halten das Repository aktuell und minimieren Konflikte.**
3. **Feature-Branches für jede neue Funktion oder Verbesserung nutzen, um die Integrität des Hauptzweigs zu bewahren.**
4. **Vor dem Pushen immer pullen, um Merge-Konflikte zu vermeiden.**
5. **Review-Prozesse einrichten, um Code-Qualität und Konsistenz zu gewährleisten.**

Git ist ein mächtiges Tool, das, wenn es richtig eingesetzt wird, die Entwicklung und Zusammenarbeit in Softwareprojekten erheblich verbessern kann. Durch das Verständnis und die Anwendung der oben genannten Konzepte und Befehle können Entwickler effizient mit Git arbeiten und ihre Projekte erfolgreich verwalten.

Hier sind einige konkrete Beispiele, die zeigen, wie man die beschriebenen Git-Befehle und -Praktiken in der Praxis anwendet.

## Initialisierung eines neuen Repositories

Um ein neues Git-Repository zu initialisieren, öffnen Sie das Terminal, navigieren Sie zu Ihrem Projektverzeichnis und führen Sie den folgenden Befehl aus:

```bash
git init
```

Dieser Befehl erstellt ein neues Git-Repository im aktuellen Verzeichnis.

## Klonen eines bestehenden Repositories

Um ein bestehendes Repository zu klonen, verwenden Sie:

```bash
git clone https://github.com/benutzername/repository-name.git
```

Ersetzen Sie `https://github.com/benutzername/repository-name.git` durch die URL des Repositories, das Sie klonen möchten.

## Änderungen hinzufügen und committen

Wenn Sie eine Datei geändert haben und diese Änderungen committen möchten, verwenden Sie:

```bash
git add dateiname.txt
git commit -m "Eine aussagekräftige Commit-Nachricht"
```

Ersetzen Sie `dateiname.txt` durch den Namen der Datei, die Sie committen möchten.

## Arbeiten mit Branches

Um einen neuen Branch zu erstellen und sofort dorthin zu wechseln:

```bash
git checkout -b neuer-branch-name
```

Um zu einem anderen Branch zu wechseln:

```bash
git checkout existierender-branch-name
```

Um einen Branch mit dem aktuellen Branch zu mergen:

```bash
git merge anderer-branch-name
```

## Änderungen pushen und pullen

Um Ihre lokalen Commits zu einem Remote-Repository (z.B. GitHub) zu pushen:

```bash
git push origin main
```

Ersetzen Sie `main` mit dem Namen des Branches, den Sie pushen möchten.

Um Änderungen von einem Remote-Repository zu holen und mit Ihrem lokalen Repository zu mergen:

```bash
git pull origin main
```

## Konflikte lösen

Konflikte treten auf, wenn Git nicht automatisch Änderungen zusammenführen kann. Git markiert die betroffenen Dateien und Sie müssen die Konflikte manuell lösen, indem Sie die Dateien bearbeiten und die gewünschten Änderungen auswählen. Nachdem Sie die Konflikte gelöst haben, fügen Sie die Dateien zum Staging-Bereich hinzu und committen Sie sie:

```bash
git add .
git commit -m "Konflikte gelöst"
```

## Best Practices umsetzen

- **Regelmäßige Commits**: Führen Sie kleine, fokussierte Änderungen durch und committen Sie diese regelmäßig mit klaren Nachrichten.
- **Review-Prozesse**: Nutzen Sie Pull Requests (auf Plattformen wie GitHub), um Code-Reviews zu erleichtern, bevor Änderungen gemerged werden.
- **Branching-Strategie**: Arbeiten Sie für neue Features in separaten Branches und mergen Sie diese zurück in den Hauptbranch (`main` oder `master`), sobald sie fertiggestellt sind.

Durch das Befolgen dieser Beispiele und Praktiken können Sie effektiver mit Git arbeiten und eine solide Basis für die Zusammenarbeit in Softwareprojekten schaffen.
