# Hennwack Post-Generator

Ein kleines Werkzeug im Browser, mit dem die Buchgenossenschaft Hennwack Veranstaltungsposts für Instagram baut. Texte und Bild eingeben, Vorlage und Farben wählen, feinjustieren, als PNG speichern.

Alles steckt in einer einzigen Datei: `index.html`. Es gibt keinen Server, keine Anmeldung und keine Datenbank. Bilder und Texte bleiben im Browser des jeweiligen Geräts.

## Benutzen

- **Online:** über GitHub Pages (siehe unten) einfach den Link öffnen, am Handy wie am Rechner.
- **Lokal:** `index.html` herunterladen und im Browser öffnen.

Die Schriften kommen von Google Fonts. Ohne Internet nimmt der Browser Ersatzschriften.

## Was das Tool kann

- **Vier Vorlagen:** Klassisch (Bild oben, Infos im Farbblock), Buchcover (Cover mit Schatten auf Farbe), Vollbild (Foto randlos mit Farbetikett), Plakat (nur Schrift).
- **Drei Formate:** Feed 4:5 (1080 × 1350), Quadrat 1:1 (1080 × 1080), Story 9:16 (1080 × 1920). Im Story-Format bleiben Texte aus dem Bereich, den Instagram mit Profilname und Antwortfeld überdeckt.
- **Zehn feste Farbkombis** aus den Logofarben. Beim Hochladen eines Bildes wählt das Tool die Kombi, die zu den kräftigsten Farben im Bild passt, und markiert die drei besten.
- **Wiedererkennung:** Farbleiste aus den acht Logofarben, gleiche Trennlinien, Logo immer unten rechts.
- **Feinschliff:** Schriftarten, Titelstärke, Größen, Zeilenabstand, Rand, Abstände, Bildhöhe, Ausrichtung, Logo-Variante und -Größe.
- **Passt automatisch:** Wird der Text zu lang, verkleinert das Tool die Schrift und sagt unter der Vorschau, um wie viel.
- **Caption kopieren:** fasst Titel, Datum, Beschreibung und Fußzeile als Text für die Bildunterschrift zusammen.

## Speichern

- Am Rechner lädt „Als PNG speichern“ die Datei direkt herunter.
- Am Handy öffnet sich das Teilen-Menü, dort „Bild sichern“ wählen.
- Klappt beides nicht, zeigt das Tool das fertige Bild an: gedrückt halten bzw. Rechtsklick → speichern.

## Auf GitHub Pages veröffentlichen

1. Im Repository auf **Settings → Pages** gehen.
2. Unter „Build and deployment“ **Deploy from a branch** wählen, Branch `main`, Ordner `/ (root)`.
3. Nach ein bis zwei Minuten steht das Tool unter `https://fassbuller.github.io/post-generator/` bereit.

## Logos

Die beiden Hennwack-Logos (bunt und schwarz-weiß) stecken als Daten-URLs in `index.html`. Das Tool startet ohne Beispielbild; im Bildbereich steht dann „Bild hinzufügen“.
