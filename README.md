#  TPot Honeypot Analyse – April 2025

Dieses Projekt dokumentiert die Ergebnisse eines Honeypot-Experiments mit *TPot, betrieben vom **01.04.2025* bis zum *14.04.2025*.  
Ziel war es, Angriffe auf ein exponiertes System zu überwachen, deren Muster zu analysieren und mögliche Trends zu erkennen.

---

## Projektübersicht

•⁠  ⁠*Zeitraum:* 01.04.2025 – 14.04.2025  
•⁠  ⁠*Plattform:* Vultr Cloud Hosting  
•⁠  ⁠*Serverstandort:* Frankfurt am Main, Deutschland  
•⁠  ⁠*Honeypot-Framework:* [TPot](https://github.com/telekom-security/tpotce)  
•⁠  ⁠*Zweck:* Analyse von Angriffsverhalten, Schwachstellen-Scanning, Credential Stuffing und OS-Identifikation.

---

## Datenübersicht

Alle Rohdaten befinden sich im Ordner [⁠ Daten Tpot/ ⁠](./Daten Tpot):

 1.⁠ ⁠⁠ attacks_histogram.csv ⁠ – Angriffe pro 12 Stunden inkl. Unique Source IPs  
 2.⁠ ⁠⁠ os_distribution.csv ⁠ – Betriebssystemverteilung der Angreifer  
 3.⁠ ⁠⁠ suricata_alerts.csv ⁠ – Alerts nach Kategorien  
 4.⁠ ⁠⁠ suricata_signatures.csv ⁠ – Top Suricata-Signaturen  
 5.⁠ ⁠⁠ suricata_cves.csv ⁠ – Erfasste CVEs  
 6.⁠ ⁠⁠ attacker_asn_top10.csv ⁠ – Top 10 Angreifer-Provider (ASN)  
 7.⁠ ⁠⁠ attacker_source_ip_top10.csv ⁠ – Meistgenutzte Angreifer-IP-Adressen  
 8.⁠ ⁠⁠ attacker_ip_reputation.csv ⁠ – IP-Reputationsanalyse  
 9.⁠ ⁠⁠ attacks_by_country_and_port.csv ⁠ – Länder + Zielports  
10.⁠ ⁠⁠ attacks_by_country.csv ⁠ – Gesamtanzahl Angriffe pro Land  
11.⁠ ⁠⁠ attacks_by_country_histogram.csv ⁠ – Angriffe pro Land im Zeitverlauf  
12.⁠ ⁠⁠ credentials_username_tagcloud.csv ⁠ – Häufigste Benutzernamen  
13.⁠ ⁠⁠ credentials_password_tagcloud.csv ⁠ – Häufigste Passwörter  
14.⁠ ⁠⁠ attack_map_data.csv ⁠ – Geo-Koordinaten für Angriffe  
15.⁠ ⁠⁠ protocol_distribution.csv ⁠ – Verteilung nach Netzwerkprotokollen  
16.⁠ ⁠⁠ port_scan_distribution.csv ⁠ – Häufigkeit der gescannten Ports

---

## Wichtige Erkenntnisse

•⁠  ⁠*Gesamtzahl Angriffe:* > 900.000 Events innerhalb von 14 Tagen  
•⁠  ⁠*Häufigstes Angriffs-OS:* Windows NT Kernel (über 1 Million Events)  
•⁠  ⁠*Top Suricata-Alert:* ⁠ SURICATA IPv4 truncated packet ⁠  
•⁠  ⁠*Meistgenutzte Schwachstelle:* ⁠ CVE-2020-11899 ⁠  
•⁠  ⁠*Auffällige Peaks:* Besonders hoher Traffic am 03.04.2025 und 12.04.2025

---

##  Visualisierungen

Screenshots und generierte Diagramme befinden sich im Ordner [⁠ Screenshots/ ⁠](./Screenshots):
 
•⁠  ⁠*Username-Tagcloud* – ⁠ username_tagcloud.png ⁠  
•⁠  ⁠*Passwort-Tagcloud* – ⁠ password_tagcloud.png ⁠  
•⁠  ⁠*Attack Map* – ⁠ attack_map.png ⁠  

---

## Beispiel-Angriffsmuster

•⁠  ⁠*Credential Stuffing:* Auffällige Wiederverwendung bestimmter User-Passwort-Kombinationen  
•⁠  ⁠*Netzwerkscans:* Erkennung mehrerer globaler IP-Scanner (u.a. ZMap)  
•⁠  ⁠*Protokoll-Missbrauch:* Häufige fehlerhafte TCP-Pakete und SMBv1-Scans

---

## Lessons Learned

 1.⁠ ⁠Exponierte Systeme werden *innerhalb weniger Minuten* nach Deployment angegriffen  
 2.⁠ ⁠Mehrheit der Angriffe erfolgt *automatisiert* (Bots / Malware-Kampagnen)  
 3.⁠ ⁠Alte Protokolle und Dienste (z. B. SMBv1) bleiben ein bevorzugtes Ziel

---

##  Kontakt

Falls du Fragen hast oder über ähnliche Projekte sprechen möchtest:  
*Autor:* [Dein Name]  
*GitHub:*Brass53 (https://github.com/Brass53)
