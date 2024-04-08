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

Hier ist dein Lernzettel in Markdown, basierend auf der Struktur der Webseite, die du angegeben hast. Dieses Format kann in einer Markdown-fähigen Umgebung, wie z.B. GitHub, GitLab oder einem lokalen Markdown-Editor, verwendet werden.

# Git - Der einfache Einstieg

Eine einfache Anleitung, um Git zu lernen. Kein Schnick-Schnack ;)

## Installation

- [Git für OS X herunterladen](http://git-scm.com/download/mac)
- [Git für Windows herunterladen](http://msysgit.github.io/)
- [Git für Linux herunterladen](http://book.git-scm.com/2_installing_git.html)

## Neues Repository erstellen

Erstelle ein neues Verzeichnis, öffne es und führe `git init` aus, um ein neues git-Repository anzulegen.

## Ein Repository auschecken

Erstelle eine Arbeitskopie, indem du folgenden Befehl ausführst:

```
git clone /pfad/zum/repository
```

Falls du ein entferntes Repository verwendest, benutze:

```
git clone benutzername@host:/pfad/zum/repository
```

## Workflow

Dein lokales Repository besteht aus drei "Instanzen", die von git verwaltet werden. Die erste ist deine `Arbeitskopie`, welche die echten Dateien enthält. Die zweite ist der `Index`, welcher als Zwischenstufe agiert und zu guter Letzt noch der `HEAD`, der auf deinen letzten Commit zeigt.

![Workflow](img/trees.png)

## Add & Commit

Du kannst Änderungen vorschlagen (zum Index hinzufügen) mit:

```
git add <dateiname>
git add *
```

Das ist der erste Schritt im git workflow, du bestätigst deine Änderungen mit:

```
git commit -m "Commit-Nachricht"
```

Jetzt befindet sich die Änderung im HEAD, aber noch nicht im entfernten Repository.

## Änderungen hochladen

Die Änderungen sind jetzt im HEAD deines lokalen Repositories. Um die Änderungen an dein entferntes Repository zu senden, führe:

```
git push origin master
```

aus. Du kannst `master` auch mit einem beliebigen anderen Branch ersetzen.

## Branching

Branches werden benutzt, um verschiedene Funktionen isoliert voneinander zu entwickeln.

![Branching](img/branches.png)

Erstelle einen neuen Branch mit dem Namen "feature_x" und wechsle zu diesem:

```
git checkout -b feature_x
```

Um zum Master zurück zu wechseln:

```
git checkout master
```

Und um den eben erstellten Branch wieder zu löschen:

```
git branch -d feature_x
```

Ein Branch ist nicht für andere verfügbar, bis du diesen in dein entferntes Repository hochlädst:

```
git push origin <branch>
```

## Update & Merge

Um dein lokales Repository mit den neuesten Änderungen zu aktualisieren, verwende:

```
git pull
```

in deiner Arbeitskopie, um die Änderungen erst herunterzuladen (fetch) und dann mit deinem Stand zusammenzuführen (merge).

## Tagging

Es wird empfohlen, für Software Releasestags zu verwenden. Du kannst einen neuen Tag namens `1.0.0` erstellen mit:

```
git tag 1.0.0 1b2e1d63ff
```

## Änderungen rückgängig machen

Wenn du mal etwas falsch machst, kannst du die lokalen Änderungen mit folgendem Befehl zurücksetzen:

```
git checkout -- <filename>
```

## Nützliche Tricks

- Eingebaute git-GUI: `gitk`
- Farbige Konsolenausgabe: `git config color.ui true`
- Eine Zeile pro Commit in der Logausgabe: `git config format.pretty oneline`
- Interaktives Hinzufügen von Änderungen: `git add -i`

## Links

### Grafische Clients

- [GitX (L) (OS X, Open Source)](http://gitx.laullon.com/)
- [Tower (OS X)](http://www.git-tower.com/)
- [Source Tree (OS X, kostenlos)](http://www.sourcetreeapp.com/)
- [GitHub for Mac (OS X, kostenlos)](http://mac.github.com/)
- [GitBox (OS X)](https://itunes.apple.com/gb/app/gitbox/id403388357?mt=12

)

### Anleitungen

- [Git Community Book](http://book.git-scm.com/)
- [Pro Git](http://progit.org/book/)
- [Think like a git](http://think-like-a-git.net/)
- [GitHub Help](http://help.github.com/)
- [A Visual Git Guide](http://marklodato.github.com/visual-git-guide/index-en.html)

Deine Anleitung sieht schon sehr gut und umfassend aus! Sie deckt viele wichtige Aspekte von Git ab und bietet sowohl Einsteigern als auch fortgeschrittenen Benutzern wertvolle Informationen. Die Integration von praktischen Beispielen und nützlichen Links macht sie besonders hilfreich.

Nun zur Nutzung von Git in Visual Studio Code (VSCode):

# Git in Visual Studio Code

Visual Studio Code (VSCode) bietet eine ausgezeichnete Unterstützung für Git, die es Entwicklern ermöglicht, Git-Operationen direkt aus der Entwicklungsumgebung heraus durchzuführen, ohne auf die Kommandozeile wechseln zu müssen. Hier ist eine kurze Anleitung, wie Git in VSCode verwendet wird.

### Git-Integration aktivieren

VSCode erkennt automatisch Git-Repositories in geöffneten Ordnern, sofern Git auf Ihrem System installiert ist. Um zu überprüfen, ob Git korrekt erkannt wurde, öffnen Sie den Befehlspalette (mit `Strg+Shift+P` oder `Cmd+Shift+P` auf macOS) und geben Sie `Git: Show Git Output` ein. Sollten keine Fehler angezeigt werden, ist Git korrekt eingerichtet.

### Grundlegende Git-Operationen in VSCode

- **Änderungen Stageen**: Ändern Sie Dateien in Ihrem Projekt und öffnen Sie dann die Git-Seitenleiste (zu finden unter dem SCM-Symbol auf der Seitenleiste oder durch Drücken von `Strg+Shift+G` / `Cmd+Shift+G`). Hier können Sie Dateien zum Staging-Bereich hinzufügen, indem Sie auf das „+“-Symbol neben jeder Datei klicken.
- **Commit**: Nachdem Sie Ihre Änderungen gestaged haben, geben Sie eine Commit-Nachricht in das Textfeld oben in der Git-Seitenleiste ein und drücken Sie `Strg+Enter` / `Cmd+Enter`, um den Commit zu erstellen.
- **Push und Pull**: Um Ihre Änderungen zu pushen, klicken Sie auf die `...`-Schaltfläche in der oberen rechten Ecke der Git-Seitenleiste und wählen Sie `Push`. Um Änderungen von einem Remote-Repository zu holen, wählen Sie `Pull`.

### Branches verwalten

- Um einen neuen Branch zu erstellen, klicken Sie auf den Branch-Namen in der unteren linken Ecke des VSCode-Fensters. Geben Sie den Namen des neuen Branches ein und bestätigen Sie mit Enter.
- Um zwischen Branches zu wechseln, klicken Sie erneut auf den Branch-Namen und wählen Sie den Branch aus, zu dem Sie wechseln möchten.

### Merge-Konflikte lösen

Wenn VSCode einen Merge-Konflikt erkennt, öffnet es einen speziellen Editor, der die Konflikte anzeigt. Sie können zwischen `Incoming Change` (den Änderungen aus dem Branch, den Sie mergen möchten) und `Current Change` (Ihren Änderungen) wählen oder beide Änderungen akzeptieren. Nachdem Sie die Konflikte gelöst haben, speichern Sie die Datei und committen Sie die Lösung.

### Erweiterungen für erweiterte Git-Operationen

VSCode hat einen blühenden Marktplatz für Erweiterungen, die die Git-Unterstützung erweitern. Beliebte Erweiterungen sind:

- **GitLens**: Bietet erweiterte Git-Funktionalitäten direkt in VSCode, einschließlich Blame-Informationen, Änderungsverläufe und vieles mehr.
- **Git Graph**: Zeigt einen visuellen Graphen aller Commits und Branches in Ihrem Repository.

### Fazit

VSCode und Git zusammen bieten eine leistungsstarke Kombination für Softwareentwicklung und -versionierung. Die Integration von Git in VSCode vereinfacht den Entwicklungsworkflow erheblich und macht viele Operationen effizienter und zugänglicher.
