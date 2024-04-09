---
title: "Routing"
date: 2024-04-07
draft: false
type: docs
description: "Routing"
---

Routing ist ein wesentlicher Bestandteil von Netzwerken, insbesondere im Internet. Es bezieht sich auf den Prozess, Datenpakete von einer Quelle zu einem Ziel durch ein Netzwerk zu leiten. 

**Quelle und Ziel**: Der Prozess des Routings beginnt, wenn ein Gerät (z. B. ein Computer oder ein Server) in einem Netzwerk Daten senden möchte. Diese Daten haben eine Quelladresse (die Adresse des sendenden Geräts) und eine Zieladresse (die Adresse des empfangenden Geräts).

**Routing-Entscheidung**: Das sendende Gerät schaut sich die Zieladresse der Datenpakete an und entscheidet, wie sie am besten zum Ziel geleitet werden können. Diese Entscheidung basiert auf einer Routing-Tabelle, die im Gerät gespeichert ist. Die Routing-Tabelle enthält Informationen darüber, wie verschiedene Netzwerkadressen erreicht werden können und welche Wege dafür am besten geeignet sind.

**Weiterleitung der Datenpakete**: Sobald das sendende Gerät eine Routing-Entscheidung getroffen hat, leitet es die Datenpakete an das nächste Gerät weiter, das sich auf dem Weg zum Ziel befindet. Dieses nächste Gerät wird als Router bezeichnet. Router sind spezielle Geräte, die für das Weiterleiten von Datenpaketen zwischen verschiedenen Netzwerken verantwortlich sind.

**Weiteres Routing**: Die Datenpakete werden von Router zu Router weitergeleitet, wobei jeder Router anhand seiner Routing-Tabelle entscheidet, wohin die Pakete als nächstes gesendet werden sollen. Dieser Prozess wird fortgesetzt, bis die Daten ihr Ziel erreichen.

**Ankunft am Ziel**: Schließlich erreichen die Datenpakete ihr Zielgerät. Dieses Zielgerät empfängt die Daten und kann entsprechend darauf reagieren, je nachdem, welche Art von Anwendung oder Dienst die Daten angefordert hat.

Beispiel

| Zielnetzwerk    | Subnetzmaske    | Gateway        | Schnittstelle   |
|-----------------|------------------|----------------|-----------------|
| 192.168.1.0     | 255.255.255.0    | 192.168.1.1    | LAN             |
| 192.168.2.0     | 255.255.255.0    | 192.168.2.1    | LAN             |
| 0.0.0.0         | 0.0.0.0          | 192.168.1.254  | WAN             |


- **Zielnetzwerk**: Dies ist die Zieladresse des Pakets, für die eine Routing-Entscheidung getroffen werden soll.

- **Subnetzmaske**: Die Subnetzmaske definiert, welche Teil der IP-Adresse die Netzwerkadresse und welche Teil die Hostadresse ist. Sie wird verwendet, um das Zielnetzwerk zu identifizieren.

- **Gateway**: Dies ist die IP-Adresse des nächsten Routers oder Gateways auf dem Weg zum Zielnetzwerk. Wenn das Zielnetzwerk lokal im selben Subnetz liegt, ist das Gateway die IP-Adresse des Geräts im lokalen Netzwerk.

- **Schnittstelle**: Dies ist die Netzwerkschnittstelle, über die das Paket weitergeleitet werden soll. Es kann entweder eine lokale Schnittstelle sein, die mit demselben Subnetz verbunden ist, oder eine Schnittstelle, die mit dem WAN (Wide Area Network) verbunden ist, das das Paket in Richtung des nächsten Routers im Netzwerk weiterleitet.

In diesem Beispiel wird beispielsweise festgelegt, dass Pakete, die an ein Zielnetzwerk mit der IP-Adresse 192.168.1.0/24 (d. h. Subnetzmaske 255.255.255.0) gerichtet sind, über das Gateway 192.168.1.1 und die lokale LAN-Schnittstelle weitergeleitet werden sollen. Wenn das Zielnetzwerk jedoch 192.168.2.0/24 ist, wird es ebenfalls lokal über die LAN-Schnittstelle erreicht, jedoch über das Gateway 192.168.2.1. Schließlich werden Pakete mit einem Ziel außerhalb der lokalen Subnetze (0.0.0.0/0) über das WAN-Gateway 192.168.1.254 und die entsprechende WAN-Schnittstelle weitergeleitet.