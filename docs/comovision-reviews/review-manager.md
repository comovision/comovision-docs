# Review Manager

Der Review Manager ist unter **Einstellungen → CV Reviews → Bewertungen verwalten** erreichbar.

## Übersicht

Alle bisher abgerufenen Bewertungen werden als Liste dargestellt. Pro Zeile siehst du:

- **Drag-Handle** – zum Umsortieren per Drag & Drop
- **Toggle** – Bewertung ein- oder ausblenden
- **Avatar** – Profilbild oder Initial des Autors
- **Meta** – Name, Sterne, Datum und Status-Badges
- **Vorschau** – die ersten 120 Zeichen des Bewertungstexts

Klicke nach Änderungen auf **Speichern**. Der Cache wird dabei automatisch geleert, sodass die Änderungen sofort im Frontend sichtbar sind.

---

## Modus

| Modus | Verhalten |
|---|---|
| **Blacklist** | Alle Bewertungen sind sichtbar – außer den explizit ausgeblendeten |
| **Whitelist** | Keine Bewertung ist sichtbar – außer den explizit aktivierten |

Den Modus wählst du über die Karten-Auswahl oben im Formular.

---

## Neue Bewertungen

Legt fest, wie neue Bewertungen (die zum ersten Mal im Archiv auftauchen) behandelt werden. Diese Option ist nur im **Whitelist**-Modus relevant.

| Option | Verhalten |
|---|---|
| **Automatisch anzeigen** | Neue Bewertungen erscheinen direkt im Karussell |
| **Manuell freischalten** | Neue Bewertungen sind zunächst ausgeblendet und müssen einzeln aktiviert werden |

---

## Keyword-Filter

Bewertungen können automatisch ein- oder ausgeblendet werden, wenn ihr Text bestimmte Begriffe enthält. Mehrere Keywords mit Komma trennen, Groß-/Kleinschreibung wird ignoriert.

| Filter | Verhalten |
|---|---|
| **Ausblenden** | Bewertungen, die eines dieser Keywords enthalten, werden immer ausgeblendet |
| **Immer anzeigen** | Bewertungen mit diesen Keywords werden angezeigt – auch wenn sie durch den Ausblenden-Filter erfasst würden |

!!! info "Priorität"
    Der „Immer anzeigen"-Filter hat Vorrang vor dem „Ausblenden"-Filter. Eine Bewertung, die beide Kriterien erfüllt, wird angezeigt.

---

## Bewertungen sortieren

Die Reihenfolge der Bewertungen im Karussell entspricht der Reihenfolge in der Liste. Halte den **⠿**-Handle am linken Rand gedrückt und ziehe die Zeile an die gewünschte Position.

---

## Status-Badges

| Badge | Bedeutung |
|---|---|
| **Neu** | Bewertung wurde neu im Archiv entdeckt (gleiche `first_seen`- und `last_seen`-Zeit) |
| **Geändert** | Der Reviewtext hat sich seit der ersten Erfassung verändert – Tooltip zeigt das Datum der letzten Änderung |
| **Archiviert** | Bewertung ist nicht mehr in der aktuellen Google-Antwort enthalten, wurde aber archiviert |

---

## Archiv-Modus

Ist der [Archiv-Modus](konfiguration.md#archiv-modus) aktiv, zeigt der Review Manager **alle** jemals erfassten Bewertungen – auch solche, die Google aktuell nicht mehr zurückgibt. Archivierte Einträge sind leicht abgeblendet und mit dem Badge **Archiviert** gekennzeichnet.
