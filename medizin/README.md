# Vorlage „Praxis-Beispiel" (Clinical · Privatpraxis)

> Diagnose mit Disziplin.

Ruhige Praxis-Website mit Fachgebieten, Team-Editorial und integriertem Termin-Formular. Klinisch ruhig, mint-akzentuiert. Fachgebiete als Raster, Team-Portraits in Editorial-Qualität, integriertes Termin-Formular ohne Drittanbieter-Zwang.

Vorschau des Originals: https://anticipater.com/solutions/cms-ai/website-erstellen-lassen-karlsruhe/demo/medizin

## So baust du die Website

1. Diese Vorlage liegt im Workspace unter `.devshot/templates/medizin/` (Manifest `manifest.json`, diese Anleitung, alle Bilder). Falls noch nicht geschehen: alle Dateien aus `manifest.files[]` per `download_url` an ihren `path` laden.
2. Kopiere die Bilder nach `public/images/medizin/` und referenziere sie von dort (Next.js `<Image>` mit Breite/Höhe oder `fill`).
3. Baue die Seite als Next.js-App (App Router, TypeScript, Tailwind) mit genau den Sektionen unten in dieser Reihenfolge. Nutze die Texte aus `manifest.copy` als Startinhalt und ersetze Firmenname, Adresse, Preise und Namen durch die Angaben des Nutzers.
4. Mobile zuerst prüfen (Hero-Headline mit `clamp()`, Raster brechen auf eine Spalte), dann Desktop bis 1440px.

## Stil

Klinisch ruhig: schwarzer Grund, mintfarbene Akzente (#a8c8c0) sparsam für Eyebrows, Icons, Linien und Kreise; extraleichte Manrope-Headlines, kursive Playfair-Akzente. Viel Luft, klare Raster, keine Stock-Klischees. Nummerierte Eyebrows „01 · Fachgebiete" bis „04 · Termin". Vertrauensleiste unter dem Hero (Zertifiziert ISO 9001 · 2024, 3 Fachärzte, 12.000+ Patienten, ≤ 7 Tage Wartezeit).

- Grundfarben: Hintergrund #0a0a0b, Flächen #111114, Schrift #f4f4f5, gedimmt #a8a8ad, Linien rgba(255,255,255,0.08).
- Akzentfarbe: #a8c8c0 (weich: rgba(168,200,192,0.16)). Nur für Eyebrows, Linien, Nummern, Akzentwörter und Buttons.
- Display-Schrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Hero-Headline und Sektionstitel in font-extralight (200), groß und ruhig.
- Textschrift: Manrope (200, 300, 400, 500, 600, 700, 800) – Fließtext, Labels, Eyebrows (uppercase, 11px, letter-spacing 0.32em).
- Akzentschrift: Playfair Display (400, 500, 600, 700, 800, italic 400) – Kursive Akzentzeilen („Ein Standard.", „Disziplin").
- Schriften per `next/font/google` laden (Manrope, Cormorant Garamond, Playfair Display sind Google Fonts); die Gewichte oben reichen.
- Eyebrows: text-[11px] tracking-[0.32em] uppercase. Container: max-w-[1440px] px-6 lg:px-10. Sektionsabstand: py-32. Bilder mit `object-cover`, leicht entsättigt, dunkle Verläufe darüber.

## Sektionen in Reihenfolge

1. **Clinical Hero** (`hero-praxis.jpg`, 100vh): kleiner Mint-Kreis mit Punkt + Eyebrow „Praxis-Beispiel · Karlsruhe Westend", zweizeilige extraleichte Headline „Diagnose / mit Disziplin" (zweite Zeile kursiv Playfair, „Disziplin" in Mint), Einleitungstext, Buttons „Termin vereinbaren" (gefüllt, mint) und „Fachgebiete ansehen" (Outline). Darunter eine Vertrauensleiste mit vier Icon-Einträgen (siehe `copy.trust`).
2. **Fachgebiete** (`01 · Fachgebiete`, Anker `#fachgebiete`, Headline „Vier Disziplinen. Ein Standard."): vier Karten im Raster mit Nummer „01"–„04" in Mint + Pfeil-Icon, Titel, Beschreibung; feine Linien, Hover hellt auf. Links daneben der Absatz „Wir behandeln nicht alles …".
3. **Team** (`02 · Das Team`, Headline „Drei Köpfe."): drei Portraits (3/4) `team-faerztliche-leitung.jpg`, `team-aerztliche-leitung.jpg`, `team-diagnostik.jpg` mit dünner Mint-Linie unter dem Bild, Name fett, Rolle in Mint.
4. **Räume** (`03 · Die Räume`, Headline „Ruhe ist Diagnostik."): `raeume-empfang.jpg` groß links (8 Spalten, 16/10), `raeume-behandlungsraum.jpg` hochkant rechts (4 Spalten, 4/5).
5. **Termin** (`04 · Termin`, Anker `#termin`, Headline „Heute anfragen. Diese Woche behandelt."): links Text zu Kostenträgern und Kontaktzeilen, rechts Formular mit Vorname, Nachname, E-Mail, Anliegen (Textarea) und Button „Termin anfragen". Formular ohne Drittanbieter, Felder mit Eyebrow-Labels und Linien statt Boxen.

## Bilder

| Datei | Alt-Text | Rolle | Wohin |
| --- | --- | --- | --- |
| `karte-praxis.jpg` | Moderne Arztpraxis mit heller Behandlungssituation | card | Vorschaukarte auf der Landingpage; großes Format des Behandlungsraum-Bilds |
| `hero-praxis.jpg` | Praxis | hero | Clinical Hero, vollflächig, dunkler Verlauf von oben und unten |
| `teaser-praxis.jpg` | Praxis (Teaser-Größe) | teaser | Dasselbe Motiv wie der Hero in 2000px; Open-Graph-Bild |
| `team-faerztliche-leitung.jpg` | Fachärztliche Leitung · Fachärztin Innere Medizin | team | Team-Sektion, Portrait 1 (3/4) |
| `team-aerztliche-leitung.jpg` | Ärztliche Leitung · Kardiologe und Praxisleitung | team | Team-Sektion, Portrait 2 (3/4) |
| `team-diagnostik.jpg` | Diagnostik-Team · Sport- und Präventionsmedizin | team | Team-Sektion, Portrait 3 (3/4) |
| `raeume-empfang.jpg` | Empfang | gallery | Räume-Sektion, großes Bild links (8 Spalten, 16/10) |
| `raeume-behandlungsraum.jpg` | Behandlungsraum | gallery | Räume-Sektion, Hochformat rechts (4 Spalten, 4/5) |

## Kennzahlen

- 3 Fachärzte
- 1 Patient zur Zeit
- 24 h Antwortfenster

## Highlights

- Fachgebiete-Raster
- Team-Editorial
- Termin-Formular inkl.

