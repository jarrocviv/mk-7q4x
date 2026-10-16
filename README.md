# Moeraki-Kemu

Das Taktikspiel am Strand der Kugelfelsen – als App für Handy und PC.
Zu zweit online, zu zweit an einem Gerät oder allein gegen einen starken Computergegner.

Moeraki-Kemu ist ein Brettspiel von **Stefan Kiehl** (Kiehly, www.kiehly.de), grafische Gestaltung von Florian Buchner.
Diese App ist eine private, nicht offizielle Umsetzung für den eigenen Spielkreis.

---

## Inhalt

- [Was die App kann](#was-die-app-kann)
- [Installation](#installation)
- [Online mit Freunden spielen](#online-mit-freunden-spielen)
- [Ton und Benachrichtigungen](#ton-und-benachrichtigungen)
- [Updates einspielen](#updates-einspielen)
- [Dateien in diesem Repository](#dateien-in-diesem-repository)
- [Datenschutz](#datenschutz)
- [Hinweise und Rechte](#hinweise-und-rechte)

---

## Was die App kann

**Spielmodi**
- **Online gegen einen Freund** – jeder auf seinem eigenen Handy, auch zeitversetzt
- **Zu zweit auf einem Gerät** – das Handy wird weitergereicht
- **Gegen den Computer** – in vier Stärken: Lehrling, Krieger, Häuptling und der gnadenlose Meister, der immer wieder andere Varianten spielt
- **Taktik-Rätsel** – 206 Stellungen, in denen sich der Sieg durch eine Kette von Drohungen erzwingen lässt (Gewinn in 2 bis 12 Zügen), mit Rätsel des Tages
- **Übungsmodus** gegen den Meister – warnt vor Gefahren („Vorsicht, Spielende in 3 Zügen möglich“), zeigt auf Wunsch den besten Zug und erlaubt das Zurücknehmen von Zügen

**Regeln nach der Originalanleitung (3. Auflage)**
- Einsteigerspiel, Basisspiel und Meisterspiel mit dem Maori-Tane
- Vorzeitige Siege durch Tahuna, Awa (Variante A und B) und Ara
- Wertung über Marae mit ganzen und halben Stammesplättchen
- Zusatzregel Mata (Auge), wahlweise zuschaltbar
- Moeraki-Skala: Match auf 3, 5, 7 oder 10 Siege

**Außerdem**
- Spielbrett im Stil des Holz-Originals mit Skala, Lagerhäusern und Kugelablagen
- Chat unter dem Spielbrett mit Schnellantworten und Anzeige, wenn der andere gerade schreibt
- Nach Spielende stehen auf allen Kugeln die Zugnummern; mit dem Schieber lässt sich die Partie Zug für Zug nachspielen
- **Spielanalyse**: Der Computer markiert Fehler und zeigt, welcher Zug besser gewesen wäre
- Zählleiste von Schwarz wahlweise weiß (wie im Original) oder schwarz
- Eigener Klang, wenn der Freund gezogen hat oder ins Spiel kommt
- Push-Benachrichtigungen aufs Handy, auch wenn die App geschlossen ist
- Originale Spielanleitung zum Durchblättern und eine Kurzfassung der Regeln
- Läuft nach der Installation auch offline (außer dem Online-Spiel)

---

## Installation

Die App ist eine Web-App. Sie wird einmal im Internet bereitgestellt und dann auf dem Handy oder PC installiert.

### 1. Bereitstellen über GitHub Pages (einmalig)

1. Repository öffnen → **Settings** → links **Pages**
2. Bei *Source* **Deploy from a branch** wählen
3. Bei *Branch* **main** und **/ (root)** wählen → **Save**
4. Nach ein bis zwei Minuten erscheint oben der Link, z. B.
   `https://BENUTZERNAME.github.io/REPOSITORY/`

> Mit einem kostenlosen GitHub-Konto muss das Repository dafür **öffentlich** sein.
> Die Seite ist dann für jeden erreichbar, der den Link kennt. Suchmaschinen werden
> durch `robots.txt` und einen Hinweis in der Seite ausgesperrt.

### 2. Auf dem Android-Handy installieren

1. Den Link in **Chrome** öffnen (nicht im Vorschau-Browser von WhatsApp o. Ä.)
2. Menü **⋮** → **App installieren** bzw. **Zum Startbildschirm hinzufügen** → **Installieren**
3. Die App startet danach wie jede andere App im Vollbild

### 3. Am PC installieren

Den Link in Chrome oder Edge öffnen und auf das Installations-Symbol rechts in der Adresszeile klicken.

### Optional: Installationsdatei (APK)

Auf [pwabuilder.com](https://www.pwabuilder.com) den Link aus Schritt 1 eingeben und unter *Package for stores* das Android-Paket erzeugen.
Die enthaltene APK kann auf dem Handy installiert werden (Installation aus unbekannten Quellen erlauben).

---

## Online mit Freunden spielen

**Neu:** Einladung per Link oder QR-Code, eigene Namen, mehrere Partien gleichzeitig („Meine Partien“), „Zug zurücknehmen?“ mit Zustimmung des Gegenübers und Revanche mit Farbtausch. Alle Spielzüge, Chat-Nachrichten und Namen werden **Ende-zu-Ende verschlüsselt** (AES-256-GCM). Der Schlüssel entsteht aus dem 8-stelligen Partie-Code und verlässt nie die Handys – die Nachrichten-Server sehen nur unlesbare Daten.

1. **Online gegen einen Freund** → Spielart, Anzahl der Siege, Farbe und Startspieler wählen → **Partie erstellen**
2. **Einladung teilen** (z. B. per WhatsApp) oder den **QR-Code** scannen lassen – alternativ den 8-stelligen Code weitergeben
3. Der Freund tippt auf den Link bzw. gibt den Code unter **Online gegen einen Freund** ein

Gut zu wissen:
- Ihr müsst **nicht gleichzeitig** online sein. Der letzte Spielstand bleibt erhalten, bis der andere die App wieder öffnet.
- Eine laufende Partie geht im Startmenü über **Online-Partie … fortsetzen** weiter.
- Oben im Spiel steht **online** oder **offline**. Ein grüner Punkt neben dem Namen zeigt, dass der Freund gerade im Spiel ist.
- Wer Weiß spielt, sieht das Brett gedreht, damit die eigene Seite unten liegt.

Die Züge werden über zwei öffentliche Nachrichten-Server übertragen (EMQX und HiveMQ, parallel genutzt).
Ein eigener Server ist nicht nötig.

---

## Ton und Benachrichtigungen

Einstellungen über **🔔** oben im Spiel oder **⚙️ Einstellungen** im Startmenü.

| Funktion | Wann sie wirkt |
|---|---|
| **Moeraki-Ruf** | App ist geöffnet – erklingt, wenn der Freund gezogen hat |
| **Freund kommt ins Spiel** | eigener Begrüßungston, wenn der Freund die Partie öffnet |
| **Vibration** | zusammen mit den Tönen |
| **Benachrichtigung im Hintergrund** | App ist offen, aber nicht im Vordergrund |
| **Push über ntfy** | auch bei geschlossener App und gesperrtem Handy |

Die Töne richten sich nach der **Medienlautstärke** des Handys. Nach dem Öffnen der App einmal hineintippen,
erst dann erlaubt Android das Abspielen.

### Push über ntfy einrichten

1. Die kostenlose App **ntfy** aus dem Play Store installieren
2. In Moeraki-Kemu unter 🔔 **Push, auch wenn die App geschlossen ist** einschalten
3. Das angezeigte Thema (z. B. `moeraki-abc123…`) in ntfy über **+** abonnieren
4. In ntfy für dieses Thema einen eigenen Ton wählen
5. Mit **Test-Benachrichtigung schicken** prüfen

Tipp: In den Android-Einstellungen für ntfy den Akku-Modus auf **Nicht eingeschränkt** stellen.
Jeder Spieler richtet das auf seinem eigenen Handy ein.

---

## Updates einspielen

1. Im Repository **+** → **Upload files**
2. Die geänderten Dateien hineinziehen (gleichnamige Dateien werden ersetzt) → **Commit changes**
3. Etwa 10 Minuten warten, dann die App auf dem Handy zweimal schließen und öffnen
4. Unten im Startmenü steht die **App-Version** – daran sieht man, ob das Update angekommen ist

---

## Dateien in diesem Repository

| Datei | Zweck |
|---|---|
| `index.html` | die komplette App (Spiel, Regeln, Anleitung, Online-Spiel) |
| `sw.js` | macht die App offline-fähig und lädt Updates |
| `manifest.webmanifest` | Name, Farben und Symbole für die Installation |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | App-Symbole |
| `robots.txt` | hält Suchmaschinen fern |
| `README.md` | diese Beschreibung |
| `CHANGELOG.md` | Änderungsprotokoll aller Versionen |

---

## Datenschutz

- Es gibt **keine Anmeldung** und es werden **keine Namen** gespeichert.
- Spielstände, Chat-Nachrichten, Namen und der Anwesenheits-Status laufen **Ende-zu-Ende verschlüsselt** über öffentliche Nachrichten-Server.
  Wer den Partie-Code bzw. Einladungslink kennt, kann mitlesen – gebt ihn deshalb nur an eure Mitspieler weiter.
- Push-Nachrichten über ntfy enthalten nur kurze Hinweise wie „hat gezogen“, nie Chat-Inhalte.
- Push-Nachrichten laufen über ntfy.sh. Der zufällige Thema-Name wirkt wie ein Passwort und sollte nicht weitergegeben werden.
- Alles andere bleibt auf dem eigenen Gerät gespeichert.

---

## Hinweise und Rechte

- **Moeraki-Kemu** – Spielidee und Regeln © Stefan Kiehl, Kiehly. Grafik der Originalausgabe: Florian Buchner.
- Die eingebaute Spielanleitung stammt aus dem Original und ist nur für Besitzer des Spiels gedacht.
- Diese App ist nicht offiziell und nicht zur öffentlichen Verbreitung bestimmt.
  Vor einer Weitergabe über den privaten Kreis hinaus bitte den Autor fragen: **info@kiehly.de**
- Das Original aus Holz, Stein und Ton gibt es unter **www.kiehly.de**.
