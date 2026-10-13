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
- **Gegen den Meister** – ein Computergegner, der mehrere Züge vorausrechnet und keinen Fehler verzeiht

**Regeln nach der Originalanleitung (3. Auflage)**
- Einsteigerspiel, Basisspiel und Meisterspiel mit dem Maori-Tane
- Vorzeitige Siege durch Tahuna, Awa (Variante A und B) und Ara
- Wertung über Marae mit ganzen und halben Stammesplättchen
- Zusatzregel Mata (Auge), wahlweise zuschaltbar
- Moeraki-Skala: Match auf 3, 5, 7 oder 10 Siege

**Außerdem**
- Spielbrett im Stil des Holz-Originals mit Skala, Lagerhäusern und Kugelablagen
- Chat unter dem Spielbrett mit Schnellantworten
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

1. **Online gegen einen Freund** → Spielart, Anzahl der Siege, Farbe und Startspieler wählen → **Partie erstellen**
2. Den angezeigten **5-stelligen Code** an den Freund schicken
3. Der Freund wählt **Online gegen einen Freund**, gibt den Code ein und tippt auf **Beitreten**

Gut zu wissen:
- Ihr müsst **nicht gleichzeitig** online sein. Der letzte Spielstand bleibt erhalten, bis der andere die App wieder öffnet.
- Eine laufende Partie geht im Startmenü über **Online-Partie … fortsetzen** weiter.
- Oben im Spiel steht **online** oder **offline**. Ein grüner Punkt neben dem Namen zeigt, dass der Freund gerade im Spiel ist.
- Wer Weiß spielt, sieht das Brett gedreht, damit die eigene Seite unten liegt.

Die Züge werden über zwei öffentliche Nachrichten-Server übertragen (EMQX und HiveMQ, parallel genutzt).
Ein eigener Server ist nicht nötig.

---

## Ton und Benachrichtigungen

Einstellungen über **🔔** oben im Spiel oder im Startmenü.

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

---

## Datenschutz

- Es gibt **keine Anmeldung** und es werden **keine Namen** gespeichert.
- Spielstände, Chat-Nachrichten und der Anwesenheits-Status laufen unverschlüsselt über öffentliche Nachrichten-Server.
  Sie enthalten nur Brettstellungen, kurze Chat-Texte und eine zufällige Geräte-Kennung.
  Vertrauliches gehört deshalb nicht in den Chat.
- Push-Nachrichten laufen über ntfy.sh. Der zufällige Thema-Name wirkt wie ein Passwort und sollte nicht weitergegeben werden.
- Alles andere bleibt auf dem eigenen Gerät gespeichert.

---

## Hinweise und Rechte

- **Moeraki-Kemu** – Spielidee und Regeln © Stefan Kiehl, Kiehly. Grafik der Originalausgabe: Florian Buchner.
- Die eingebaute Spielanleitung stammt aus dem Original und ist nur für Besitzer des Spiels gedacht.
- Diese App ist nicht offiziell und nicht zur öffentlichen Verbreitung bestimmt.
  Vor einer Weitergabe über den privaten Kreis hinaus bitte den Autor fragen: **info@kiehly.de**
- Das Original aus Holz, Stein und Ton gibt es unter **www.kiehly.de**.
