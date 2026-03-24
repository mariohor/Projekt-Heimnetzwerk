# 🛡️ Virtuelle Netzwerk- & Security-Umgebung (Heimnetzwerk)

## 🗺️ Netzwerkdiagramm

Eine visuelle Übersicht über die gesamte virtuelle Umgebung:

<p align="center">
  <img src="screenshoots/Netzwerktopologie.jpg" alt="Netzwerktopologie" width="700">
</p>




## 📌 Projektübersicht

Dieses Projekt zeigt den Aufbau einer virtualisierten Netzwerkumgebung mit mehreren Linux- und Windows-Systemen. Ziel war es, sichere Kommunikation zwischen den Systemen zu ermöglichen sowie Remotezugriffe effizient und praxisnah umzusetzen.

Dabei lag der Fokus auf SSH-Authentifizierung, Netzwerkverständnis und der Nutzung eines modernen VPNs (Tailscale).

---

## 🎯 Ziel des Projekts

- Aufbau einer virtuellen Testumgebung  
- Sichere Verbindung zwischen mehreren Systemen  
- Umsetzung von SSH-Key-basierter Authentifizierung  
- Einrichtung eines einfachen, sicheren Remotezugriffs  
- Verständnis von IP-Strukturen und Netzwerkkommunikation  

---

## 🏗️ Setup

- Virtualisierung: Oracle VM VirtualBox  
- Mehrere virtuelle Maschinen (Linux & Windows)  
- Gemeinsames Netzwerk zur Kommunikation  

---

## 🖥️ Verwendete Systeme

- Debian  
- AlmaLinux  
- Ubuntu Server  
- Ubuntu Desktop  
- Arch Linux  
- Windows 11  


<p align="center">
  <img src="screenshoots/VirtualBox-Übersicht.jpg" alt="VirtualBox Übersicht" width="700">
</p>


---

## ⚙️ Umsetzung

- Installation mehrerer Betriebssysteme in VirtualBox  
- Aktualisierung aller Systeme auf den neuesten Stand  
- Aufbau einer funktionierenden Netzwerkverbindung zwischen den VMs  
- Einrichtung von Remotezugriffen (SSH & RDP)  

---

## 🔐 SSH-Konfiguration

✔ Gemeinsame Einstellungen auf allen Systemen
PermitRootLogin no  
Root‑Login ist deaktiviert, um unbefugten Zugriff zu verhindern.

PubkeyAuthentication yes  
Nur SSH‑Key‑Authentifizierung ist erlaubt.

PasswordAuthentication no  
Passwort‑Login wurde vollständig abgeschaltet.

MaxSessions 1  
Jede Verbindung erlaubt nur eine aktive SSH‑Session.

Port 50000  
SSH läuft auf einem alternativen Port, um Standard‑Scans zu reduzieren.

<p align="center">
  <img src="screenshoots/PermitRootLogin%20no.jpg" alt="PermitRootLogin no" width="45%">
  <img src="screenshoots/Port%2050000.jpg" alt="Port 50000" width="45%">
</p>


Um den Zugriff innerhalb der virtuellen Umgebung zu vereinfachen, habe ich alle Hostnames der Systeme (z. B. arch, debian, ubuntu-desktop, alma, win11) zentral dokumentiert. Dadurch kann ich mich deutlich schneller verbinden, ohne IP‑Adressen nachschlagen zu müssen.

<p align="center">
  <img src="screenshoots/SSH-Konfiguration%20unter%20Windows.jpg" alt="SSH-Konfiguration unter Windows" width="700">
</p>


- Erstellung von SSH-Key-Paaren  
- Verteilung der Public Keys auf Linux-Systeme  
- Passwortlose Anmeldung zwischen Systemen  

Beispiel:
ssh arch

➡️ Direkter Zugriff von Windows 11 auf Arch Linux ohne Passwort

<p align="center">
  <img src="screenshoots/SSH-Verbindung%20-%20Alma%20to%20Debian%20and%20Ubuntu%20Desktop%20.jpg" alt="SSH Verbindung Alma" width="45%">
  <img src="screenshoots/SSH-Verbindung%20-%3E%20win11-ubuntu%20desktop.jpg" alt="SSH Verbindung Win11" width="45%">
</p>



🌐 Netzwerk
Kommunikation zwischen allen Systemen innerhalb der virtuellen Umgebung
Nutzung von Hostnames zur Vereinfachung des Zugriffs

🔗 VPN (Tailscale)
Integration aller Systeme in ein Tailscale-Netzwerk
Automatische Vergabe zusätzlicher IP-Adressen
Zugriff auf Systeme über diese IP-Adressen von überall

Beispiel:
ssh user@100.x.x.x

---

## 🧠 Was ich gelernt habe

Vertieftes Verständnis für virtuelle Netzwerkarchitekturen und die Kommunikation zwischen verschiedenen Betriebssystemen innerhalb einer gemeinsamen Umgebung.

Sichere SSH‑Konfigurationen inklusive Key‑Authentifizierung, Port‑Anpassungen und Hostname‑basiertem Zugriff.

Analyse und Behebung typischer Netzwerkprobleme, z. B. DNS‑Fehler, Routing‑Konflikte, Firewall‑Regeln oder falsche Adaptereinstellungen.

Effiziente Remotezugriffe über SSH, RDP und Tailscale – ohne öffentliche Portfreigaben.

Strukturierter Aufbau einer Laborumgebung, inklusive Dokumentation, Screenshots und Netzwerkdiagrammen.

Praxisnahe Arbeit mit mehreren Linux‑Distributionen, deren Paketverwaltung, Systemdiensten und Benutzerverwaltung.

Grundlagen sicherer Netzwerkarchitektur, wie Segmentierung, Zugriffskontrolle und sichere Kommunikation zwischen Systemen.

Verbesserte Dokumentations‑ und GitHub‑Skills, um technische Projekte nachvollziehbar und professionell aufzubereiten.

👤 Autor
Mario Horvat


## ⚖️ Hinweis

Dieses Projekt wurde vollständig von mir erstellt.  
Die Inhalte, Texte, Screenshots und Diagramme dürfen ohne meine ausdrückliche Zustimmung nicht kopiert oder weiterverwendet werden.

