---
title: "Switching"
date: 2024-04-07
draft: false
type: docs
description: "Switching"
---

Switching ist ein Prozess in Netzwerken, bei dem Datenpakete innerhalb eines lokalen Netzwerks (LAN) effizient weitergeleitet werden. Im Gegensatz zum Routing, das Datenpakete zwischen verschiedenen Netzwerken (z. B. LANs) weiterleitet, bezieht sich Switching auf die Weiterleitung von Daten innerhalb desselben Netzwerks. Hier ist eine grundlegende Erklärung, wie Switching funktioniert:

**Ankunft von Datenpaketen**: Datenpakete, die von Geräten im lokalen Netzwerk generiert werden (z. B. Computer, Drucker, Server), gelangen zum Switch.

**Zieladressenlernen**: Beim ersten Eintreffen eines Datenpakets überprüft der Switch die Ziel-MAC-Adresse (Media Access Control) des Pakets. Die MAC-Adresse identifiziert ein bestimmtes Gerät in einem Netzwerk. Der Switch speichert die MAC-Adresse des Absenders und die Schnittstelle, über die das Paket empfangen wurde, in seiner MAC-Adresstabelle.

**Weiterleitung von Datenpaketen**: Wenn ein Datenpaket an den Switch gesendet wird und die Ziel-MAC-Adresse in seiner MAC-Adresstabelle vorhanden ist, leitet der Switch das Paket direkt an die Schnittstelle weiter, die mit dem Gerät verbunden ist, das dieser MAC-Adresse entspricht. Dadurch werden Datenpakete nur an die Geräte gesendet, für die sie bestimmt sind, was die Netzwerkleistung verbessert.

**Broadcasts und Unbekanntes**: Wenn die Ziel-MAC-Adresse nicht in der MAC-Adresstabelle des Switches vorhanden ist oder das Paket an eine Broadcast-Adresse gerichtet ist (z. B. ARP-Anforderungen), wird das Paket an alle angeschlossenen Schnittstellen (außer derjenigen, über die das Paket empfangen wurde) weitergeleitet.

**Aktualisierung der MAC-Adresstabelle**: Der Switch aktualisiert kontinuierlich seine MAC-Adresstabelle, indem er die Quell-MAC-Adressen von Paketen überwacht, die über seine Schnittstellen empfangen werden.

Switching ist schnell und effizient, da es Datenpakete nur an die erforderlichen Ziele weiterleitet und nicht die gesamte Netzwerkverkehrslast an alle angeschlossenen Geräte sendet. Es ist ein wesentlicher Bestandteil von lokalen Netzwerken und wird häufig in Bürogebäuden, Rechenzentren und anderen Umgebungen eingesetzt, um eine schnelle und zuverlässige Kommunikation zwischen Geräten zu ermöglichen.