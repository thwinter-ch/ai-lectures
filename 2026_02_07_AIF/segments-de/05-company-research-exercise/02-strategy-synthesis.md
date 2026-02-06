# Prompt für Strategie-Synthese

## Anleitung

**Fügen Sie Ihr Deep-Research-Output oberhalb dieses Prompts ein und führen Sie ihn dann aus.**

Dieser Prompt transformiert Rohdaten der Unternehmensrecherche in ein strukturiertes Strategiedokument unter Verwendung dreier bewährter Frameworks.

---

## Die Frameworks (30-Sekunden-Überblick)

| Framework | Zweck |
|-----------|-------|
| **Golden Circle** | Artikuliert den Unternehmenszweck (Why), die Differenzierung (How) und das Angebot (What) - die strategische Identität. |
| **Business Model Canvas (BMC)** | Bildet die neun Bausteine ab, wie das Unternehmen Wert schafft, liefert und erfasst. |
| **Value Proposition Canvas (VPC)** | Zoomt auf Kundenjobs, Schmerzen und Gewinne - und wie das Unternehmen diese adressiert. |

---

## Der Prompt

```
You are a senior, McKinsey-level strategy consultant. Using the research provided above, produce a **board-ready strategy document** that integrates the Golden Circle, Business Model Canvas, and Value Proposition Canvas.

**Opening Requirement:**
Begin with a **one-sentence executive maxim** — a crisp, authoritative quote capturing the strategic thesis.

**Output Rules:**
- One structured document (no tables, charts, or Excel)
- Consulting report style: clear headings, numbered subsections, concise paragraphs
- Each subsection starts with a 1-2 sentence executive summary, then detail
- Neutral, professional tone suitable for executives and boards
- Length: ~1,200–2,000 words
- Ground assertions in the research; mark unknowns as "TBD" with explicit assumptions
- Ensure Golden Circle ↔ BMC ↔ VPC are mutually consistent

---

### Part 1 — Golden Circle

**1. Why**
- Core statement: Single-sentence purpose
- Elaboration: Strategic implications (positioning, customer promise, culture)

**2. How**
- Core statement: Signature capabilities and principles
- Elaboration: Operating model, differentiators, proof points

**3. What**
- Core statement: Offerings and business scope
- Elaboration: Products/services and customer outcomes

---

### Part 2 — Business Model Canvas

For each of the nine blocks, provide a 1-2 sentence summary, then expand with concise bullets:

1. **Key Partners** — Critical alliances and supplier relationships
2. **Key Activities** — Core operations that make the model work
3. **Key Resources** — Assets required to deliver value
4. **Value Propositions** — The bundle of benefits for each segment
5. **Customer Relationships** — How the company acquires, retains, grows customers
6. **Channels** — How value reaches customers
7. **Customer Segments** — Who the company serves (and who it doesn't)
8. **Cost Structure** — Major cost drivers and economics
9. **Revenue Streams** — How the company monetizes

Mark financial unknowns as **TBD** and specify what evidence would resolve them.

---

### Part 3 — Value Proposition Canvas

**Customer Profile:**
- **Jobs to be Done** — Functional, emotional, and social jobs customers are trying to accomplish
- **Pains** — Obstacles, risks, and frictions (prioritize severe and frequent)
- **Gains** — Desired outcomes (distinguish must-haves from delighters)

**Value Map:**
- **Products & Services** — Offerings mapped to specific jobs
- **Pain Relievers** — How the offer removes key pains (be explicit)
- **Gain Creators** — How the offer enables gains (link to measurable outcomes)

**Conclude with a Fit Statement (2-3 sentences):** Summarize how Pain Relievers and Gain Creators address the most critical Jobs/Pains/Gains.

---

Now analyze the research above and produce the strategy document.
```

---

## Was Sie mit dem Output machen

Die Synthese liefert Ihnen drei Ebenen strategischer Klarheit. So nutzen Sie jede:

### Sofortige Anwendungen

| Output-Abschnitt | Anwendungsfall |
|------------------|----------------|
| **Executive Maxim** | Pitch Decks, Investorengespräche, interne Alignment-Dokumente |
| **Golden Circle** | Markenbotschaft, Kulturdokumente, "Über uns"-Texte, Einstellungskriterien |
| **BMC** | Vorstandspräsentationen, Partnerschaftsgespräche, operative Planung |
| **VPC** | Produkt-Roadmaps, Marketing-Messaging, Sales Enablement |

### Folgeaktionen

1. **Annahmen validieren** — Die Synthese markiert "TBD"-Punkte. Dies sind Ihre Recherche-Lücken. Priorisieren Sie das Schliessen derjenigen, die wichtige Entscheidungen beeinflussen.

2. **Das Fit Statement testen** — Entspricht Ihr VPC Fit Statement dem, was echte Kunden sagen? Falls nicht, haben Sie ein Positionierungsproblem oder eine Recherche-Lücke gefunden.

3. **Auf Widersprüche prüfen** — Die Frameworks sollten sich gegenseitig verstärken. Wenn Ihr Golden Circle "Why" nicht mit Ihrem VPC "Jobs to be Done" übereinstimmt, stimmt etwas nicht.

4. **Abgeleitete Artefakte erstellen:**
   - Verwandeln Sie den BMC in eine Investoren-Folie
   - Extrahieren Sie die VPC Pain Relievers für Feature-Priorisierung
   - Nutzen Sie den Golden Circle als Input für Messaging-Workshops

### Qualitätsprüfung

Bevor Sie den Output verwenden, verifizieren Sie:

- [ ] Das Executive Maxim ist verteidigbar (kein generisches Füllwort)
- [ ] BMC Kosten-/Umsatzstrukturen sind plausibel (oder als TBD markiert)
- [ ] VPC Jobs entsprechen Ihrem Zielkunden, nicht einem idealisierten
- [ ] Keine Widersprüche zwischen Golden Circle Positionierung und BMC Value Propositions

---

## Workflow-Zusammenfassung

```
Schritt 1: Deep Research      → Rohe Analyse und Fakten über das Unternehmen
Schritt 2: Strategie-Synthese → Strukturierte Frameworks (dieser Prompt)
Schritt 3: Ihr Urteil         → Validieren, verfeinern und einsetzen
```

AI übernimmt die Strukturierung. Sie übernehmen den Plausibilitäts-Check.
