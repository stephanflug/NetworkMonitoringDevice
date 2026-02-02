
<h1 align="center">NetworkMonitoringDevice</h1>

<p align="center">
  Ein übersichtliches Tool zur Überwachung von IP-Geräten im Netzwerk – per Ping oder TCP-Port-Check, mit Protokollierung und Export als Nachweis.
</p>

---

## Überblick

**NetworkMonitoringDevice** überwacht Geräte im Netzwerk und zeigt dir in einer klaren Oberfläche, ob ein Gerät **erreichbar (UP)** oder **nicht erreichbar (DOWN)** ist.  
Bei Ausfällen werden Geräte **farblich hervorgehoben**, alle Prüfungen werden **geloggt** und du kannst für jedes Gerät einen **Export als Beweis** erstellen.

---

## Funktionen

### Monitoring
- **Ping-Überwachung** (Erreichbarkeit)
- **TCP-Port-Überwachung** (z. B. 80/443/3389 usw.)
- **Viele Geräte gleichzeitig** (parallele Checks)
- **Intervall & Timeout** pro Gerät einstellbar

### Darstellung
- **GUI-Übersicht** mit Status (UP/DOWN/Unbekannt)
- **Farbmarkierung** bei Ausfall
- **Detailansicht** mit Verlaufsgrafik

### Protokolle & Nachweis
- **Automatische Logdateien** im Ordner `logs/`
- **Export pro Gerät**:
  - **SVG-Grafik** (druckbar, ideal für Dokumentation)
  - **CSV-Rohdaten** (Messwerte / Verlauf)
  - **TXT-Ausfallbericht** (Start, Ende, Dauer)


### Autostart (optional)
- **Optional aktivierbar** über Menü (mit Ja/Nein/Abbrechen-Abfrage)
- Startet auf Wunsch automatisch nach Windows-Neustart

---

## Installation

### Windows (Setup)
1. Setup-Datei herunterladen (aus den Releases oder vom Anbieter).
2. Setup ausführen und installieren.
3. Programm starten.

> Hinweis: Bei vorhandener Firewall/Policy kann Ping oder TCP-Connect eingeschränkt sein. In dem Fall die Regeln im Netzwerk/Endpoint prüfen.

---

## Schnellstart

1. Programm starten  
2. **Neu** → Gerät anlegen  
3. Werte eintragen:
   - **Name**
   - **Host/IP**
   - **Methode**
     - `PING` (Erreichbarkeit)
     - `TCP` (Portprüfung)
   - (bei TCP) **Port**
   - **Intervall (s)** und **Timeout (s)**
4. **Speichern**  
5. Gerät wird automatisch überwacht und in der Liste angezeigt

---

## Statusanzeige

| Status | Bedeutung |
|-------:|-----------|
| UP | Gerät erreichbar / Port erreichbar |
| DOWN | Gerät nicht erreichbar / Port nicht erreichbar |
| Unbekannt | noch keine Messung vorhanden |

Geräte mit **DOWN** werden in der Übersicht **auffällig markiert**, damit Ausfälle sofort sichtbar sind.

---

## Export (Nachweis bei Ausfällen)

Für jedes Gerät kann ein Export erstellt werden (z. B. zur Dokumentation oder als Beweis):

- **SVG**: Verlaufsgrafik (druckbar)  
- **CSV**: Rohdaten (Zeitstempel, Status, Latenz)  
- **TXT**: Ausfallbericht (Ausfall-Zeitfenster + Dauer)

**So geht’s:**
- Gerät auswählen → **„Verlauf exportieren…“**  
- Zielpfad wählen → Export wird als **SVG** gespeichert, zusätzlich werden **CSV** und **TXT** mit gleichem Namen erzeugt.

Die Dateien findest du anschließend im gewählten Ordner (oder im Standardordner `exports/`).

---

## Autostart (optional)

Im Menü **Optionen → Autostart bei Windows-Anmeldung…** wirst du gefragt:

- **Ja** → Autostart aktivieren  
- **Nein** → Autostart deaktivieren  
- **Abbrechen** → keine Änderung

Damit entscheidest du bewusst, ob das Monitoring nach einem Neustart automatisch laufen soll.




---

## Typische Einsatzbereiche

- Überwachung von **Servern**, **NAS**, **Routern/Switches**, **Druckern**
- Prüfung von **Diensten** über TCP-Port (Webserver, RDP, Kameras, VPN)
- Dokumentation von **Störungen** inklusive Export als Nachweis

---

## Hinweise

- Ein **TCP-DOWN** bedeutet: Der Port ist nicht erreichbar (Dienst down, Firewall blockt, Ziel nicht erreichbar, …).
- Bei Ping kann eine Firewall ICMP blockieren – dann besser **TCP** nutzen (passender Port).

---
### Unterstütze das Büro-Kaffeekonto!

Damit der Kaffee im Büro nie ausgeht, wäre eine kleine Spende super! 💰☕  
Jeder Beitrag hilft, die Kaffeemaschine am Laufen zu halten, damit wir alle produktiv bleiben können!

[**Spende für Kaffee**](https://www.paypal.com/donate/?business=ACU26RPTCA44S&no_recurring=0&item_name=Dieses+Projekt+und+der+Service+kann+nur+durch+eure+Spenden+finanziert+werden.&currency_code=EUR)

Vielen Dank für deine Unterstützung! 🙌
