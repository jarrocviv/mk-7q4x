# Moeraki-Kemu – eigenständige App

## Was ohne Internet geht
- Zu zweit auf einem Handy
- Gegen den Meister (Bot)
- Spielanleitung und Kurzregeln

Für das Online-Spiel braucht ihr Internet. Die Züge laufen über zwei kostenlose öffentliche
Nachrichten-Server (EMQX und HiveMQ, gleichzeitig – fällt einer aus, übernimmt der andere).
Ein eigener Server ist nicht nötig. Ihr müsst nicht gleichzeitig online sein: Der letzte
Spielstand bleibt beim Server liegen, bis der andere die App wieder öffnet.
Hinweis: Die Spielstände sind dort nicht verschlüsselt – sie enthalten aber nur Brettstellungen,
keine Namen oder persönlichen Daten.

## 1. Online stellen (einmalig, kostenlos)
Damit die App auf dem Handy installierbar ist, muss der Ordner unter einer https-Adresse liegen.

**GitHub Pages**
1. Kostenloses Konto auf github.com anlegen.
2. Neues öffentliches Repository erstellen, z. B. `moeraki-kemu`.
3. Alle Dateien aus diesem Ordner hochladen („Add file“ → „Upload files“).
4. Settings → Pages → Branch `main`, Ordner `/ (root)` → Save.
5. Nach ein bis zwei Minuten ist die App unter `https://DEINNAME.github.io/moeraki-kemu/` erreichbar.

Alternativ geht jeder andere Webspace mit https, z. B. Netlify oder der eigene Homepage-Speicher.

## 2. Auf dem Android-Handy installieren
1. Die Adresse in Chrome öffnen.
2. Menü (⋮) → „App installieren“ bzw. „Zum Startbildschirm hinzufügen“.
3. Die App startet danach wie jede andere App, im Vollbild und auch offline.

Am PC: Adresse in Chrome oder Edge öffnen und über das Install-Symbol in der Adresszeile installieren.

## 3. Optional: echte Installationsdatei (APK)
1. pwabuilder.com öffnen und die Adresse aus Schritt 1 eingeben.
2. „Package for stores“ → Android wählen und das Paket herunterladen.
3. Die enthaltene APK auf das Handy kopieren und installieren (dazu „Installation aus unbekannten Quellen“ erlauben).

## 4. Mit dem Freund spielen
1. Beide installieren die App über dieselbe Adresse.
2. Du: „Online gegen einen Freund“ → Einstellungen wählen → „Partie erstellen“. Es erscheint ein 5-stelliger Code.
3. Freund: „Online gegen einen Freund“ → Code eingeben → „Beitreten“.
4. Später einfach die App öffnen und „Online-Partie … fortsetzen“ tippen.

## Hinweis
Moeraki-Kemu ist ein Spiel von Stefan Kiehl (Kiehly). Die eingebaute Spielanleitung stammt aus dem Original.
Die App ist für den privaten Gebrauch gedacht – vor einer Weitergabe bitte den Autor fragen (info@kiehly.de).

## 5. Ton und Benachrichtigungen (🔔 oben im Spiel)
- **Moeraki-Ruf:** eigener Klang, sobald der Freund gezogen hat (App geöffnet).
- **Benachrichtigung im Hintergrund:** solange die App offen, aber nicht im Vordergrund ist.
- **Push, auch wenn die App geschlossen ist:** über die kostenlose App „ntfy“ (Play Store).
  Im 🔔-Menü einschalten, das angezeigte Thema in ntfy abonnieren, dort einen Ton wählen.
  Jeder Spieler macht das auf seinem eigenen Handy.
