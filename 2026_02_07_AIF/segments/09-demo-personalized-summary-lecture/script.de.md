# Demo-Skript: Personalisierter Zusammenfassungs-Workflow

**Dauer:** ca. 15 Minuten (inkl. Q&A)
**Begleitdokument:** Siehe `n8n-workflow.md` für technische Referenz

---

## 1. Setup (Was das Publikum sieht)

### Vorbereitung vor der Demo

| Element | Status | Hinweise |
|---------|--------|----------|
| n8n Workflow | Im Browser-Tab geöffnet | Auf Bildschirmgrösse gezoomt |
| Notion Profil-DB | Zweiter Tab | Ein Beispiel-Benutzerprofil sichtbar |
| Beispiel-Transkript | Bereit zum Einfügen | 500-800 Wörter, Meeting-Notizen-Format |
| Notion Output-DB | Dritter Tab | Leer oder mit einer früheren Zusammenfassung |
| E-Mail-Client | Optionaler vierter Tab | Um Zustellung zu zeigen, falls konfiguriert |

### Bildschirm-Layout

```
+------------------------+------------------------+
|                        |                        |
|   n8n Workflow         |   Notion Profil-DB     |
|   (Hauptfokus)         |   (Kontext)            |
|                        |                        |
+------------------------+------------------------+
```

### Einstieg (Erste 30 Sekunden)

> „Jede Führungskraft, die ich kenne, hat das gleiche Problem: Sie verlassen ein Meeting, Ihre Notizen existieren irgendwo, und dann... nichts. Sie verrotten. Dieser Workflow verwandelt rohe Meeting-Inhalte in etwas, das Sie tatsächlich lesen würden – formatiert so, wie *Sie* es wollen, fokussiert auf das, was *Ihnen* wichtig ist. Lassen Sie mich zeigen, wie es funktioniert."

---

## 2. Durchgang (Schritt für Schritt)

### Schritt 1: Das Benutzerprofil zeigen (~2 Min.)

**Zu Notion Profil-Tab wechseln**

> „Bevor die AI irgendetwas anfasst, muss sie wissen, für wen sie arbeitet. Hier ist mein Profil."

Hinweisen auf:
- **Zusammenfassungsstil:** „Aufzählungspunkte, keine Prosa – ich scanne, ich lese nicht"
- **Fokusgebiete:** „Umsatzauswirkungen, nötige Entscheidungen, Blocker"
- **Tonpräferenz:** „Direkt, kein Füllmaterial"
- **Zustellung:** „Notion + E-Mail"

**Der Clou:** „Das ist keine Konfiguration, die im Code vergraben ist. Es ist eine Notion-Datenbank, die Sie jederzeit aktualisieren. Meinung geändert? Feld ändern. Der Workflow passt sich an."

---

### Schritt 2: Den Workflow auslösen (~1 Min.)

**Zu n8n wechseln**

> „Beobachten Sie, was passiert, wenn Inhalt ins System kommt."

- Das Beispiel-Transkript in den Input-Node einfügen (oder Webhook auslösen)
- Auf **Execute Workflow** klicken

**Während der Ausführung:** „Beachten Sie, dass zuerst mein Profil abgerufen wird, bevor irgendetwas anderes passiert. Kontext zuerst, dann Aktion."

---

### Schritt 3: Den Flow durchgehen (~4 Min.)

**Jeden Node durchgehen, während er ausgeführt wird:**

| Node | Das sagen |
|------|-----------|
| **Trigger** | „Das kann manuell, geplant oder von einem anderen System ausgelöst werden – Slack-Bot, E-Mail-Parser, was auch immer." |
| **Input** | „Roher Inhalt rein. Kann ein Transkript sein, ein Dokument, ein E-Mail-Thread. Egal – Text ist Text." |
| **Notion Get** | „Hier ist die Magie: Wir rufen die Präferenzen des Benutzers *zur Laufzeit* ab. Nicht hartcodiert. Nicht statisch." |
| **Merge** | „Transkript trifft auf Präferenzen. Hier passiert die Personalisierung – bevor die AI es überhaupt sieht." |
| **AI Agent** | „Der Prompt wird *konstruiert*, nicht geschrieben. Stil, Fokus, Länge – alles aus Ihrem Profil injiziert." |
| **Notion Create** | „Output geht direkt in Ihr Second Brain. Getaggt, datiert, durchsuchbar." |
| **Email** | „Optionale Benachrichtigung – weil manche von Ihnen in ihrem Posteingang leben." |

---

### Schritt 4: Den Output zeigen (~2 Min.)

**Zu Notion Output-DB wechseln**

> „Hier ist, was gerade angekommen ist."

Zeigen:
- Zusammenfassung entspricht dem gewünschten Stil (Aufzählungspunkte, keine Absätze)
- Fokusgebiete werden hervorgehoben (Umsatz, Entscheidungen, Blocker)
- Ton entspricht der Präferenz
- Metadaten erfasst (Quelle, Datum, verknüpfter Benutzer)

**Falls Zeit:** E-Mail öffnen, um parallele Zustellung zu zeigen.

---

### Schritt 5: Live-Variation (~2 Min.)

> „Ändern wir etwas."

1. Zur Profil-DB wechseln
2. Eine Präferenz ändern (z.B. „Zusammenfassungsstil" → „Executive-Brief-Absatz")
3. Dasselbe Transkript erneut ausführen
4. Unterschiedliches Output-Format zeigen

**Der Punkt:** „Gleicher Inhalt, andere Person, anderer Output. Das ist es, was ‚personalisiert' tatsächlich bedeutet."

---

## 3. Wichtige Punkte zum Betonen

### Warum das wichtig ist

| Punkt | Was sagen |
|-------|-----------|
| **AI allein reicht nicht** | „GPT kann alles zusammenfassen. Aber eine Zusammenfassung, die niemand liest, ist wertlos. Personalisierung ist der Unterschied zwischen ‚funktioniert' und ‚nützlich'." |
| **Trennung der Verantwortlichkeiten** | „Benutzerpräferenzen leben in Notion. Workflow-Logik lebt in n8n. AI macht einen Job. Jedes Teil ist austauschbar." |
| **No-Code bedeutet nicht No-Architecture** | „Das sieht einfach aus, aber es ist designt. Der Merge-Node ist kein Zufall – das ist das Pattern." |
| **Runtime > Build Time** | „Präferenzen sind nicht eingebacken. Sie werden bei jeder Ausführung frisch abgerufen. Sie können 50 verschiedene Personen mit einem Workflow bedienen." |

### Der Business Case

> „Ich habe das an einem Nachmittag gebaut. Es läuft kostenlos auf einem 5-Dollar-VPS. Es spart mir 20 Minuten pro Meeting – mal 10 Meetings pro Woche, mal 50 Wochen... das sind über 160 Stunden pro Jahr. Was ist Ihr Stundensatz?"

---

## 4. Variationen (Was kann man sonst noch machen?)

### Gleiches Pattern, verschiedene Inputs

| Input-Quelle | Anwendungsfall |
|--------------|----------------|
| E-Mail-Weiterleitung | Newsletter automatisch zusammenfassen |
| Slack-Nachricht | Team-Update-Digest |
| RSS-Feed | Branchen-News-Briefing |
| Kalender-API | Pre-Meeting-Kontextvorbereitung |
| Dokument-Upload | Vertrags-/Bericht-Zusammenfassung |

### Gleiches Pattern, verschiedene Outputs

| Output | Anwendungsfall |
|--------|----------------|
| Slack DM | Echtzeit-Benachrichtigung |
| Todoist/Things | Action Items extrahieren |
| CRM-Notiz | Kunden-Meeting-Log |
| Wöchentlicher Digest | Aggregierte Zusammenfassungs-E-Mail |
| Audio-Datei (ElevenLabs) | Beim Pendeln anhören |

### Gleiches Pattern, verschiedene Profile

> „Sie können ein ganzes Team mit einem Workflow bedienen. Jede Person hat ihr Profil. Der CEO bekommt strategische Aufzählungspunkte. Der PM bekommt Action Items. Der Analyst bekommt volle Details."

---

## 5. Q&A-Anregungen (Falls das Publikum still ist)

Diese verwenden, um die Diskussion anzuregen:

1. „Welche Inhalte generieren oder empfangen Sie, die diese Behandlung gebrauchen könnten?"
2. „Wo sterben Zusammenfassungen in Ihrer Organisation gerade?"
3. „Was würden Sie in Ihr persönliches Profil aufnehmen, das ich nicht habe?"
4. „Wer sonst in Ihrem Team würde ein anderes Output-Format benötigen?"

---

## Backup: Falls n8n versagt

| Problem | Ausweichstrategie |
|---------|-------------------|
| API-Timeout | Das Mermaid-Diagramm in `n8n-workflow.md` durchgehen, jeden Schritt konzeptionell erklären |
| Notion Auth-Problem | Screenshot des erwarteten Outputs zeigen, auf „Warum" fokussieren, nicht auf „Wie" |
| E-Mail versagt | Überspringen – „E-Mail ist sowieso optional, der Notion-Output ist der Kern" |

---

## Zeitplan

| Abschnitt | Zeit |
|-----------|------|
| Einstieg + Setup-Kontext | 0:00 - 0:30 |
| Benutzerprofil zeigen | 0:30 - 2:30 |
| Workflow auslösen | 2:30 - 3:30 |
| Flow durchgehen | 3:30 - 7:30 |
| Output zeigen | 7:30 - 9:30 |
| Live-Variation | 9:30 - 11:30 |
| Wichtige Punkte | 11:30 - 13:00 |
| Variationen-Überblick | 13:00 - 14:00 |
| Q&A | 14:00 - 15:00 |

---

## Notizen für den Vortragenden

- **Energie:** Das ist eine *Show* – lassen Sie den Workflow laufen, lassen Sie die Leute die Magie sehen
- **Tempo:** Den Merge-Node nicht zu schnell erklären. Dort lebt die Architektur.
- **Publikumsverbindung:** Blickkontakt beim Wechseln der Profile. „Was würde *Ihr* Profil sagen?"
- **Technische Fragen:** Tiefgehende n8n-Fragen für den Workshop parken. „Gute Frage – lassen Sie uns das gemeinsam in der Hands-on-Session bauen."

---

*Skript-Version: 2026-01-31*
