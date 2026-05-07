# Konfiguration

Die Einstellungen findest du unter **Einstellungen → CV Reviews → Tab: Einstellungen**.

## Google Places API

### API-Key besorgen

1. Öffne die [Google Cloud Console](https://console.cloud.google.com)
2. Erstelle ein Projekt oder wähle ein bestehendes aus
3. Aktiviere die **Places API** unter *APIs & Dienste → Bibliothek*
4. Erstelle unter *APIs & Dienste → Anmeldedaten* einen neuen **API-Key**
5. Stelle die Einschränkungen auf **Keine** (der Key wird serverseitig verwendet, nicht im Browser)

!!! info "Warum keine HTTP-Referrer-Einschränkung?"
    Das Plugin ruft die Google API serverseitig auf – dabei wird kein HTTP-Referrer-Header mitgeschickt. Referrer-Einschränkungen würden deshalb alle Anfragen blockieren. Stattdessen kann der Key auf **IP-Adressen** eingeschränkt werden.

### Place ID finden

Die Place ID identifiziert deinen Google-Unternehmenseintrag eindeutig.

1. Öffne den [Place ID Finder](https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder)
2. Suche nach deinem Unternehmen
3. Kopiere die angezeigte Place ID (beginnt meist mit `ChIJ…`)

## Einstellungen im Überblick

| Einstellung | Beschreibung |
|---|---|
| **API-Key** | Google Places API-Schlüssel |
| **Place ID** | ID des Google-Unternehmenseintrags |
| **Anzahl Bewertungen** | Wie viele Bewertungen im Karussell angezeigt werden (max. 5 bei normaler Abfrage) |
| **Mindestbewertung** | Nur Bewertungen ab dieser Sternezahl anzeigen (1–5) |
| **Cache-Dauer** | Wie lange Bewertungen zwischengespeichert werden (in Stunden) |
| **Archiv-Modus** | Bewertungen dauerhaft akkumulieren (empfohlen) |
| **Lizenzschlüssel** | Aktivierungsschlüssel für das Plugin |

## Archiv-Modus

Google gibt pro API-Abfrage maximal 5 Bewertungen zurück – und nicht immer dieselben. Mit aktiviertem **Archiv-Modus** speichert das Plugin alle jemals abgerufenen Bewertungen dauerhaft und reichert das Archiv bei jeder Abfrage an.

!!! tip "Empfehlung"
    Den Archiv-Modus von Beginn an aktivieren, damit nach einiger Zeit ein vollständiger Pool an Bewertungen zur Verfügung steht.
