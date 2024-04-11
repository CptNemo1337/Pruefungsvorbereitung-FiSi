---
title: "IPv4 oder IPv6"
date: 2024-04-10
draft: false
type: docs
description: "IPv4 oder IPv6"
---

## IPv4-Adressen Aufbau

- Eine IPv4-Adresse ist eine hierarchische 32-Bit-Adresse, die sich aus einem Netzwerk- und einem Host-Teil zusammensetzt.

## IPv4 Komunikationsformen / Adressschemata

- unicast	Host to Host
- broadcast	Host to all Hosts
- multicast	Host to more than one Host but not all Hosts

## IPv6-Adressen Aufbau

Eine IPv6-Adresse besteht aus 128 Bits, was im Vergleich zu IPv4-Adressen (32 Bits) eine erhebliche Erweiterung darstellt. Diese 128 Bits werden üblicherweise in acht Blöcke von jeweils 16 Bits aufgeteilt, die durch Doppelpunkte getrennt sind. Ein Beispiel für eine IPv6-Adresse ist:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

**Network-Identifier**: Die ersten 64 Bits einer IPv6-Adresse enthalten den **Netzwerkpräfix** und den **Subnet-Identifier** und identifizieren das Netzwerk. Der Präfix wird üblicherweise von einem Internetdienstanbieter (ISP) zugewiesen und hat eine Länge zwischen 32 und 56 Bit.

**Interface-Identifier**: Die letzten 64 Bits einer IPv6-Adresse enthalten den Interface-Identifier, der eindeutig ein Gerät in einem Netzwerk identifiziert. Dieser Teil kann basierend auf der MAC-Adresse des Geräts oder durch zufällige Generierung erstellt werden.

Die IPv6-Adressen können auch in verkürzter Form geschrieben werden, um sie handlicher zu machen. Dazu können führende Nullen in jedem Block weggelassen werden, und aufeinanderfolgende Blöcke von Nullen können durch Doppelpunkte ersetzt werden. Zum Beispiel kann die obige Adresse verkürzt werden als:

```
2001:db8:85a3::8a2e:370:7334
```

Es ist wichtig zu beachten, dass IPv6-Adressen im Gegensatz zu IPv4-Adressen normalerweise nicht in Dezimalzahlen geschrieben werden, sondern in Hexadezimalzahlen, um die Länge zu reduzieren und die menschliche Lesbarkeit zu verbessern.


[Erklär Video IPv6 Subnetting](https://www.youtube.com/watch?v=z2NDIHsxP1Q&t=458s)