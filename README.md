# BEYONDER · 68 KI-Use-Cases · Landingpage

Eine interaktive Landingpage, die 68 erprobte KI-Use-Cases nach **Funktion** und **Branche** filterbar präsentiert. Besucher können per 4-Schritt-Quiz personalisierte Empfehlungen erhalten, alle Cases durchsuchen und filtern, und im Austausch gegen ihre Kontaktdaten die komplette Excel-Liste herunterladen.

🌐 **Live-Demo:** _Wird nach Aktivierung von GitHub Pages hier verlinkt_

## Inhalt

| Datei | Zweck |
|---|---|
| `index.html` | Komplette Landingpage (alles inline, eine Datei) |
| `BEYONDER-68-KI-Use-Cases.xlsx` | Lead-Magnet — Auto-Download nach Submit, direkt in Google Sheets importierbar |

## Features

- **Hero-Sektion** mit klarem Value Proposition
- **4-Schritt-Quiz**: Funktion → Branche → Nutzen → personalisierte Empfehlungen
- **Filter-Grid** mit Volltextsuche, Funktions-, Branchen- und Nutzen-Filtern
- **HubSpot-Integration**: Lead-Formular (E-Mail + Firmenname) → direkter Submit an HubSpot Forms API
- **Auto-Download** der Excel-Datei nach erfolgreichem Submit
- **Responsive Design** für Desktop & Mobile

## Setup

### 1. Lokal testen
Doppelklick auf `index.html` öffnet die Seite im Browser. Formular-Submits funktionieren nur unter `http(s)://` — lokal landet der Lead nicht in HubSpot.

### 2. HubSpot anbinden
In `index.html` ganz unten im Script-Block die zwei Konstanten ausfüllen:

```js
const HUBSPOT_PORTAL_ID = "12345678";
const HUBSPOT_FORM_ID   = "a1b2c3d4-e5f6-7890-abcd-ef1234567890";
```

Werte findet man in HubSpot → Marketing → Formulare → Aktionen → Embed-Code.
Das HubSpot-Formular muss mindestens die Felder `email` und `company` enthalten.

### 3. Hosten via GitHub Pages (gratis)

1. Im Repo: **Settings** → **Pages**
2. Source: **Deploy from a branch** → Branch: `main` → Folder: `/ (root)`
3. Save klicken
4. Nach 1–2 Min ist die Seite unter `https://beyonder-ag.github.io/<repo-name>/` erreichbar

### 4. Andere Hosting-Optionen
- **Netlify Drop** (https://app.netlify.com/drop): beide Dateien reinziehen → URL erhalten
- **Vercel**: Repo verbinden → Auto-Deploy
- **Eigener Webspace**: beide Dateien per FTP ins gleiche Verzeichnis

## Use Cases anpassen

Die 68 Cases sind als JSON direkt in `index.html` eingebettet (Suche im Code nach `id="caseData"`). Bei Änderungen entweder direkt im JSON editieren oder aus einer aktualisierten Excel neu generieren.

## Tech-Stack

- Reines HTML/CSS/JavaScript — keine Build-Tools, keine Dependencies
- HubSpot Forms Submissions API v3
- Funktioniert ohne Cookies, ohne Tracking-Scripts

## Lizenz

MIT — siehe [LICENSE](LICENSE)

---

© BEYONDER AG
