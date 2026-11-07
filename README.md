# Hennwack Post-Generator

Ein kleines Werkzeug im Browser, mit dem die Buchgenossenschaft Hennwack Instagram-Posts, Plakate und Flyer für Veranstaltungen baut. Medium wählen, Texte und Bild eingeben, Aufbau und Farben wählen, feinjustieren, als PNG oder PDF speichern.

Alles steckt in einer einzigen Datei: `index.html`. Es gibt keinen Server, keine Anmeldung und keine Datenbank. Bilder und Texte bleiben im Browser des jeweiligen Geräts.

## Benutzen

- **Online:** über GitHub Pages (siehe unten) einfach den Link öffnen, am Handy wie am Rechner.
- **Lokal:** `index.html` herunterladen und im Browser öffnen.

Die Schriften kommen von Google Fonts. Ohne Internet nimmt der Browser Ersatzschriften.

## Zwei Schritte: erst das Medium, dann der Aufbau

**Medium** – wofür ist es?

| Medium | Größen | Datei |
|---|---|---|
| Instagram | Feed 4:5 (1080 × 1350), Quadrat (1080 × 1080), Story (1080 × 1920) | PNG |
| Plakat | A4 (300 dpi), A3 (250 dpi) | PDF oder PNG |
| Flyer | A5 – 2 pro A4-Blatt, A6 – 4 pro A4-Blatt | PDF-Bogen zum Schneiden oder einzelner Flyer als PNG |

Jedes Medium bringt passende Voreinstellungen mit: Instagram ohne QR-Code, Plakat und Flyer mit QR-Code unten links, 5 mm weißem Druckrand und PDF. Was man danach ändert, merkt sich das Medium. Im Story-Format bleiben Texte aus dem Bereich, den Instagram mit Profilname und Antwortfeld überdeckt.

**Aufbau** – welches Material hast du?

| Aufbau | passt, wenn du … hast |
|---|---|
| Bild + Text | ein Bild und viel zu erzählen |
| Buchcover | ein Buch (Cover freigestellt mit Schatten) |
| Foto | ein starkes Foto (randlos, Text auf einem Etikett) |
| Nur Schrift | kein Bild |

Jeder Aufbau funktioniert in jedem Medium. Plakate und Flyer haben alle das DIN-Seitenverhältnis 1 : √2, deshalb sieht derselbe Entwurf auf A3, A4, A5 und A6 gleich aus – nur die Schrift wird mit dem Papier kleiner.

## Was das Tool sonst kann

- **QR-Code:** Link zur Anmeldung eintragen, der Code erscheint sofort im Bild – unten links (gegenüber dem Logo), neben dem Logo, oben links oder oben rechts, mit Beschriftung und Größenregler. Sitzt der Code unten, wird das Logo genauso hoch; die Größe stellt man dann für beide beim QR-Code ein. Ohne `https://` wird es automatisch ergänzt. Der Code wird direkt im Browser erzeugt, kein fremder Dienst bekommt den Link zu sehen. Die Farben wählt das Tool so, dass jede Handykamera den Code liest (dunkle Felder auf hellem Grund).
- **Zehn feste Farbkombis** aus den Logofarben. Beim Hochladen eines Bildes wählt das Tool die Kombi, die zu den kräftigsten Farben im Bild passt, und markiert die drei besten.
- **Wiedererkennung:** Farbleiste aus den acht Logofarben, gleiche Trennlinien, Logo immer unten rechts.
- **Feinschliff:** Schriftarten, Titelstärke, Größen, Zeilenabstand, Rand, Abstände, Bildhöhe, Ausrichtung, Logo-Variante und -Größe.
- **Passt automatisch:** Wird der Text zu lang, verkleinert das Tool die Schrift und sagt unter der Vorschau, um wie viel.
- **Auswahl statt Tippen:** Für die Dachzeile (Buchvorstellung, Lesung, Konzert, DIY-Abend …) und die Fußzeile (Eintritt frei, Spenden willkommen …) gibt es Chips zum Antippen. Eigene Einträge lassen sich hinzufügen, Standardeinträge ausblenden.
- **Caption kopieren:** fasst Titel, Datum, Beschreibung, Fußzeile und Anmeldelink als Text für die Bildunterschrift zusammen.

## Listen für alle ändern

Eigene Kategorien und Bausteine speichert jedes Gerät für sich. Sollen sie für alle gelten, gehören sie in die Standardlisten: In `index.html` nach `const PRESETS` suchen und die Einträge bei `dach` (Dachzeile) oder `fuss` (Fußzeile) ergänzen.

## Speichern

- Am Rechner lädt „Als PNG speichern“ bzw. „Als PDF speichern“ die Datei direkt herunter.
- Am Handy öffnet sich das Teilen-Menü, dort „Bild sichern“ wählen.
- Klappt beides nicht, zeigt das Tool das fertige Bild an: gedrückt halten bzw. Rechtsklick → speichern.

## Drucken

- Im Druckdialog **„Tatsächliche Größe“ bzw. 100 %** wählen, nicht „An Seite anpassen“ – sonst wird der Rand doppelt.
- **Flyer:** Das PDF ist ein A4-Bogen mit 2 (A5) bzw. 4 (A6) Flyern. Entlang der gestrichelten Linien schneiden, dann hat jeder Flyer rundum 5 mm weißen Rand. Ohne Druckrand (Copyshop) fehlen die Linien, dort wird nach Maß geschnitten.
- **A3** druckt kaum ein Heimdrucker – das PDF im Copyshop abgeben.
- Faustregel für den QR-Code: Er sollte etwa ein Zehntel des Abstands breit sein, aus dem Leute ihn scannen. Das Tool zeigt die gedruckte Breite unter dem Link-Feld an.
- Vor dem Aushängen einmal mit dem Handy scannen.

## Auf GitHub Pages veröffentlichen

1. Im Repository auf **Settings → Pages** gehen.
2. Unter „Build and deployment“ **Deploy from a branch** wählen, Branch `main`, Ordner `/ (root)`.
3. Nach ein bis zwei Minuten steht das Tool unter `https://fassbuller.github.io/post-generator/` bereit.

## Logos

Die beiden Hennwack-Logos (bunt und schwarz-weiß) stecken als Daten-URLs in `index.html`. Das Tool startet ohne Beispielbild; im Bildbereich steht dann „Bild hinzufügen“.
