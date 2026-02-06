# Claude Projekt + Notion Auto-Push Einrichtungsanleitung

**Einrichtungszeit: ca. 10 Minuten**

Mach jede Claude-Konversation zu einem dauerhaften Wissens-Asset. Diese Anleitung zeigt dir, wie du ein Claude-Projekt konfigurierst, das automatisch Erkenntnisse zusammenfasst und in dein Notion Second Brain überträgt.

---

## Voraussetzungen

- Claude Pro Abonnement (für die Projekte-Funktion)
- Notion mit Claude verbunden (siehe [claude-notion-setup.md](./claude-notion-setup.md))

---

## Schritt 1: Notion-Datenbank erstellen lassen

Du musst die Datenbank nicht manuell erstellen — Claude kann das direkt für dich erledigen. Starte eine Konversation und sag:

> «Erstelle mir eine Second-Brain-Datenbank in Notion mit Feldern für Titel, Datum, Kernerkenntnisse, Quelle, Tags, Aktionspunkte und Konfidenz. Gib mir die Datenbank-ID.»

Claude erstellt die Datenbank und gibt dir die ID zurück. **Kopiere diese ID** — du brauchst sie im nächsten Schritt für die Projektanweisungen.

---

## Schritt 2: Claude-Projektanweisungen

Erstelle ein neues Claude-Projekt und füge diese Anweisungen ein:

### Basisanweisungen (Kopierfertig)

```
# Wissenserfassungsprotokoll

Du hast Zugriff auf Notion via MCP. Am Ende substantieller Gespräche überträgst du Erkenntnisse in mein Second Brain.

## Notion-Datenbank
- Datenbank-ID: [HIER DEINE ID EINFÜGEN]

## Automatische Erfassungsauslöser
Übertragung zu Notion bei:
- Ich sage «speichere das», «erfasse das», «push zu Notion» oder «Sitzung beenden»
- Gespräch enthält umsetzbare Erkenntnisse, Entscheidungen oder neuartige Frameworks
- Recherche liefert wiederverwendbare Ergebnisse

KEINE Übertragung bei:
- Schnellen Frage-Antwort-Sequenzen ohne dauerhaften Wert
- Fehlerbehebungssitzungen (es sei denn, sie offenbaren wiederverwendbare Muster)
- Beiläufigen Gesprächen

## Erfassungsformat
Bei Übertragung zu Notion wie folgt strukturieren:

**Titel**: [Prägnantes Thema — max. 60 Zeichen]

**Kernerkenntnisse** (3-5 Punkte):
- Mit dem Nicht-Offensichtlichen beginnen
- Fokus auf «was mein Denken verändert hat» oder «was ich nutzen kann»
- Überspringe Kontext, der googlebar ist

**Tags**: [Relevante Domänen-Tags]

**Quelle**: Claude Chat (oder passende Alternative)

**Konfidenz**:
- Hoch = verifiziert, gut begründet
- Mittel = plausibel, bedarf Validierung
- Spekulativ = Hypothese, frühe Überlegung

**Aktionspunkte**: [Nur wenn echte nächste Schritte vorhanden]

## Verhalten
- Vor Übertragung nachfragen, wenn der Wert unklar ist
- Zusammenfassen, was erfasst werden soll, bevor die Übertragung erfolgt
- Erfolgreiche Übertragung mit dem Eintragstitel bestätigen
```

---

## Schritt 3: Gesprächsabschluss-Prompt-Muster

Verwende diese Phrasen, um die Erfassung auszulösen:

| Phrase | Verhalten |
|--------|-----------|
| `«Speichere das in Notion»` | Sofortige Übertragung |
| `«Sitzung beenden»` | Zusammenfassen + übertragen + bestätigen |
| `«Was ist erfassenswert?»` | Claude schlägt vor, du genehmigst |
| `«Übertrage [spezifische Erkenntnis] zu Notion»` | Gezielte Erfassung |

### Beispielinteraktion

```
Du: «Dieses Framework zur Lieferantenbewertung ist nützlich. Speichere das in Notion.»

Claude: «Übertragung in dein Second Brain:

**Titel**: Lieferantenbewertungs-Framework — Make vs Buy
**Kernerkenntnisse**:
- Gesamtbetriebskosten schlagen Listenpreis (Integration, Schulung, Wechselkosten einbeziehen)
- Warnsignal: Lieferant kann seinen Wettbewerbsvorteil nicht artikulieren
- Entscheidungsheuristik: Wenn Sie es anders bauen würden, kaufen Sie es nicht
**Tags**: #beschaffung #entscheidungs-frameworks
**Quelle**: Claude Chat
**Konfidenz**: Hoch

Bestätigt: Eintrag erfolgreich erstellt.»
```

---

## Variante: Recherche-Modus

Für dedizierte Recherchesitzungen füge dies zu deinen Projektanweisungen hinzu:

```
## Recherche-Modus

Wenn ich «Recherche-Modus» sage, Verhalten anpassen:
- Alle substantiellen Erkenntnisse erfassen, nicht nur Schlussfolgerungen
- Quellen-URLs einbeziehen, wo relevant
- Mit #recherche und dem Thema taggen
- Mehrere Einträge erstellen, wenn verschiedene Unterthemen behandelt werden

Recherche-Modus beenden mit «Recherche abschliessen» — zu einem Zusammenfassungseintrag konsolidieren, der auf Detaileinträge verlinkt.
```

---

## Variante: Meeting-Notizen

Für die Erfassung von Meeting-Erkenntnissen:

```
## Meeting-Erfassung

Wenn ich sage «Meeting-Modus: [Meeting-Name]»:
- Fokus auf getroffene Entscheidungen, nicht auf Diskussion
- Aktionspunkte mit Verantwortlichen erfassen
- Meinungsverschiedenheiten oder offene Fragen notieren
- Mit #meeting und Teilnehmernamen taggen

Übertragungsformat:
- Titel: «[Datum] [Meeting-Name] — Kernentscheidungen»
- Kernerkenntnisse: Nur Entscheidungen
- Aktionspunkte: Wer macht was bis wann
```

---

## Variante: Brainstorming-Sitzungen

Für kreative Sitzungen:

```
## Brainstorming-Erfassung

Wenn ich «Brainstorming-Modus» sage:
- Konfidenz-Schwelle senken — spekulative Ideen erfassen
- Mit #brainstorming und #[thema] taggen
- «Kill-Kriterien» für Ideen einbeziehen (was würde dies widerlegen)

Am Ende: Ideen nach potenziellem Impact ranken, bevor sie übertragen werden.
```

---

## Fehlerbehebung

| Problem | Lösung |
|---------|--------|
| «Kann nicht auf Notion zugreifen» | MCP-Konfiguration in den Claude Desktop-Einstellungen prüfen |
| Übertragung schlägt stillschweigend fehl | Überprüfen, ob die Datenbank-ID korrekt ist |
| Falsche Datenbank | Bestätigen, dass die Datenbank-ID verwendet wird, nicht die Seiten-ID |
| Fehlende Eigenschaften | Sicherstellen, dass die Notion-Datenbank alle erforderlichen Spalten hat |

---

## Schnellreferenzkarte

```
┌─────────────────────────────────────────────────────────────┐
│ AUSLÖSER                                                    │
│ «speichere das» / «push zu Notion» / «Sitzung beenden»      │
├─────────────────────────────────────────────────────────────┤
│ MODI                                                        │
│ «Recherche-Modus» → mehr erfassen, am Ende konsolidieren    │
│ «Meeting-Modus: [Name]» → Entscheidungen + Aktionspunkte    │
│ «Brainstorming-Modus» → niedrigere Schwelle, Spekulatives   │
├─────────────────────────────────────────────────────────────┤
│ ABFRAGEN                                                    │
│ «Was ist erfassenswert?» → Claude schlägt vor               │
│ «Übertrage [spezifisches]» → gezielte Erfassung             │
└─────────────────────────────────────────────────────────────┘
```

---

## Was dir das bringt

- **Gespräche werden zu Assets** — Erkenntnisse überdauern den Chatverlauf
- **Durchsuchbare Wissensbasis** — Notions Filterung schlägt das Durchscrollen von Chats
- **Weniger Reibung** — kein manuelles Kopieren und Einfügen, keine Neuformatierung
- **Konsistente Struktur** — jede Erkenntnis wird gleich erfasst

Das beste Second Brain ist eines, das du tatsächlich nutzt. Dies beseitigt die Reibung, die die meisten Wissensmanagement-Systeme scheitern lässt.
