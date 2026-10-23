# Vorlage „Kanzlei-Beispiel" (Classic · Kanzlei)

> Argument. Akte. Autorität.

Souveräner Kanzlei-Auftritt mit Bibliotheksbildwelt, Rechtsgebieten und Partner-Portrait. Bibliothek statt Stockfotos. Klassische Serifen-Typo, römische Nummerierung für Rechtsgebiete, Auswahl-Akten mit BGH/OLG-Stempel.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/anwalt

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/anwalt/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `download_url` an ihren `path` laden.
2. Kopiere die Bilder nach `public/images/anwalt/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Klassisch-souverän: schwarzer Grund mit weinrotem Akzent (#8a2a2f), im Hero ein radialer Schimmer in Weinrot; Playfair-Display-Serifen für alle Headlines, Manrope für Text. Römische Nummerierung (I–VI) und lateinische Eyebrows „Sectio I · Rechtsgebiete", „Sectio II · Auswahl von Verfahren", „Sectio III · Partner". Vertrauensleiste mit Rankings (Best Lawyers · 2024, JUVE · Top 50 Wirtschaftskanzleien, Handelsblatt · Beste Anwälte, Legal 500 · Empfohlen).

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #8a2a2f (weich: rgba(138,42,47,0.22)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Playfair Display (400, 500, 600, 700, 800, italic 400) – Alle Headlines (Hero dreizeilig, Sektionstitel 5xl–6xl), Akzentwörter kursiv in Weinrot.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Labels, Eyebrows (uppercase, 11px, letter-spacing 0.32em).
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Cathedral Hero** (`hero-bibliothek.jpg`, 100vh): weinrote Linie + Eyebrow „Kanzlei-Beispiel · est. 1971", dreizeilige Playfair-Headline „Argument. / Akte. / Autorität." (zweite Zeile kursiv in Weinrot), Einleitungstext, Buttons „Vertrauliche Beratung" (gefüllt, weiß auf Weinrot oder weinrot) und „Rechtsgebiete" (Outline). Darunter die Rankings-Leiste (vier Einträge, uppercase, gedimmt).
2. **Rechtsgebiete** (`Sectio I · Rechtsgebiete`, Anker `#rechtsgebiete`, Headline „Rechtsgebiete. Eine Schreibtischlampe."): sechs Felder I–VI im 2×3- oder 3×2-Raster, römische Ziffer in Weinrot, Titel in Playfair, Beschreibung gedimmt, feine Rahmenlinien. Einleitungsabsatz „Wir konzentrieren uns …" davor.
3. **Akten-Auswahl** (`Sectio II · Auswahl von Verfahren`, Headline „Ausgewählte Akten."): drei Zeilen oder Karten mit Gerichts-Stempel („BGH · 2024", „OLG Karlsruhe · 2023", „LAG · 2023") als Eyebrow in Weinrot, Titel in Serife, Blurb, Pfeil-Icon rechts.
4. **Partner** (`Sectio III · Partner`): `partner-portrait.jpg` hochkant links (5 Spalten, 3/4), rechts Headline „Partner-Portrait" + kursiv „Mandat." in Weinrot, Vita-Text, dezente Signaturlinie.
5. **Kontakt** (Anker `#kontakt`): zentriert Headline „Schreiben Sie uns." + „Wir antworten am gleichen Tag.", Absatz zur vertraulichen Erstberatung, großer E-Mail-Link als Button (Platzhalter-Adresse durch die echte ersetzen).

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `karte-bibliothek.jpg` | Bibliothek einer Kanzlei mit hohen Regalen | card | Vorschaukarte auf der Landingpage; gleiches Motiv wie der Hero in anderer Kompression |
| `hero-bibliothek.jpg` | Bibliothek | hero | Cathedral Hero, vollflächig, Verlauf von links plus weinroter Radialschimmer |
| `teaser-kanzlei.jpg` | Kanzlei-Arbeitsplatz mit Akten | teaser | Teaser der Landingpage; eignet sich als Bild für die Akten-Sektion oder als Open-Graph-Bild |
| `partner-portrait.jpg` | Partner-Portrait | story | Partner-Sektion, Hochformat 3/4 links (5 Spalten) neben dem Text |

## Kennzahlen

- 1971 Kanzlei seit
- 6 Rechtsgebiete
- 2 Partner

## Highlights

- Römisch-numerierte Felder
- Auswahl-Verfahren
- Partner-Portrait

