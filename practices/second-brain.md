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

Build a system that automatically saves insights from Claude conversations to Notion. No copy-paste, no friction.

```mermaid
flowchart LR
    A[Connect Notion] --> B[Create database]
    B --> C[Configure project]
    C --> D["Test: 'Save this'"]
```

---

## Step 1: Connect Claude to Notion

One-time setup (~10 minutes). After this, Claude can read and write directly to your Notion.

### Prerequisites

| Requirement | Details |
|-------------|---------|
| **Claude Pro** | Free version has no integrations. Check at claude.ai/settings |
| **Notion account** | Free tier is enough |
| **Desktop browser** | Chrome, Edge, Safari, or Firefox (not mobile) |

### 1a. Enable the Notion integration in Claude

1. Open [claude.ai](https://claude.ai) and sign in
2. Click your **profile icon** (bottom left)
3. Select **Settings**
4. Navigate to **Integrations** or **Connected Apps**
5. Find **Notion** and click **Connect**

### 1b. Authorize Claude in Notion

After clicking Connect, the Notion authorization page opens:

1. **Sign in to Notion** if needed
2. Review the permissions (read, insert, update)
3. **Select pages to share:**
   - Click **"Select pages"** (not "Access all pages")
   - Pick a dedicated page for your Second Brain
   - Do NOT share: sensitive HR, finance, or confidential pages
4. Click **Allow access**

### 1c. Verify the connection

Back in Claude:

1. Go to **Settings > Integrations**
2. Notion should show **"Connected"** (green indicator)

### 1d. Test it

Start a new Claude conversation and try:

```
Search my Notion for pages about [a topic you know exists]
```

If Claude finds nothing:
- Check that the page is in your shared selection
- Try a more specific page name

Then test write access:

```
Create a new page in my Notion called "Claude Test Note" with the content:
"This is a test note created by Claude."
```

Check in Notion that the page appears.

### Security notes

- Claude only accesses pages you explicitly shared
- You can revoke access anytime: Settings > Integrations > Notion > Disconnect
- Notion's workspace permissions still apply

---

## Step 2: Create the Notion database

Open a new Claude conversation and say:

> "Create a Second Brain database in my Notion with fields for Title, Date, Key Insights, Source, Tags, Action Items, and Confidence. Give me the database ID."

Claude creates the database and returns the ID. **Copy this ID.**

---

## Step 3: Set up the Claude Project

**Setup time: ~10 minutes**

Turn every Claude conversation into a permanent knowledge asset. You configure a Claude Project that summarizes and saves insights to your Notion Second Brain on command.

### Prerequisites

- Claude Pro subscription (for Projects feature)
- Notion connected to Claude (Step 1 above)

### Create the project

1. Go to [claude.ai](https://claude.ai) -> **Projects** (left sidebar)
2. Click **New Project**
3. Name it (e.g., "Second Brain")
4. Open **Project Instructions** and paste the text below
5. Replace `[YOUR DATABASE ID HERE]` with your database ID from Step 2

### Project Instructions (copy and paste)

```
# Wissenserfassungsprotokoll

Du hast Zugriff auf Notion via MCP. Am Ende substantieller Gespräche überträgst du Erkenntnisse in mein Second Brain.

## Notion-Datenbank
- Datenbank-ID: [YOUR DATABASE ID HERE]

## Wann übertragen
Übertragung zu Notion bei:
- Ich sage «speichere das», «erfasse das», «push zu Notion» oder «Sitzung beenden»
- Gespräch enthält umsetzbare Erkenntnisse, Entscheidungen oder neuartige Frameworks
- Recherche liefert wiederverwendbare Ergebnisse

NICHT übertragen bei:
- Schnellen Frage-Antwort-Sequenzen ohne dauerhaften Wert
- Fehlerbehebungssitzungen (es sei denn, sie offenbaren wiederverwendbare Muster)
- Beiläufigen Gesprächen

## Erfassungsformat
Bei Übertragung zu Notion so strukturieren:

**Titel**: [Prägnantes Thema — max. 60 Zeichen]

**Kernerkenntnisse** (3-5 Punkte):
- Mit dem Nicht-Offensichtlichen beginnen
- Fokus auf «was mein Denken verändert hat» oder «was ich nutzen kann»
- Überspringe Kontext, der googlebar ist

**Tags**: [Relevante Domänen-Tags]
**Quelle**: Claude Chat
**Konfidenz**: Hoch / Mittel / Spekulativ
**Aktionspunkte**: [Nur wenn echte nächste Schritte vorhanden]

## Verhalten
- Vor Übertragung nachfragen, wenn der Wert unklar ist
- Zusammenfassen, was erfasst werden soll, bevor die Übertragung erfolgt
- Erfolgreiche Übertragung mit dem Eintragstitel bestätigen
```

---

## Step 4: Test the full flow

1. Open a new conversation **inside your project** (not a regular conversation)
2. Have a short conversation -- e.g., ask for a summary of a topic
3. At the end, say: **"Save this to Notion"** (or "Speichere das in Notion")
4. Check in Notion that the entry appears

### Example

```
You: "Explain the key principles of value investing."

Claude: [explains value investing]

You: "Save this to Notion."

Claude: "Transferring to your Second Brain:

Title: Value Investing — Core Principles
Key Insights:
- Intrinsic value > market price = margin of safety
- Long-term horizon beats short-term volatility
- Quality companies at fair price > cheap companies
Tags: #investing #frameworks
Confidence: High

Confirmed: Entry created successfully."
```

---

## What you end up with

```
You: [Have a conversation with Claude]
You: "Save this to Notion"
Claude: [Summarizes, saves to database, confirms]
```

Every valuable conversation becomes a searchable, tagged entry in your Second Brain. No copying. No friction.

---

## Daily usage

| You say... | Claude does... |
|------------|----------------|
| "Save this to Notion" | Immediate transfer |
| "End session" | Summarize + transfer + confirm |
| "What's worth capturing?" | Claude suggests, you approve |
| "Capture [specific insight]" | Targeted capture |

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| "Claude can't access Notion" | Settings > Integrations > Notion > Manage access > Add page |
| Page created but not visible | Check the "Private" section in Notion, or search for the exact title |
| Claude can read but not write | Re-authorize the connection; check "Insert content" permission |
| Integration doesn't appear | Confirm Claude Pro (not free version). Sign out and back in. |
| Transfer fails | Check database ID in Project Instructions |
| Wrong database | Make sure you're using the database ID, not the page ID |
| Missing properties | Ensure the Notion database has all the required columns |
| Transfer not triggered | Make sure you're working inside the project, not in a regular conversation |

---

## Optional extensions (after the course)

You can extend the Project Instructions with modes. Open your existing project, go to **Project Instructions**, and add the desired block at the end.

### Research mode

```
## Recherche-Modus
Wenn ich «Recherche-Modus» sage:
- Erfasse jede substantielle Erkenntnis einzeln mit Quellen-URL
- Markiere Konfidenz pro Erkenntnis (Hoch/Mittel/Spekulativ)
- Bei «Recherche abschliessen»: Erstelle einen konsolidierten Eintrag mit allen Erkenntnissen, gruppiert nach Thema
```

### Meeting mode

```
## Meeting-Modus
Wenn ich «Meeting-Modus: [Name]» sage:
- Erfasse nur: Entscheidungen, Aktionspunkte (mit Verantwortlichen), offene Fragen
- Ignoriere Smalltalk und Hintergrundinfos
- Titel-Format: «Meeting — [Name] — [Datum]»
- Bei «Meeting Ende»: Übertrage sofort mit Aktionspunkten als Checkliste
```

### Brainstorming mode

```
## Brainstorming-Modus
Wenn ich «Brainstorming-Modus» sage:
- Erfasse auch spekulative und unfertige Ideen
- Konfidenz immer «Spekulativ» setzen
- Für jede Idee ein Kill-Kriterium notieren (was müsste stimmen, damit die Idee funktioniert?)
- Bei «Brainstorming Ende»: Übertrage alle Ideen als einzelnen Eintrag, sortiert nach Potenzial
```
