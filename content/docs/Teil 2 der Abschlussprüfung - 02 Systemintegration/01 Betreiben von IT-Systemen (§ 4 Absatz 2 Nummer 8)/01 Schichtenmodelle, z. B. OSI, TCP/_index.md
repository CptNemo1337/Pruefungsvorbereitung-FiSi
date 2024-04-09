---
title: "01 Schichtenmodelle, z. B. OSI, TCP"
date: 2024-04-07
draft: false
type: docs
description: "01 Schichtenmodelle, z. B. OSI, TCP description"
---

| Schicht         | Beschreibung                                | Protokolle/Technologien         |
|-----------------|---------------------------------------------|--------------------------------|
| Anwendungsschicht   | Bietet Dienste direkt für Anwendungen an, z. B. Dateiübertragung, E-Mail. | HTTP, FTP, SMTP, DNS          |
| Darstellungsschicht | Wandelt Daten in ein für die Übertragung geeignetes Format um und umgekehrt. | JPEG, GIF, ASCII, SSL         |
| Sitzungsschicht     | Ermöglicht die Kommunikation und Verwaltung von Sitzungen zwischen Anwendungen. | NetBIOS, SSH, RPC             |
| Transportschicht    | Ermöglicht die zuverlässige Kommunikation zwischen Endsystemen. | TCP, UDP                      |
| Vermittlungsschicht | Steuert die Weiterleitung von Datenpaketen durch das Netzwerk. | IP, ICMP, ARP                 |
| Sicherungsschicht   | Überträgt Daten zuverlässig zwischen direkt benachbarten Netzwerkknoten. | Ethernet, WLAN, PPP, HDLC     |
| Bitübertragungsschicht | Überträgt Bitfolgen über das physikalische Medium. | Ethernet PHY, DSL, Wi-Fi PHY |


| Protokoll         | Portnummer | Beschreibung                            |
|-------------------|------------|----------------------------------------|
| TCPMUX            | 1          | TCP Port Service Multiplexer           |
| TCP Port Service Multiplexer | 1 | TCP Port Service Multiplexer           |
| Echo              | 7          | Echo                                   |
| Discard           | 9          | Discard                                |
| systat            | 11         | Active Users                           |
| daytime           | 13         | Daytime                                |
| qotd              | 17         | Quote of the Day                       |
| chargen           | 19         | Character Generator                    |
| **FTP Data**          | 20         | File Transfer [Default Data]           |
| **FTP**               | 21         | File Transfer [Control]                |
| **SSH**               | 22         | Secure Shell (SSH)                     |
| **Telnet**            | 23         | Telnet                                 |
| **SMTP**              | 25         | Simple Mail Transfer Protocol (SMTP)   |
| time              | 37         | Time                                   |
| rlp               | 39         | Resource Location Protocol             |
| NIC Host Name     | 42         | Host Name Server                       |
| WHOIS             | 43         | WHOIS                                  |
| MTP               | 57         | Mail Transfer Protocol                 |
| TACACS-DS         | 65         | TACACS-Database Service                |
| **DNS**               | 53         | Domain Name System (DNS)               |
 Bootps            | 67         | Bootstrap Protocol Server              |
| Bootpc            | 68         | Bootstrap Protocol Client              |
| **TFTP**              | 69         | Trivial File Transfer Protocol (TFTP)  |
| gopher            | 70         | Gopher                                 |
| rje               | 77         | Remote Job Entry                       |
| Finger            | 79         | Finger                                 |
| **http**              | 80         | Hypertext Transfer Protocol (HTTP)     |
| Kerberos          | 88         | Kerberos                               |
| **pop3**              | 110        | Post Office Protocol - Version 3 (POP3)|
| **NTP**               | 123        | Network Time Protocol (NTP)            |
| NetBIOS           | 137        | NetBIOS Name Service                   |
| NetBIOS           | 138        | NetBIOS Datagram Service               |
| NetBIOS           | 139        | NetBIOS Session Service                |
| IMAP4             | 143        | Internet Message Access Protocol (IMAP)|
| **SNMP**              | 161        | Simple Network Management Protocol (SNMP)|
| SNMP Trap         | 162        | SNMP Trap (SNMPTRAP)                   |
| bgp               | 179        | Border Gateway Protocol (BGP)          |
| ldap              | 389        | Lightweight Directory Access Protocol (LDAP)|
| **https**             | 443        | HTTP Secure (HTTPS)                    |
| Microsoft-DS      | 445        | Microsoft-DS                           |
| exec              | 512        | Remote Process Execution               |
| login             | 513        | Remote Login                           |
| shell             | 514        | Remote Shell                           |
| printer           | 515        | Printer                                |
| talk              | 517        | Talk                                   |
| ntalk             | 518        | Unix Time Stamp                        |
| utime             | 519        | Unix Time Stamp                        |
| efs               | 520        | Extended File Name Server              |
| timed             | 525        | Timed                                  |
| tempo             | 526        | Newdate                                |
| courier           | 530        | Courier                                |
| conference        | 531        | Conference                             |
| netnews           | 532        | Netnews                                |
| uucp              | 540        | UUCP                                   |
| klogin            | 543        | Kerberos Login                         |
| kshell            | 544        | Kerberos Shell                         |
| kerberos-adm      | 749        | Kerberos administration               |
| **nntp**              | 119        | Network News Transfer Protocol (NNTP) |
| irc               | 194        | Internet Relay Chat (IRC)              |
| **POP3S**             | 995        | Post Office Protocol 3 over TLS/SSL (POP3S)|
| **IMAPS**             | 993        | Internet Message Access Protocol over TLS/SSL (IMAPS)|
| LDAPS             | 636        | Lightweight Directory Access Protocol over TLS/SSL (LDAPS)|
| **telnets**           | 992        | Telnet over TLS/SSL                    |
| submission        | 587        | Message Submission                     |
| syslog            | 514        | Remote Syslog                          |
| uucp-path         | 117        | UUCP Path Service                      |
| tcpwrapped        | 7          | TCP Wrapped Services                   |