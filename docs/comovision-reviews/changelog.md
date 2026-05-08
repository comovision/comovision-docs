# Changelog

## 1.1.0

**Design-System & Backend-Überarbeitung**

- **Neu:** Tab „Anpassen" mit vollständigem Design-System: Layout-Typ (Karussell, Liste, Masonry), Spalten, Karussell-Optionen, Header, Typographie, Farben, Abstände und Beitragsstil
- **Neu:** Layout-Typen Liste und Masonry mit konfigurierbaren Spalten je Gerät
- **Neu:** „Mehr laden"-Button für Liste und Masonry
- **Neu:** Header-Bereich mit konfigurierbarer Überschrift, Bewertungsanzeige und CTA-Button
- **Neu:** Vollständig anpassbarer Beitragsstil (Schatten, Eckenradius, Rahmen, Hintergrundfarbe)
- **Verbessert:** Modernes Admin-Styling konsistent über alle drei Tabs
- **Verbessert:** Nach dem Speichern bleibt man im gleichen Tab und Unterelement
- **Fix:** CSS-Design-Variablen wurden nicht im `<head>` ausgegeben, sodass alle Farb- und Typographie-Einstellungen wirkungslos blieben – behoben durch frühzeitiges Einreihen via `wp_enqueue_scripts`
- **Fix:** DSGVO: `local_avatar()` gibt nie mehr eine externe Google-URL zurück
- **Fix:** Vollständiger CSRF-Schutz und MIME-Type-Fix für sichere Dateiauslieferung

---

## 1.0.0 – 2025-05-07

Erstveröffentlichung.

**Features:**

- Google Reviews Karussell via Places API
- Review Manager mit Blacklist/Whitelist, Sortierung und Keyword-Filter
- Archiv-Modus zum Akkumulieren von Bewertungen
- Lokales Avatar-Caching (DSGVO-konform, keine externen Anfragen im Frontend)
- Lizenzvalidierung über eigenen Lizenzserver
- Automatische Plugin-Updates über Lizenzserver
