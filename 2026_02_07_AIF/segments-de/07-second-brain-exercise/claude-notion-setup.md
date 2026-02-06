# Claude mit Notion verbinden

Einmalige Einrichtung. Danach kann Claude direkt in dein Notion lesen und schreiben.

---

## Voraussetzungen

| Anforderung | Details |
|-------------|---------|
| **Claude Pro** | Die kostenlose Version hat keine Integrationen. Prüfe unter claude.ai/settings |
| **Notion-Konto** | Kostenlose Version reicht |
| **Desktop-Browser** | Chrome, Edge, Safari oder Firefox (kein Mobile) |

---

## Schritt 1: Notion-Integration in Claude aktivieren

1. Öffne [claude.ai](https://claude.ai) und melde dich an
2. Klicke auf dein **Profilsymbol** (unten links)
3. Wähle **Einstellungen**
4. Navigiere zu **Integrationen** oder **Verbundene Apps**
5. Finde **Notion** und klicke auf **Verbinden**

---

## Schritt 2: Claude in Notion autorisieren

Nach dem Klick auf Verbinden öffnet sich die Notion-Autorisierungsseite:

1. **Melde dich bei Notion an**, falls nötig
2. Überprüfe die Berechtigungen (Lesen, Einfügen, Aktualisieren)
3. **Wähle die zu teilenden Seiten:**
   - Klicke auf **«Seiten auswählen»** (nicht «Zugriff auf alle Seiten»)
   - Wähle eine dedizierte Seite für dein Second Brain
   - NICHT: sensible HR-, Finanz- oder vertrauliche Seiten
4. Klicke auf **Zugriff erlauben**

---

## Schritt 3: Verbindung prüfen

Zurück in Claude:

1. Gehe zu **Einstellungen > Integrationen**
2. Notion sollte **«Verbunden»** anzeigen (grüner Indikator)

---

## Schritt 4: Testen

Starte eine neue Claude-Konversation und versuch:

```
Durchsuche mein Notion nach Seiten über [Thema, das du kennst]
```

Falls Claude nichts findet:
- Prüfe, ob die Seite in deiner Freigabe ist
- Versuch einen spezifischeren Seitennamen

Dann teste Schreibzugriff:

```
Erstelle eine neue Seite in meinem Notion mit dem Namen «Claude Testnotiz» mit dem Inhalt:
«Dies ist eine Testnotiz, erstellt von Claude.»
```

Prüfe in Notion, ob die Seite erscheint.

---

## Fehlerbehebung

| Problem | Lösung |
|---------|--------|
| «Claude kann nicht auf Notion zugreifen» | Einstellungen > Integrationen > Notion > Zugriff verwalten > Seite hinzufügen |
| Seite erstellt, aber nicht sichtbar | Prüfe den «Privat»-Bereich in Notion, oder suche nach dem exakten Titel |
| Claude kann lesen, aber nicht schreiben | Verbindung erneut autorisieren; Berechtigung «Inhalte einfügen» prüfen |
| Integration erscheint nicht | Bestätige Claude Pro (nicht kostenlose Version). Ausloggen und wieder einloggen. |

---

## Sicherheit

- Claude greift nur auf explizit freigegebene Seiten zu
- Du kannst den Zugriff jederzeit widerrufen: Einstellungen > Integrationen > Notion > Trennen
- Notions Workspace-Berechtigungen gelten weiterhin

---

*Setup abgeschlossen. Weiter zu [auto-push-project.md](./auto-push-project.md).*
