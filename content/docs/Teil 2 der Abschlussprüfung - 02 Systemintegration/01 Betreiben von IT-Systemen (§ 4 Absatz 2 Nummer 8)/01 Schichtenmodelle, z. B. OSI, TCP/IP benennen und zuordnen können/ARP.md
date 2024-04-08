---
title: "ARP"
date: 2024-04-07
draft: false
type: docs
description: "ARP"
---

**Grundlegende Funktion:** ARP ermöglicht es Geräten in einem lokalen Netzwerk, die MAC-Adresse eines anderen Geräts zu ermitteln, wenn nur dessen IP-Adresse bekannt ist.

**ARP-Tabelle:** Jedes Gerät im Netzwerk enthält eine ARP-Tabelle, die eine Zuordnung von IP-Adressen zu MAC-Adressen speichert. Diese Tabelle wird verwendet, um den Netzwerkverkehr effizient zu leiten.

**ARP-Anfrage und -Antwort:** Wenn ein Gerät die MAC-Adresse eines anderen Geräts benötigt, sendet es eine ARP-Anfrage an das Netzwerk mit der Ziel-IP-Adresse. Das Gerät mit dieser IP-Adresse antwortet dann mit seiner MAC-Adresse.

**ARP-Cache:** Um die Effizienz zu steigern, speichern Geräte die Ergebnisse von ARP-Anfragen in einem Cache, um bei Bedarf schnell auf sie zugreifen zu können. Dieser Cache wird verwendet, um zukünftige ARP-Anfragen zu beantworten, ohne das Netzwerk zu belasten.

**ARP und IPv6:** Während ARP hauptsächlich mit IPv4 verwendet wird, gibt es auch ein ähnliches Protokoll für IPv6, das als Neighbor Discovery Protocol (NDP) bekannt ist. NDP bietet ähnliche Funktionen wie ARP, aber mit einigen Unterschieden und zusätzlichen Funktionen für IPv6-Netzwerke.