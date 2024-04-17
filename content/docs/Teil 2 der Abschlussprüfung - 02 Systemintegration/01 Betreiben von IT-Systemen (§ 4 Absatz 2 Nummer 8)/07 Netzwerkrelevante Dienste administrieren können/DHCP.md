---
title: "DHCP"
date: 2024-04-07
draft: false
type: docs
description: "DHCP"
---

# DHCP

DHCP steht für "Dynamic Host Configuration Protocol". Es ist ein Netzwerkprotokoll, das automatisch IP-Adressen und andere Netzwerkeinstellungen an Geräte in einem Netzwerk verteilt. 

## DHCP Funktionsweise 

| Schritt              | Aktion                                                         |
|----------------------|----------------------------------------------------------------|
| 1. Anfrage (Discover)| Das Gerät sendet eine DHCP-Anfrage, um eine IP-Adresse zu      |
|                      | erhalten. Diese Anfrage wird als "Discover"-Nachricht bezeichnet|
|                      | und an alle Geräte im Netzwerk gesendet.                      |
|----------------------|----------------------------------------------------------------|
| 2. Angebot (Offer)   | DHCP-Server im Netzwerk empfangen die Discover-Nachricht und   |
|                      | antworten mit einem Angebot ("Offer"). Der DHCP-Server         |
|                      | schlägt eine verfügbare IP-Adresse vor.                       |
|----------------------|----------------------------------------------------------------|
| 3. Anforderung       | Das Gerät wählt aus den Angeboten einen DHCP-Server aus und    |
|    (Request)         | sendet eine Anforderung ("Request") für die zugewiesene        |
|                      | IP-Adresse an diesen Server.                                   |
|----------------------|----------------------------------------------------------------|
| 4. Bestätigung       | Der DHCP-Server vergibt die IP-Adresse an das Gerät und sendet |
|    (Acknowledge)     | eine Bestätigung ("Acknowledge"). Diese enthält neben der       |
|                      | IP-Adresse auch andere Netzwerkkonfigurationseinstellungen.    |
|----------------------|----------------------------------------------------------------|
| 5. Nutzung           | Das Gerät verwendet nun die zugewiesene IP-Adresse und andere  |
|                      | Netzwerkkonfigurationseinstellungen, um mit dem Netzwerk zu     |
|                      | kommunizieren.                                                 |
