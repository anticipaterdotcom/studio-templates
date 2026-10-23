# Vorlage „Handwerks-Beispiel" (Industrial · Manufaktur)

> Material. Maß. Meisterschaft.

Digitale Visitenkarte für Schreinereien, Metallbauer und Manufakturen mit Werkstatt-Mosaik. Industrial-Premium. Fette Display-Typo, Werkstatt-Galerie wie ein Foto-Essay, transparenter Prozess vom Entwurf bis zur Montage.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/handwerk

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/handwerk/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `run_command` mit curl an ihren `path` laden (z. B. `curl -fsSL <url> -o <path>`, Ordner vorher anlegen).
2. Kopiere die Bilder nach `public/images/handwerk/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Industrial-Premium: schwarzer Grund, kupferfarbene Akzente (#b87333) für Linien, Nummern und Eyebrows, fette Manrope-Versalien als Headlines, Werkstattfotos mit hartem Kino-Look und Verlauf von links. Ein laufender Material-Ticker („Eiche · Nussbaum · Esche · Kirsche", „Edelstahl · Messing · Bronze", „CNC · Handarbeit · 1908 – heute", „Karlsruhe · Baden · Schwarzwald"). Sektionen mit Eyebrows „Werk · 01" bis „Werk · 03".

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #b87333 (weich: rgba(184,115,51,0.18)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Hero-Headline dreizeilig, uppercase, font-extrabold/black, sehr eng (tracking -0.04em); Sektionstitel uppercase extrabold; große Zahlen.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Labels, Eyebrows (uppercase, 11px, letter-spacing 0.32em).
- Akzentschrift: Playfair Display (400, 500, 600, 700, 800, italic 400) – Kursive Akzentwörter und das Kundenzitat.
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Industrial Hero** (`hero-schreinerei.jpg`, 100vh, Verlauf von links): kupferfarbene Linie + Eyebrow „Handwerks-Beispiel · Anno 1908", dreizeilige Versal-Headline „MATERIAL. / MASS. / MEISTER." (mittlere Zeile in Kupfer), Einleitungstext, Buttons „Leistungen" (gefüllt) und „Werkstatt besichtigen" (unterstrichener Textlink). Rechts eine Kennzahlen-Karte: „117 Jahre Handwerk", „4 Generationen" mit gepunkteten Trennlinien.
2. **Material-Ticker**: schmale Laufzeile mit den vier Ticker-Texten, uppercase, gedimmt, endlos von rechts nach links.
3. **Disziplinen-Grid** (`Werk · 01`, Headline „Vier Disziplinen."): vier Karten (2×2 oder 4 Spalten) mit Code „01"–„04" in Kupfer, Name fett uppercase, Blurb; jede zweite Karte leicht versetzt. Darüber der Absatz „Jedes Stück, das die Werkstatt verlässt …".
4. **Werkstatt-Mosaik** (`Werk · 02`, Headline „In der Werkstatt.", Anker `#galerie`): 12er-Raster mit `mosaik-hobelbank.jpg` (5 Spalten, 4/5), `mosaik-massivholz-eiche.jpg` (7 Spalten, 4/3), `mosaik-spaene-detail.jpg` (7 Spalten, 4/3), `mosaik-politur.jpg` (5 Spalten, 4/5). Label unten links in Kupfer, leichter Zoom beim Hover.
5. **Prozess** (`Werk · 03`, Headline „Der Weg vom Wort zum Werk."): vier Schritte I–IV als Karten mit Kupfer-Rahmen (Beratung, Entwurf, Werkstatt, Montage). Danach ein Garantie-Block mit Siegel-Icon und 25-Jahre-Hinweis.
6. **Kundenzitat**: großes kursives Zitat (Playfair Display) der Familie Reinhardt mit Quelle in Kupfer.
7. **Abschluss-CTA** (Eyebrow „Auftrag", Headline „Schreiben Sie uns"): Button „Werkstatt anrufen" in Kupfer, dazu Telefon und Adresse als Platzhalter.

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `karte-werkstatt.jpg` | Werkstatt mit Holz und Werkzeugen | card | Vorschaukarte auf der Landingpage; gleiches Motiv wie der Hero in anderer Kompression |
| `hero-schreinerei.jpg` | Schreinerei | hero | Industrial Hero, vollflächig, Verlauf von links (Text links lesbar) |
| `teaser-massivholz.jpg` | Massivholz-Werkstück aus Eiche | teaser | Teaser der Landingpage; großes Format des Mosaik-Bilds „Massivholz · Eiche", geeignet als Open-Graph-Bild |
| `mosaik-hobelbank.jpg` | Hobelbank | gallery | Werkstatt-Mosaik, Kachel 1 (Spalte 5, 4/5), Label „Hobelbank" |
| `mosaik-massivholz-eiche.jpg` | Massivholz · Eiche | gallery | Werkstatt-Mosaik, Kachel 2 (Spalte 7, 4/3), Label „Massivholz · Eiche" |
| `mosaik-spaene-detail.jpg` | Späne · Detail | gallery | Werkstatt-Mosaik, Kachel 3 (Spalte 7, 4/3), Label „Späne · Detail" |
| `mosaik-politur.jpg` | Politur | gallery | Werkstatt-Mosaik, Kachel 4 (Spalte 5, 4/5), Label „Politur" |

## Kennzahlen

- 117 Jahre Handwerk
- 4 Prozessschritte
- 25 Jahre Garantie

## Highlights

- Werkstatt-Mosaik
- Prozess in 4 Schritten
- 25 Jahre Garantie-Stempel

