# Studio-Vorlagen

Sechs Branchen-Vorlagen der KI-Website-Landingpage (https://anticipater.com/solutions/cms-ai/ki-webseite-erstellen-lassen), aufbereitet für den DevShot-Studio-Agenten: pro Vorlage ein Manifest, eine Bauanleitung und die echten Bilder.

| Vorlage | Manifest |
| --- | --- |
| Gastronomie-Beispiel (Editorial · Restaurant) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/gastronomie/manifest.json |
| Handwerks-Beispiel (Industrial · Manufaktur) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/handwerk/manifest.json |
| Praxis-Beispiel (Clinical · Privatpraxis) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/medizin/manifest.json |
| Kanzlei-Beispiel (Classic · Kanzlei) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/anwalt/manifest.json |
| Immobilien-Beispiel (Architectural · Premium) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/immobilien/manifest.json |
| Salon-Beispiel (Editorial · Salon) | https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/beauty/manifest.json |

Übersicht: https://raw.githubusercontent.com/anticipaterdotcom/studio-templates/main/index.json

## Aufbau je Vorlage

- `manifest.json`: Name, Typ, Pitch, Tagline, Beschreibung, Sektionen, Highlights, Kennzahlen, Akzentfarben, Schriften (Familien und Gewichte), die Texte des Beispiels (`copy`), `images[]` (Dateiname, Alt-Text, Rolle, Platz) und `files[]` (jede Datei mit Raw-URL und Zielpfad im Workspace unter `.devshot/templates/<slug>/`).
- `README.md`: deutsche Bauanleitung für den Agenten (Sektionen in Reihenfolge, Stil, welche Bilder wohin).
- `*.jpg`: die Bilder der Vorlage.

Die Bilder sind lizenzfreie Motive (Unsplash), wie sie auch die Live-Demos nutzen. Der Agent lädt die Dateien per `run_command` mit curl in den Workspace und baut die Website in Next.js nach.
