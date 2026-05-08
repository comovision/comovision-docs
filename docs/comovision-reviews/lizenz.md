# Lizenz & Updates

## Lizenzschlüssel eintragen

1. Navigiere zu **Einstellungen → CV Reviews → Einstellungen**
2. Trage den Lizenzschlüssel im Feld **Lizenzschlüssel** ein
3. Klicke auf **Speichern**

Das Plugin verbindet sich beim Speichern automatisch mit dem Lizenzserver und aktiviert die Domain. Eine Internetverbindung ist dafür erforderlich.

## Lizenzstatus

| Status | Bedeutung |
|---|---|
| ✅ Aktiv | Lizenz ist gültig, Domain ist freigeschaltet |
| Kein Lizenzschlüssel | Es wurde noch kein Schlüssel eingetragen |
| Ungültig | Schlüssel existiert nicht oder wurde widerrufen |
| Abgelaufen | Lizenz ist abgelaufen (Verlängerung erforderlich) |

Der aktuelle Status wird direkt neben dem Lizenzschlüssel-Feld angezeigt.

!!! info "Grace Period"
    Nach Ablauf der Lizenz gibt es eine Kulanzzeit von 14 Tagen, in der das Plugin weiterhin funktioniert.

## Mehrere Installationen

Ein Lizenzschlüssel kann auf einer bestimmten Anzahl von Domains aktiviert werden (abhängig von deiner Lizenz). Staging- und Entwicklungsumgebungen zählen ebenfalls als Installationen.

!!! warning "Lokale Entwicklungsumgebungen"
    Domains wie `localhost`, `*.local` oder `*.test` werden vom Lizenzserver in der Regel nicht als vollwertige Installationen gezählt. Prüfe dies im Zweifelsfall mit dem Support.

## Plugin-Updates

Sobald eine neue Version verfügbar ist, erscheint die Meldung direkt im WordPress-Backend unter **Dashboard → Updates** – wie bei jedem anderen Plugin aus dem offiziellen Verzeichnis.

**Voraussetzung:** Der Lizenzschlüssel muss aktiv sein. Nur Installationen mit gültiger Lizenz erhalten Updates.

Updates werden über einen signierten, zeitlich begrenzten Download-Link übertragen, der vom Lizenzserver ausgestellt wird.
