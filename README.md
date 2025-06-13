|![Node.js](https://img.shields.io/badge/Node.js-18%2B-green)|![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow)|![HTML](https://img.shields.io/badge/HTML5-UI-blue)|![CSS](https://img.shields.io/badge/CSS3-Neon%20Style-purple)|![Shell](https://img.shields.io/badge/Shell-Bash%20%26%20Batch-lightgrey)|![Puppeteer](https://img.shields.io/badge/Puppeteer-Automation-brightgreen)|
|---|---|---|---|---|---|

#### **SpeedScanX** ist ein lokal ausführbares Diagnosetool mit Weboberfläche zur Analyse von Heim- und Büronetzwerken.  

<br>

> Es bietet
- ✅ Ping
- ✅ Speedtest (CLI)
- ✅ Portscanner
- ✅ Netzwerkscan
- ✅ DHCP-Leases und automatisierten Zugriff auf Router-Logdaten
      
<br>

> Optimiert
- ✅ Speedport Smart 4
- ✅ universell einsetzbar

| Die Anwendung läuft lokal | Speichert keine Daten extern | Liefert strukturierte Ergebnisse mit einer modernen Benutzeroberfläche |
|---|---|---|

<br>

---

<br>

> 📁 Projektstruktur

```yarn
SpeedScanX/
├── backend/                         # Backend-Funktionen
│   ├── ping.js                      # Ping mit Latenzanalyse
│   ├── speedtest.js                 # CLI-Speedtest via Ookla
│   ├── scanner.js                   # Ping-Sweep + ARP-Tabelle
│   ├── ports.js                     # Portscan (TCP)
│   ├── dhcp.js                      # DHCP-Analyse via arp -a
│   └── logs.js                      # Router-Logs via Puppeteer
│
├── public/                          # Web-GUI (Frontend)
│   ├── index.html                   # Benutzeroberfläche
│   ├── script.js                    # Diagnosefunktionen (Fetch + Anzeige)
│   └── style.css                    # Neon-UI mit Animation
│
├── utils/                           # Hilfsfunktionen
│   └── secureEnv.js                 # AES-Entschlüsselung (optional)
│
├── app.js                           # API-Router & Express-Server
├── config.json                      # Zentrale Konfiguration (Netz, Sprache, Optionen)
├── .env                             # Router-Passwort (lokal)
├── .env.secure                      # Optional: verschlüsselte .env-Variante
├── .gitignore                       # Ausschluss sensibler Daten
├── install.bat                      # Windows Start-/Install-Skript
├── install.sh                       # Linux/macOS Start-/Install-Skript
├── README.md                        # Diese Dokumentation
```

<br>

---

<br>

## 🔍 Funktionen

| 🧩 Funktion           | Beschreibung                                                                 |
|------------------------|------------------------------------------------------------------------------|
| 📡 **Ping-Test**         | Strukturierte Antwortzeiten (min, max, avg) mit Paketstatistik               |
| 📶 **Speedtest (CLI)**   | Download-/Upload-Geschwindigkeit und Ping via Ookla Speedtest CLI           |
| 🖧 **Netzwerkscan**      | Aktive Geräte im lokalen Netz durch Ping-Sweep + ARP-Auswertung              |
| 📄 **DHCP-Leases**       | IPs und MAC-Adressen über lokale ARP-Tabelle (Windows)                      |
| 🔌 **Portscanner**       | Scan definierter TCP-Ports auf eine Ziel-IP                                 |
| 📘 **Router-Logs**       | Login in Speedport Webinterface + automatisches Auslesen von Ereignislogs   |
| 🌐 **Web-GUI**           | Lokale HTML/JS-Oberfläche mit Neon-Design, ausklappbaren Rohdaten           |
| 🔐 **.env-Unterstützung**| Sicheres Laden sensibler Daten (z. B. Router-PIN) aus `.env`                |
| 🛠️ **Konfigurierbar**     | zentrale `config.json` für Zielnetz, Portlisten, Sprache etc.              |

<br>

---

<br>

## 🛠️ Installation

| Schritt                        | Befehl / Aktion                                                   |
|--------------------------------|-------------------------------------------------------------------|
| 📥 Projekt entpacken           | Entpacke ZIP oder clone das Repository                            |
| 🔧 Speedtest CLI installieren  | [Download hier](https://www.speedtest.net/apps/cli) → z. B. `C:\Tools\speedtest.exe` |
| 🖊️ `.env` bearbeiten            | Trage dein Router-Passwort ein → `ROUTER_PASSWORD=deinpasswort`   |
| 📦 Abhängigkeiten installieren | `npm install`                                                    |
| 🚀 Starten                     | `node app.js` oder `install.bat`                                 |
| 🌐 Webinterface aufrufen       | `http://localhost:3000`                                          |
