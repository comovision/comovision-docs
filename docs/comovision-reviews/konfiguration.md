# Konfiguration

Das Plugin-Backend erreichst du unter **Einstellungen → CV Reviews**.

---

## Tab: Einstellungen

### Google Places API

#### API-Key besorgen

1. Öffne die [Google Cloud Console](https://console.cloud.google.com)
2. Erstelle ein Projekt oder wähle ein bestehendes aus
3. Aktiviere die **Places API** unter *APIs & Dienste → Bibliothek*
4. Erstelle unter *APIs & Dienste → Anmeldedaten* einen neuen **API-Key**

!!! info "Einschränkungen des API-Keys"
    Das Plugin ruft die Google API **serverseitig** auf – dabei wird kein HTTP-Referrer-Header mitgeschickt. Referrer-Einschränkungen würden deshalb alle Anfragen blockieren. Du kannst den Key stattdessen auf **IP-Adressen** einschränken (empfohlen für Produktivumgebungen).

#### Place ID finden

Die Place ID identifiziert deinen Google-Unternehmenseintrag eindeutig.

1. Öffne den [Place ID Finder](https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder)
2. Suche nach deinem Unternehmen
3. Kopiere die angezeigte Place ID (beginnt meist mit `ChIJ…`)

### Einstellungen im Überblick

| Einstellung | Beschreibung | Standard |
|---|---|---|
| **API-Key** | Google Places API-Schlüssel | – |
| **Place ID** | ID des Google-Unternehmenseintrags | – |
| **Anzahl Bewertungen** | Wie viele Bewertungen angezeigt werden (max. 5 ohne Archiv-Modus, bis 100 mit) | 5 |
| **Mindestbewertung** | Nur Bewertungen ab dieser Sternezahl anzeigen (1–5) | 4 |
| **Cache-Dauer** | Wie lange Bewertungen zwischengespeichert werden (1–168 Stunden) | 12 |
| **Archiv-Modus** | Bewertungen dauerhaft akkumulieren (empfohlen) | aus |
| **Lizenzschlüssel** | Aktivierungsschlüssel für das Plugin | – |

### Archiv-Modus

Google gibt pro API-Abfrage maximal 5 Bewertungen zurück – und nicht immer dieselben. Mit aktiviertem **Archiv-Modus** speichert das Plugin alle jemals abgerufenen Bewertungen dauerhaft in der WordPress-Datenbank und reichert das Archiv bei jeder Cache-Aktualisierung an.

!!! success "Empfehlung"
    Den Archiv-Modus von Beginn an aktivieren. Nach einigen Wochen steht so ein vollständiger Pool aller Bewertungen zur Verfügung – unabhängig davon, welche 5 Google gerade zurückgibt.

### Cache leeren

In der Seitenleiste unter **Einstellungen** findest du den aktuellen Cache-Status (Ablaufzeit der letzten Abfrage). Über **Cache jetzt leeren** werden neue Bewertungen beim nächsten Seitenaufruf sofort von Google abgerufen.

---

## Tab: Anpassen

Der Tab **Anpassen** enthält alle visuellen Einstellungen des Karussells. Änderungen wirken sich sofort beim nächsten Seitenaufruf aus. Die Einstellungen sind in drei Bereiche unterteilt.

### Subtab: Layout

#### Layout-Typ

| Typ | Beschreibung |
|---|---|
| **Karussell** | Slides wechseln automatisch oder per Klick – eine Bewertung sichtbar gleichzeitig |
| **Liste** | Alle freigegebenen Bewertungen nebeneinander im Raster |
| **Masonry** | Bewertungen im Pinterest-Stil – unterschiedliche Höhen erlaubt |

#### Anzahl Bewertungen

Legt fest, wie viele Bewertungen initial angezeigt werden – getrennt nach **Desktop**, **Tablet** und **Mobil**.

Bei Liste und Masonry steuert diese Zahl, wie viele Bewertungen beim ersten Laden sichtbar sind. Weitere Bewertungen können über den [„Mehr laden"-Button](#mehr-laden-button) nachgeladen werden.

#### Spalten

Anzahl der nebeneinander dargestellten Spalten – getrennt nach **Desktop**, **Tablet** und **Mobil**. Gilt nur für Liste und Masonry.

#### Karussell-Optionen

| Option | Beschreibung | Standard |
|---|---|---|
| **Loop-Typ** | Endlos (dreht sich endlos), Zurückspulen (kehrt zum Start zurück), Stopp (hält am Ende an) | Endlos |
| **Intervall** | Seconds between auto-advance (1–60) | 5 |
| **Navigationspfeile** | Pfeil-Buttons links und rechts einblenden | an |
| **Seitennumerierung** | Punkte unterhalb des Karussells | an |
| **Automatische Wiedergabe** | Karussell startet automatisch | an |

#### Inhaltslänge

Maximale Zeichenanzahl für den Bewertungstext. Längere Bewertungen werden mit `…` abgeschnitten. `0` = vollständiger Text.

---

### Subtab: Header

Der Header erscheint oberhalb des Karussells und kann ein- oder ausgeschaltet werden.

| Element | Beschreibung |
|---|---|
| **Header aktivieren** | Header komplett ein-/ausblenden |
| **Überschrift** | Optionaler Titeltext über dem Karussell, mit Schriftgröße, -stärke, Farbe und Abständen |
| **CTA-Button** | Link-Button „Neue Bewertung schreiben" – verweist auf den Google-Unternehmenseintrag |
| **Durchschnittliche Bewertung** | Zeigt die Gesamtnote, Sterne und Anzahl der Bewertungen an |

Die Typographie (Schriftgröße, -stärke, Zeilenhöhe) und Farben der Bewertungsanzeige sind separat konfigurierbar.

---

### Subtab: Einzelne Elemente

Jedes Element des Bewertungs-Slides kann unabhängig konfiguriert werden.

#### Beitragsstil

Steuert das Aussehen der Karten-Hülle jeder einzelnen Bewertung.

| Option | Beschreibung |
|---|---|
| **Stil-Typ** | Box (mit Hintergrund und Rahmenoptionen) oder Normal (transparent, kein Rahmen) |
| **Hintergrundfarbe** | Füllfarbe der Karte |
| **Box-Schatten** | Schatten mit X, Y, Blur, Spread und Farbe einstellbar |
| **Eckenradius** | Abrundung der Ecken in Pixeln |
| **Strichstil** | Rahmen mit Breite und Farbe |
| **Innenabstand** | Padding der Karte (oben, rechts, unten, links) |

#### Autor und Datum

| Option | Beschreibung |
|---|---|
| **Aktivieren** | Kopfzeile (Avatar, Name, Datum, Google-Logo) ein-/ausblenden |
| **Name des Autors** | Name separat ein-/ausblenden |
| **Autorenbild** | Avatar-Bild separat ein-/ausblenden |
| **Datum** | Datum separat ein-/ausblenden |
| **Farben** | Farbe für Name und Datum getrennt einstellbar |
| **Abstände** | Innen- und Außenabstand des Kopfbereichs |

#### Bewertung

Sternebewertung unterhalb des Autorbereichs.

| Option | Beschreibung |
|---|---|
| **Aktivieren** | Sterneleiste ein-/ausblenden |
| **Icon-Farbe** | Farbe der gefüllten Sterne |
| **Abstände** | Innen- und Außenabstand |

#### Bewertungs-Absatz

Der eigentliche Reviewtext.

| Option | Beschreibung |
|---|---|
| **Aktivieren** | Text ein-/ausblenden |
| **Schriftart** | Schriftgröße, -stärke und Zeilenhöhe |
| **Farbe** | Textfarbe |
| **Abstände** | Innen- und Außenabstand |

#### „Mehr laden"-Button {#mehr-laden-button}

Nur relevant bei **Liste** und **Masonry**. Blendet nach dem initialen Ladevorgang einen Button ein, mit dem weitere Bewertungen nachgeladen werden können.

| Option | Beschreibung |
|---|---|
| **Aktivieren** | Button ein-/ausblenden |
| **Text** | Beschriftung des Buttons |
| **Schriftart** | Größe, Stärke, Zeilenhöhe |
| **Text** | Textfarbe im Normalzustand |
| **Text/Hover** | Textfarbe beim Hover |
| **Hintergrund/Hover** | Hintergrundfarbe beim Hover |
| **Abstände** | Innen- und Außenabstand |
