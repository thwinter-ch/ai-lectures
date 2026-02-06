# Workshop-Übung: AI-gestützte Unternehmensrecherche

**Dauer:** 30 Minuten
**Output:** Führungskräfte-taugliches Unternehmens-Briefing mit Quellenangaben

---

## Schnellstart (Ergebnisse in 3-4 Minuten)

**Plattform:** Perplexity Pro (empfohlen) oder Claude mit Websuche

### Schritt 1: Diesen Prompt kopieren

```
You are a senior corporate strategist producing a concise, MECE briefing.

**Company:** [PASTE COMPANY NAME]
**Domain:** [PASTE INDUSTRY/WEBSITE IF KNOWN]
**Focus:** [YOUR COUNTRY/REGION]

Deliver a 1-page executive summary covering:
1. What they do & who they serve (2-3 bullets)
2. Business model & revenue streams (2-3 bullets)
3. Key differentiators vs. competitors (2-3 bullets)
4. 3 opportunities / 3 risks
5. Estimated size: revenue band, headcount band, growth signal

Cite sources inline. Flag anything estimated as [Est.].
```

### Schritt 2: In Perplexity Pro einfügen

1. Öffnen Sie [perplexity.ai](https://perplexity.ai)
2. Fügen Sie den Prompt ein
3. Ersetzen Sie die Platzhalter in Klammern durch Ihr Zielunternehmen
4. Enter drücken

### Schritt 3: Output prüfen

Sie erhalten ein Briefing mit Quellenangaben in ca. 60 Sekunden. Nutzen Sie dies als Ausgangspunkt für die vertiefte Analyse.

---

## Vollständiges 30-Minuten-Protokoll

### Wählen Sie Ihr Rechercheziel

| Option | Am besten für | Was Sie lernen |
|--------|---------------|----------------|
| **Ihr eigenes Unternehmen** | Selbstbewertung | Wie der Markt Sie sieht; blinde Flecken in der Positionierung |
| **Ein Wettbewerber** | Competitive Intelligence | Deren Strategien, Preisgestaltung, Schwächen zum Ausnutzen |
| **Ein Kunde/Prospect** | Vertriebsvorbereitung | Pain Points, Entscheidungskriterien, Budgetsignale |

---

## Der Prompt (Vollversion)

Kopieren Sie alles zwischen den gestrichelten Linien und fügen Sie es in Ihr AI-Tool ein.

---

```markdown
You are a **senior corporate strategist** producing a **McKinsey-style briefing**.

**INPUTS (fill these in):**
- **Company:** [COMPANY NAME]
- **Primary domain:** [INDUSTRY OR WEBSITE]
- **Geo focus:** [COUNTRY/REGION]
- **Tone:** Business (no humor)
- **Language:** English

---

## Research Protocol (in order)

1. **Company-owned sources:** website, product pages, pricing, newsroom, leadership bios, job posts
2. **Official registries:** SEC/Companies House/local equivalent, trademark databases
3. **Third-party data:** Crunchbase, LinkedIn, G2/Capterra, Glassdoor, Similarweb
4. **Media/analyst coverage:** business press, trade publications, conference mentions

---

## Deliverables

### Executive Summary (6-10 bullets max)
- What they do, who they serve, where they win/lose
- 3 opportunities, 3 risks
- Key metrics: revenue band, headcount band, growth signal, funding status
- Mark confidence: High/Med/Low for each headline

### Business Model Deep Dive
- Revenue streams & pricing model
- Cost structure signals
- Moat sources (IP, data, switching costs, distribution)

### Products & Solutions Table

| Product | Overview | Strengths | Weaknesses | Ideal Customer | Pricing |
|---------|----------|-----------|------------|----------------|---------|
| ... | ... | ... | ... | ... | ... |

### Competition Snapshot

| Competitor | Position | Strength | Weakness | Pricing Posture |
|------------|----------|----------|----------|-----------------|
| ... | ... | ... | ... | ... |

### Key Risks & Flags
- Legal/regulatory exposure
- Financial health signals
- Leadership/culture red flags

### Data Gaps
- What couldn't be verified
- Questions for management/sales calls

---

## Quality Rules

- **Cite every material claim** with (Source, Date) and link
- **No speculation** - mark estimates as [Est.] and show method
- **If sources conflict**, present both and state which you weight more
- **Numbers over adjectives** - "30% growth" not "rapid growth"
- **If no data found**, say exactly: "No reliable public data found."
```

---

## Plattform-Empfehlungen

| Plattform | Stärken | Einschränkungen | Am besten für |
|-----------|---------|-----------------|---------------|
| **Perplexity Pro** | Echtzeit-Web, Auto-Zitate, Quellenlinks | Gelegentlich oberflächlich | Schnelle Recherche, zitationsintensiver Output |
| **Claude (Web)** | Bessere Analyse, strukturierter Output | Langsamer, weniger Quellen | Synthese & strategische Einordnung |
| **ChatGPT (Web)** | Gute allgemeine Abdeckung | Zitatqualität variiert | Breite Recherche-Sweeps |
| **Gemini** | Stark bei aktuellen News, Google-Integration | Kann Details halluzinieren | News-lastige Recherche |

**Empfehlung:** Starten Sie mit Perplexity Pro für Fakten und Zitate. Nutzen Sie Claude für Synthese und strategische Einordnung.

---

## Erwarteter Output

Nach 30 Minuten sollten Sie haben:

1. **Executive Summary** (1 Seite) - teilbar mit der Führungsebene
2. **Produktetabelle** - copy-paste-bereit
3. **Wettbewerbermatrix** - Positionierung auf einen Blick
4. **Risikohinweise** - rot/gelb/grün mit Belegen
5. **Zitationsnachweis** - jede Aussage durch 1+ Quellen gestützt

**Qualitätsmassstab:** Ein Kollege sollte dieses Briefing in einem Kundengespräch oder bei der Vorstandsvorbereitung nutzen können, ohne zusätzliche Recherche.

---

## Problemlösung

| Problem | Lösung |
|---------|--------|
| "No data found" für Finanzdaten | Privates Unternehmen - suchen Sie nach Finanzierungsrunden, Mitarbeiterzahl-Proxies, Glassdoor-Gehaltsdaten |
| Widersprüchliche Zahlen | Beide präsentieren, beide zitieren, angeben welche glaubwürdiger ist und warum |
| Output zu lang | Nachfragen: "Summarize as 10 bullet points with citations" |
| Output zu oberflächlich | Nachfragen: "Go deeper on [specific section]. Cite 3+ sources." |
| Falsches Unternehmen | Disambiguierende Info hinzufügen: "The [City]-based [Industry] company, not the [Other] one" |

---

## Zeitaufteilung

| Phase | Zeit | Aktivität |
|-------|------|-----------|
| Setup | 2 Min. | Ziel wählen, Prompt-Variablen ausfüllen |
| Schnell-Scan | 3 Min. | Schnellstart-Prompt ausführen, ersten Output prüfen |
| Vertiefung | 15 Min. | Vollständigen Prompt ausführen, Lücken iterieren |
| Synthese | 5 Min. | Tabellen bereinigen, Zitate verifizieren |
| Sicherung | 5 Min. | Output speichern, Folgefragen notieren |

---

## Nach dem Workshop

Nehmen Sie Ihr Recherche-Output und:

1. **Identifizieren Sie 3 handlungsrelevante Erkenntnisse**, die Sie vorher nicht kannten
2. **Markieren Sie 2 Fragen** zur Verifizierung mit Primärquellen (Anrufe, Meetings)
3. **Teilen Sie eine Erkenntnis** mit einem Kollegen, der sie nutzen könnte

Das Ziel ist nicht ein perfekter Bericht - es ist der Aufbau der Routine für AI-gestützte Recherche, die Sie in unter einer Stunde zu "informiert genug zum Handeln" bringt.
