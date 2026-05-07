# ComoVision Reviews

Google Reviews als Karussell direkt in WordPress einbinden – **DSGVO-konform**, ohne externe Dienste, ohne monatliche Gebühren.

## DSGVO-konform by Design

Viele Review-Plugins laden Bewertungen direkt im Browser des Besuchers – dabei entstehen automatisch Verbindungen zu Google-Servern, die ohne Einwilligung nicht erlaubt sind.

ComoVision Reviews funktioniert anders: **Alle Kommunikation mit Google findet ausschließlich serverseitig statt.** Im Frontend werden keinerlei externe Requests ausgelöst.

!!! success "Was das konkret bedeutet"
    - Kein Browser des Besuchers verbindet sich mit Google
    - Profilbilder werden lokal auf deinem Server gespeichert und von dort ausgeliefert
    - Das Google-Logo ist als inline SVG eingebettet – keine externe Datei
    - Kein Consent-Banner für das Karussell erforderlich

## Was das Plugin kann

- **DSGVO-konform** – keine externen Verbindungen im Frontend
- **Google Reviews abrufen** via Places API und als Karussell darstellen
- **Review Manager** – einzelne Bewertungen ein-/ausblenden, sortieren und filtern
- **Archiv-Modus** – Bewertungen akkumulieren (Google gibt pro Abfrage max. 5 zurück)
- **Lokales Avatar-Caching** – Profilbilder werden lokal gespeichert und ausgeliefert
- **Automatische Updates** – neue Versionen erscheinen direkt im WP-Backend

## Voraussetzungen

| | |
|---|---|
| WordPress | 6.0 oder höher |
| PHP | 8.0 oder höher |
| Google Places API Key | mit aktivierter Places API |
| Lizenzschlüssel | erhältlich bei [ComoVision](https://www.comovision.de) |

## Schnellstart

1. [Plugin installieren](installation.md)
2. [API-Key und Place ID eintragen](konfiguration.md)
3. [Lizenzschlüssel aktivieren](lizenz.md)
4. Shortcode `[comovision_reviews]` in eine Seite einfügen
