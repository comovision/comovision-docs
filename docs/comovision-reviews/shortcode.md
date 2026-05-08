# Shortcode

## Verwendung

```
[comovision_reviews]
```

Den Shortcode einfach in den Inhalt einer Seite, eines Beitrags oder eines Widgets einfügen. Der Shortcode hat keine Parameter – alle Einstellungen werden im Backend unter **Einstellungen → CV Reviews** vorgenommen.

## Was wird angezeigt

Das Karussell zeigt alle im [Review Manager](review-manager.md) freigegebenen Bewertungen. Je nach Konfiguration enthält jede Karte:

- Profilbild (lokal gecacht) oder Initial des Autors
- Name und Datum
- Sternebewertung
- Bewertungstext (ggf. gekürzt)
- Google-Logo

Im [Header](konfiguration.md#subtab-header) optional:

- Überschrift
- Gesamtbewertung mit Sternen und Anzahl der Google-Bewertungen
- CTA-Button „Neue Bewertung schreiben"

## Layout-Modi

Das Karussell unterstützt drei Darstellungsarten, die du unter **Anpassen → Layout** auswählst:

=== "Karussell"

    Slides wechseln automatisch oder per Klick. Eine Bewertung ist gleichzeitig sichtbar.

    - Navigation per Pfeil-Button, Maus-Klick auf Punkte, Swipe (Touch) oder Pfeiltasten
    - Pausiert automatisch bei Hover und Fokusverlust
    - Loop-Typ wählbar: Endlos, Zurückspulen oder Stopp am Ende

=== "Liste"

    Alle freigegebenen Bewertungen nebeneinander im Raster. Spaltenanzahl je nach Gerät konfigurierbar.

    - Anfangs werden nur so viele Bewertungen angezeigt, wie unter *Anzahl Bewertungen* eingestellt
    - Optionaler „Mehr laden"-Button lädt weitere nach

=== "Masonry"

    Wie Liste, aber Karten dürfen unterschiedliche Höhen haben (Pinterest-Stil). Gut für Bewertungen mit sehr unterschiedlich langen Texten.

## Barrierefreiheit

- Karussell ist per Tastatur bedienbar (← / →)
- ARIA-Labels auf allen interaktiven Elementen
- Bilder mit `alt`-Attribut
- `aria-hidden` auf inaktiven Slides

## Voraussetzungen

!!! warning "Lizenzschlüssel und API-Key"
    Ohne aktiven Lizenzschlüssel wird das Karussell nicht ausgegeben. Admins sehen stattdessen eine Fehlermeldung, Besucher sehen nichts.

    Ohne gültigen API-Key oder Place ID werden keine Bewertungen abgerufen.

## Mehrfach auf einer Seite

Der Shortcode kann mehrfach auf derselben Seite eingesetzt werden. Jede Instanz bekommt eine eindeutige ID und läuft unabhängig. Das Stylesheet und die Design-Einstellungen werden nur einmal geladen.
