# Second Brain

**Duration:** 25 min
**Tools:** Claude Pro + Notion (required combination)
**Deliverable:** Auto-capture system that saves Claude conversations to Notion
**Status:** proven
**Used in:** 2026_02_07_AIF

> **Which tool?**
> - **Claude Pro + Notion:** Only combination that works natively (MCP integration)
> - ChatGPT and Perplexity cannot write to Notion
> - Free Claude cannot connect to Notion

---

> Baue ein System, das deine Erkenntnisse aus Claude-Gesprächen automatisch in Notion speichert. Kein Copy-Paste, keine Reibung.

```mermaid
flowchart LR
    A[Notion verbinden] --> B[Datenbank erstellen]
    B --> C[Projekt konfigurieren]
    C --> D["Testen: 'Speichere das'"]
```

---

## Los geht's

### 1. Claude mit Notion verbinden

Folge der Anleitung in [guides/claude-notion-setup.md](./guides/claude-notion-setup.md). Am Ende hast du Claude mit deinem Notion-Workspace verbunden.

> **Voraussetzung:** Claude Pro und ein Notion-Konto (kostenlose Version reicht).

### 2. Notion-Datenbank erstellen

Öffne eine neue Claude-Konversation und sag:

> «Erstelle mir eine Second-Brain-Datenbank in Notion mit Feldern für Titel, Datum, Kernerkenntnisse, Quelle, Tags, Aktionspunkte und Konfidenz. Gib mir die Datenbank-ID.»

Claude erstellt die Datenbank und gibt dir die ID. **Kopiere diese ID.**

### 3. Claude-Projekt einrichten

Folge der Anleitung in [guides/auto-push-project.md](./guides/auto-push-project.md). Du erstellst ein Claude-Projekt mit Anweisungen, die automatisch Erkenntnisse in dein Notion speichern.

### 4. Testen

Führe ein kurzes Gespräch in deinem neuen Projekt. Am Ende sag:

> «Speichere das in Notion.»

Prüfe in Notion, ob der Eintrag erscheint.

---

## Was du am Ende hast

```
Du: [Führst ein Gespräch mit Claude]
Du: «Speichere das in Notion»
Claude: [Fasst zusammen, speichert in Datenbank, bestätigt]
```

Jedes wertvolle Gespräch wird zu einem durchsuchbaren, getaggten Eintrag in deinem Second Brain. Kein Kopieren. Keine Reibung.

---

## Files

| File | Purpose | Duration |
|------|---------|----------|
| [guides/claude-notion-setup.md](./guides/claude-notion-setup.md) | Connect Claude to Notion (one-time) | 10 min |
| [guides/auto-push-project.md](./guides/auto-push-project.md) | Configure auto-capture project | 10 min |

**Order:** Setup first, then project.
