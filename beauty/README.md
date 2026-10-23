# Vorlage „Salon-Beispiel" (Editorial · Salon)

> Editorial. Empirisch. Eigenwillig.

Magazin-würdiger Salon-Auftritt mit Split-Hero, Service-Cards und Lookbook-Galerie. Split-Hero im Vogue-Stil. Lookbook-Galerie als Story, Press-Strip mit Magazinen, Service-Cards im Editorial-Format mit Großbildern.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/beauty

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/beauty/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `run_command` mit curl an ihren `path` laden (z. B. `curl -fsSL <url> -o <path>`, Ordner vorher anlegen).
2. Kopiere die Bilder nach `public/images/beauty/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Vogue-artiges Editorial in Rosé: schwarzer Grund, Akzent Altrosa (#d4a4a4) für Linien, Eyebrows und Preise; leichte Cormorant-Garamond-Serifen, Manrope-Text, Monospace für Look-Nummern. Hero geteilt: links Bild (7 Spalten, mit Parallax), rechts Text auf Schwarz. Kapitel-Eyebrows „Kapitel I · Disziplinen", „Kapitel II · Lookbook", „Kapitel III · Termin". Press-Strip mit Magazin-Namen (VOGUE Deutschland, Harper's Bazaar, ELLE, InStyle, Glamour) als Text-Logos.

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #d4a4a4 (weich: rgba(212,164,164,0.18)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Cormorant Garamond (300, 400, 500, 600, 700, italic 300/400) – Hero-Headline dreizeilig (font-light), Sektionstitel teils italic („Unzählige Looks."), Zitat.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Service-Beschreibungen; Look-Nummern und kleine Labels in Monospace (ui-monospace).
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Split-Hero** (100vh): links `hero-editorial-portrait.jpg` über 7 Spalten (Bild 120 % hoch, leichter Parallax beim Scrollen, Verlauf nach rechts ins Schwarz), rechts auf Schwarz: Rosé-Linie + Eyebrow „Salon-Beispiel · Hair · Skin · Studio", dreizeilige Serifen-Headline „Editorial. / Empirisch. / Eigenwillig." (mittlere Zeile kursiv in Rosé), Einleitungstext, Button „Termin buchen" (gefüllt, rosé) und Textlink „Leistungen ansehen". Darunter der Press-Strip mit fünf Magazin-Namen in Serife, gedimmt.
2. **Services** (`Kapitel I · Disziplinen`, Anker `#leistungen`, Headline „Vier Studios. Eine Handschrift."): vier Editorial-Cards mit Großbild (3/4) `service-color-editorial.jpg`, `service-cut-and-form.jpg`, `service-studio-make-up.jpg`, `service-skin-atelier.jpg`, darunter Titel in Serife und Beschreibung mit Ab-Preis. Einleitungsabsatz „Wir mischen jede Farbe selbst …".
3. **Lookbook** (`Kapitel II · Lookbook`, Headline kursiv „Unzählige Looks."): sechs Bilder `look-01.jpg` bis `look-06.jpg` im Masonry- oder 3-Spalten-Raster (Hochformat), Nummer „Look 01" … in Monospace oben links, leichter Zoom beim Hover. Begleittext „Eine Auswahl aus dem Atelier …".
4. **Zitat**: Press-Testimonial in großer Serife mit Quelle „— Editor, VOGUE Deutschland".
5. **Booking** (`Kapitel III · Termin`, Anker `#buchen`, Headline „Schenken Sie sich" + kursiv „Nachmittag."): Button „Termin buchen" in Rosé, dazu Öffnungszeiten und Adresse als Platzhalter; optional Terminformular (Leistung, Datum, Name, E-Mail).

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `karte-salon.jpg` | Editoriales Beauty- und Salonmotiv | card | Vorschaukarte auf der Landingpage; großes Format des Service-Bilds „Cut & Form", geeignet als Open-Graph-Bild |
| `hero-editorial-portrait.jpg` | Editorial portrait | hero | Split-Hero, linke Hälfte (7 Spalten) mit Parallax; zugleich das Teaser-Bild der Landingpage |
| `service-color-editorial.jpg` | Color Editorial · Balayage und Lowlights | service | Service-Card 1 „Color Editorial" |
| `service-cut-and-form.jpg` | Cut & Form · Schnitt und Pflege | service | Service-Card 2 „Cut & Form" |
| `service-studio-make-up.jpg` | Studio Make-up · Editorial und Bridal | service | Service-Card 3 „Studio Make-up" |
| `service-skin-atelier.jpg` | Skin Atelier · Microneedling und Peelings | service | Service-Card 4 „Skin Atelier" |
| `look-01.jpg` | Look 01 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 1 |
| `look-02.jpg` | Look 02 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 2 |
| `look-03.jpg` | Look 03 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 3 |
| `look-04.jpg` | Look 04 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 4 |
| `look-05.jpg` | Look 05 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 5 |
| `look-06.jpg` | Look 06 aus dem Lookbook | lookbook | Lookbook-Galerie, Bild 6 |

## Kennzahlen

- 2017 Studio seit
- 6 Looks
- 3 Servicewelten

## Highlights

- Split-Hero
- Lookbook-Galerie
- Press-Strip

