# Claude mit Notion verbinden: Ihr Second Brain Setup

Eine praktische Anleitung zur Nutzung von Claude Pro/Max mit Notion als integriertem Wissenssystem.

---

## Voraussetzungen

Stellen Sie vor Beginn sicher, dass Sie Folgendes haben:

| Anforderung | Details |
|-------------|---------|
| **Claude Pro oder Max Abonnement** | Die kostenlose Version enthält keine MCP-Integrationen. Überprüfen Sie dies unter claude.ai/settings |
| **Notion-Konto** | Kostenlose, Plus- oder Business-Version funktionieren alle |
| **Desktop-Browser** | Chrome, Edge, Safari oder Firefox (Mobile wird für das Setup nicht unterstützt) |
| **10-15 Minuten** | Einmalige Einrichtung |

---

## Schritt 1: Notion-Integration in Claude aktivieren

1. Öffnen Sie [claude.ai](https://claude.ai) und melden Sie sich an
2. Klicken Sie auf Ihr **Profilsymbol** (unten links)
3. Wählen Sie **Einstellungen**
4. Navigieren Sie zu **Integrationen** oder **Verbundene Apps** in der linken Seitenleiste
5. Finden Sie **Notion** in der Liste der verfügbaren Integrationen
6. Klicken Sie auf **Verbinden**

> **Was Sie sehen werden:** Ein Schalter oder «Verbinden»-Button neben dem Notion-Logo. Der Status zeigt zunächst «Nicht verbunden».

---

## Schritt 2: Claude in Notion autorisieren

Nach dem Klick auf Verbinden öffnet sich die Notion-Autorisierungsseite:

1. **Melden Sie sich bei Notion an**, falls erforderlich
2. Überprüfen Sie die Berechtigungen, die Claude anfordert:
   - Inhalte von Seiten und Datenbanken lesen
   - Inhalte einfügen
   - Inhalte aktualisieren
3. **Wählen Sie die zu teilenden Seiten:**
   - Klicken Sie auf **«Seiten auswählen»** (nicht «Zugriff auf alle Seiten erlauben», es sei denn, dies ist beabsichtigt)
   - Markieren Sie die spezifischen Seiten oder Datenbanken, auf die Claude zugreifen soll
   - Sie können später jederzeit weitere hinzufügen
4. Klicken Sie auf **Zugriff erlauben**

> **Was Sie sehen werden:** Ein Notion-Popup mit Ihrem Workspace-Namen, angeforderten Berechtigungen und einem Seitenauswahl-Baum.

### Empfohlene Erstauswahl

Für ein «Second Brain»-Setup gewähren Sie Zugriff auf:
- Eine dedizierte «AI Notizen»- oder «Claude Workspace»-Seite
- Alle Datenbanken, die Claude abfragen soll (z.B. Meeting-Notizen, Projekte, Leseliste)
- NICHT: sensible HR-, Finanz- oder vertrauliche Seiten

---

## Schritt 3: Verbindung überprüfen

Zurück in Claude:

1. Kehren Sie zu **Einstellungen > Integrationen** zurück
2. Notion sollte jetzt **«Verbunden»** mit einem grünen Indikator anzeigen
3. Hinweis: Möglicherweise sehen Sie die spezifischen Seiten/Datenbanken aufgelistet

> **Was Sie sehen werden:** Status geändert zu «Verbunden» mit Optionen zum «Trennen» oder «Zugriff verwalten».

---

## Schritt 4: Lesezugriff testen

Starten Sie eine neue Claude-Konversation und versuchen Sie:

```
Durchsuche mein Notion nach Seiten über [Thema, das Sie kennen]
```

**Erwartetes Ergebnis:** Claude ruft relevante Inhalte von Ihren verbundenen Seiten ab und fasst sie zusammen.

Falls Claude sagt, dass er nicht auf Notion zugreifen kann oder nichts findet:
- Überprüfen Sie, ob die Seite in Ihrer freigegebenen Auswahl ist
- Prüfen Sie, ob die Seite die Suchbegriffe enthält
- Versuchen Sie einen spezifischeren Seitennamen

---

## Schritt 5: Schreibzugriff testen

Versuchen Sie, eine einfache Testnotiz zu erstellen:

```
Erstelle eine neue Seite in meinem Notion mit dem Namen «Claude Testnotiz» mit dem Inhalt:
«Dies ist eine Testnotiz, erstellt von Claude am [heutiges Datum].»
```

**Erwartetes Ergebnis:** Claude bestätigt die Erstellung und stellt möglicherweise einen Link zur neuen Seite bereit.

**In Notion überprüfen:**
1. Öffnen Sie Notion
2. Prüfen Sie Ihre Seitenleiste oder suchen Sie nach «Claude Testnotiz»
3. Bestätigen Sie, dass der Inhalt korrekt erscheint

---

## Schritt 6: Praktische Anwendungsbeispiele

Nach der Verbindung probieren Sie diese wertvollen Anwendungsfälle:

| Anwendungsfall | Beispiel-Prompt |
|----------------|-----------------|
| **Meeting-Synthese** | «Fasse alle meine Meeting-Notizen der letzten Woche zusammen und identifiziere Aktionspunkte» |
| **Wissensabruf** | «Was sagen meine Notizen über den Projektzeitplan von [Kundenname]?» |
| **Inhaltserstellung** | «Erstelle eine Notion-Seite, die die wichtigsten Punkte aus diesem Dokument zusammenfasst: [Text einfügen]» |
| **Datenbankabfragen** | «Zeige mir alle Aufgaben in meiner Projekte-Datenbank, die als hohe Priorität markiert sind» |
| **Querverweise** | «Finde Verbindungen zwischen meinen Notizen zu AI-Strategie und digitaler Transformation» |

---

## Fehlerbehebung

### «Claude kann nicht auf Notion zugreifen» oder «Ich habe keinen Zugriff darauf»

| Ursache | Lösung |
|---------|--------|
| Seite nicht in freigegebener Auswahl | Einstellungen > Integrationen > Notion > Zugriff verwalten > Seite hinzufügen |
| Verbindung abgelaufen | Integration trennen und neu verbinden |
| Seite in anderem Workspace | Stellen Sie sicher, dass Sie den richtigen Notion-Workspace autorisiert haben |

### «Seite erstellt, aber ich kann sie nicht finden»

- Prüfen Sie Ihren Notion-Bereich «Privat» (neue Seiten landen standardmässig dort)
- Suchen Sie nach dem exakten Seitentitel in Notion
- Geben Sie eine übergeordnete Seite in Ihrem Prompt an: «Erstelle eine Seite unter [Name der übergeordneten Seite]»

### «Claude kann lesen, aber nicht schreiben»

- Autorisieren Sie die Verbindung erneut; stellen Sie sicher, dass die Berechtigung «Inhalte einfügen» erteilt ist
- Einige Notion Enterprise Workspaces beschränken externe App-Schreibvorgänge — prüfen Sie dies mit Ihrer IT-Abteilung

### Integration erscheint nicht in den Claude-Einstellungen

- Bestätigen Sie, dass Sie Claude Pro oder Max haben (nicht die kostenlose Version)
- Versuchen Sie, sich ab- und wieder anzumelden
- Löschen Sie den Browser-Cache und aktualisieren Sie die Seite

### Synchronisierungsverzögerungen

- Notion-Änderungen können 1-2 Minuten benötigen, bis sie in Claude sichtbar sind
- Für Echtzeit-Anforderungen weisen Sie Claude explizit an, die Seite zu «aktualisieren» oder «erneut zu prüfen»

---

## Sicherheitshinweise

- Claude greift nur auf Seiten zu, die Sie explizit freigeben
- Sie können den Zugriff jederzeit widerrufen: Einstellungen > Integrationen > Notion > Trennen
- Die Freigabeeinstellungen von Notion gelten weiterhin — Claude kann Ihre Workspace-Berechtigungen nicht umgehen
- Überprüfen Sie freigegebene Seiten vierteljährlich; entfernen Sie, was Claude nicht mehr zugreifen muss

---

## Nächste Schritte

Sobald Ihre Verbindung funktioniert:

1. **Erstellen Sie eine dedizierte Claude-Workspace-Seite** in Notion für AI-generierte Inhalte
2. **Richten Sie eine «Quick Capture»-Datenbank ein**, in der Claude Erkenntnisse, Ideen oder Zusammenfassungen protokollieren kann
3. **Experimentieren Sie mit Datenbankabfragen**, wenn Sie Notion-Datenbanken für Projekte oder Aufgaben verwenden

---

*Setup abgeschlossen. Ihr Second Brain ist jetzt verbunden.*
