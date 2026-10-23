# Vorlage „Immobilien-Beispiel" (Architectural · Premium)

> Architektur als Argument.

Premium-Plattform für Makler, Bauträger und Verwaltungen mit Objekt-Switcher und Standort-Bühne. Architektur-Magazin. Interaktiver Objekt-Switcher mit AnimatePresence, Off-Market-Hinweis, kartografische Standort-Visualisierung.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/immobilien

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/immobilien/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `download_url` an ihren `path` laden.
2. Kopiere die Bilder nach `public/images/immobilien/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Architektur-Magazin in Silbergrau: schwarzer Grund, Akzent ist helles Silber (#d6d6d6) statt einer Buntfarbe, dünne weiße Linien, extraleichte Manrope-Headlines mit kursiven Playfair-Einschüben. Bilder mit hartem Kino-Look. Eyebrows „Kollektion · 2025", „Service · 02", „Standorte · 03". Kennzahlen-Leiste unter dem Hero (€ 1,2 Mrd. vermitteltes Volumen, 186 Premium-Transaktionen, 21 Jahre am Markt, 4,9/5 Bewertungsschnitt).

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #d6d6d6 (weich: rgba(214,214,214,0.15)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Hero-Headline (clamp(56px,9vw,148px), leading 0.92) und Sektionstitel in font-extralight.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Labels, Eyebrows (uppercase, 11px, letter-spacing 0.32em).
- Akzentschrift: Playfair Display (400, 500, 600, 700, 800, italic 400) – Kursive Akzentzeilen („Argument", „Ein Standard.", „zwischen Schloss und Rhein.").
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Architectural Hero** (`hero-villa.jpg`, 100vh, Text unten links): Eyebrow „Immobilien-Beispiel · Immobilien · Karlsruhe", Headline „Architektur / als Argument" (zweites Wort kursiv Playfair), Absatz „Wir vermitteln keine Quadratmeter …" neben den Buttons „Aktuelle Objekte" (gefüllt, silber) und „Service-Spektrum" (Outline). Darunter die Kennzahlen-Leiste (vier Werte, siehe `copy.stats`).
2. **Objekte** (`Kollektion · 2025`, Anker `#objekte`, Headline „Vier Adressen. Ein Standard."): interaktiver Objekt-Switcher: links eine Tab-Liste „01 Villa am Hangweg" bis „04 Stadtvilla im Bauhaus-Stil" (aktiver Tab hell, mit Ort), rechts das große Bild (8 Spalten, 16/10) mit Überblendung beim Wechsel (AnimatePresence/Framer Motion oder CSS-Fade) und Datenzeile Preis · Fläche · Lage. Kleiner Off-Market-Hinweis darunter.
3. **Services** (`Service · 02`, Anker `#service`, Headline „Vom Exposé bis zur Übergabe."): drei Spalten Wertgutachten, Off-Market, Notar & Abwicklung mit feinen Linien und Icon.
4. **Standort** (`Standorte · 03`, Headline „Wir kennen jede Straße" + kursiv „zwischen Schloss und Rhein."): `standort-karlsruhe-karte.jpg` im Format 2/1 mit dunkler Überlagerung (40 %) und vier animierten Pins (Punkt in Silber, dünne Linie, Label uppercase) an den Positionen aus `copy.locations.pins`.
5. **Abschluss-CTA**: Einladung zur diskreten Objektanfrage mit E-Mail-/Telefon-Platzhaltern.

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `hero-villa.jpg` | Moderne Villa als Premium-Immobilie | hero | Architectural Hero, vollflächig; zugleich die Vorschaukarte der Landingpage |
| `objekt-01-villa-am-hangweg.jpg` | Villa am Hangweg, Karlsruhe · Durlach | gallery | Objekt-Switcher, Tab 01 |
| `objekt-02-penthouse-schloss-carre.jpg` | Penthouse Schloss-Carré, Karlsruhe · Innenstadt | gallery | Objekt-Switcher, Tab 02 |
| `objekt-03-glaswuerfel-am-waldrand.jpg` | Glaswürfel am Waldrand, Baden-Baden · Lichtental | gallery | Objekt-Switcher, Tab 03; zugleich das Teaser-Bild der Landingpage |
| `objekt-04-stadtvilla-bauhaus.jpg` | Stadtvilla im Bauhaus-Stil, Karlsruhe · Weststadt | gallery | Objekt-Switcher, Tab 04 |
| `standort-karlsruhe-karte.jpg` | Karlsruhe Karte | map | Standort-Sektion, Kartenbild 2/1 mit vier Pins (Durlach, Innenstadt, Weststadt, Baden-Baden), halbtransparent abgedunkelt |

## Kennzahlen

- 3 Objektklassen
- Off Market-Modus
- KA Fokusgebiet

## Highlights

- Interaktive Objekt-Tabs
- Off-Market-Netzwerk
- Standort-Karte

