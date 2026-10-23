# Vorlage „Gastronomie-Beispiel" (Editorial · Restaurant)

> Tafel, Terroir, Theater.

Ein Restaurantauftritt mit Speisekarte als Hauptdarsteller, Reservierungs-CTA und Atmosphäre-Galerie. Editorial-Layout im Stil eines Sterne-Magazins. Speisekarte als Hauptdarsteller, Reservierungsbutton immer in Reichweite, Atmosphäre-Galerie als Sehnsuchts-Trigger.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/gastronomie

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/gastronomie/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `download_url` an ihren `path` laden.
2. Kopiere die Bilder nach `public/images/gastronomie/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Dunkles Editorial wie ein Sterne-Magazin: schwarzer Grund, viel Weißraum, große leichte Serifen (Cormorant Garamond), goldene Akzentfarbe nur für Eyebrows, Linien, Preise und Akzentwörter. Bilder mit Kino-Look (leicht entsättigt, dunkle Verläufe von unten). Sektionen mit nummerierten Eyebrows „N° 01 · Restaurant" bis „N° 04 · Le chef". Reservierungs-Button immer sichtbar (Hero und Abschluss-CTA).

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #c9a45a (weich: rgba(201,164,90,0.18)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Cormorant Garamond (300, 400, 500, 600, 700, italic 300/400) – Hero-Headline (clamp(64px,10vw,168px), font-light, leading 0.9), Sektionstitel, Zahlen; Akzentwörter italic in der Akzentfarbe.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Labels, Eyebrows (uppercase, 11px, letter-spacing 0.32em).
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Cinematic Hero** (`hero-restaurantsaal.jpg`, 100vh): Eyebrow „Restaurant · Karlsruhe · Beispiel" in Gold, zweizeilige Headline in Cormorant Garamond light („Gastronomie" / „Beispiel." mit zweiter Zeile in der Akzentfarbe), Einleitungstext, Info-Block mit Uhr und Adresse, Button „Reservierung anfragen". Darunter ein Award-Strip: ★★ Guide Michelin · 17,5 Gault & Millau · 92 pt Falstaff · 2024 Best of Baden.
2. **Restaurant-Story** (`N° 01 · Restaurant`): Headline „Ein Teller ist eine Behauptung." und zwei Absätze Haltung (Text in `copy.story`). Kein Bild, viel Weißraum, zweispaltig.
3. **Saisonale Karte** (`N° 02 · La carte`): Liste aus vier Gerichten (Gang als goldener Eyebrow, Name groß in Serife, Beschreibung gedimmt, Preis rechts mit €-Zeichen in Gold), Zeilen durch feine Linien getrennt, leichte Einblend-Animation je Zeile, darunter Outline-Button „Komplette Karte herunterladen".
4. **Atmosphäre-Galerie** (`N° 03 · L'atmosphère`, Headline „Drei Räume. Eine Bühne."): 12er-Raster, links `galerie-speisesaal.jpg` (Spalte 7, 4/5), rechts untereinander `galerie-weinkeller.jpg` und `galerie-chefs-table.jpg` (Spalte 5, je 4/3). Jedes Bild mit Caption-Overlay unten links (Eyebrow + Titel).
5. **Chef-Story** (`N° 04 · Le chef`): `chef-kuechenteam.jpg` hochkant links (Spalte 5), rechts Headline „Küchenteam." (zweites Wort kursiv in Gold), Text und Blockzitat mit goldener Linie.
6. **Reservierung** (Abschluss-CTA): Eyebrow „Réservez", Headline „Einen Platz am Pass.", Button „Tisch reservieren" (gefüllt in Gold). Optional kleines Formular (Datum, Personen, Name, E-Mail).

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `karte-restaurant.jpg` | Premium-Restaurant mit gedeckten Tischen | card | Vorschaukarte auf der Landingpage (nicht Teil der Seite); eignet sich als zweites Hero- oder Story-Bild |
| `hero-restaurantsaal.jpg` | Restaurantsaal | hero | Cinematic Hero, vollflächig (100vh), Verlauf von unten nach oben |
| `teaser-restaurantsaal.jpg` | Restaurantsaal (Teaser-Größe) | teaser | Dasselbe Motiv wie der Hero in 2000px; für Open-Graph-Bild oder Übersichtskarte |
| `galerie-speisesaal.jpg` | Speisesaal | gallery | Atmosphäre-Galerie, großes Bild links (4/5), Eyebrow „Salon principal", Titel „42 Plätze" |
| `galerie-weinkeller.jpg` | Weinkeller | gallery | Atmosphäre-Galerie, rechts oben (4/3), Eyebrow „Cave à vins", Titel „1.200 Etiketten" |
| `galerie-chefs-table.jpg` | Chef's Table | gallery | Atmosphäre-Galerie, rechts unten (4/3), Eyebrow „Chef's Table", Titel „8 Plätze" |
| `chef-kuechenteam.jpg` | Küchenteam | story | Chef-Sektion „N° 04 · Le chef", Hochformat 4/5 links neben Text und Zitat |

## Kennzahlen

- 18-23 Uhr Reservierung
- 42 Plätze
- 1.200 Weinetiketten

## Highlights

- Animierte Karten-Sektion
- Reservierungs-Modul
- Chef-Story & Awards

