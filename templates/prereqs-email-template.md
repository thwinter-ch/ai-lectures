# Pre-Session Email Template

Template for sending prerequisite instructions to participants before a lecture.

## Template Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{name}}` | Participant's first name | Maria |
| `{{session_title}}` | Name of the session | AI Governance for Board Directors |
| `{{session_date}}` | Date of the session | 15. Februar 2026 |
| `{{session_time}}` | Start time | 09:00 Uhr |
| `{{session_location}}` | Venue or "Online" | HWZ Zürich, Raum 3.12 |
| `{{instructor_names}}` | Instructor names | Thomas Winter & Patrick Comboeuf |

---

## Email Template (German)

**Subject:** Vorbereitung für {{session_title}} am {{session_date}}

---

Guten Tag {{name}},

Wir freuen uns, Sie am **{{session_date}}** um **{{session_time}}** zum Workshop **{{session_title}}** begrüssen zu dürfen.

### Vorbereitungen

Damit wir die Zeit optimal nutzen können, bitten wir Sie, folgende Punkte **vor dem Workshop** zu erledigen:

#### Erforderlich

- [ ] **GitHub-Konto erstellen** (kostenlos)
  → [github.com/signup](https://github.com/signup)
  Wir nutzen GitHub für Kursmaterialien und praktische Übungen.

- [ ] **Claude Pro-Abo abschliessen** (CHF 20/Monat)
  → [claude.ai](https://claude.ai)
  Claude ist unser Haupt-Tool für die Hands-on-Übungen.

- [ ] **Laptop mitbringen**
  Mit aktuellem Browser (Chrome, Firefox, Safari oder Edge)

#### Optional (empfohlen)

- [ ] ChatGPT Plus für Vergleichsübungen
- [ ] Perplexity Pro für Recherche-Demos

### Treffpunkt

**Ort:** {{session_location}}
**Zeit:** {{session_date}}, {{session_time}}

Bei Fragen erreichen Sie uns jederzeit.

Freundliche Grüsse,
{{instructor_names}}

---

## Email Template (English)

**Subject:** Preparation for {{session_title}} on {{session_date}}

---

Dear {{name}},

We look forward to welcoming you to **{{session_title}}** on **{{session_date}}** at **{{session_time}}**.

### Preparation

To make the most of our time together, please complete the following **before the session**:

#### Required

- [ ] **Create a GitHub account** (free)
  → [github.com/signup](https://github.com/signup)
  We'll use GitHub for course materials and exercises.

- [ ] **Subscribe to Claude Pro** ($20/month)
  → [claude.ai](https://claude.ai)
  Claude is our primary tool for hands-on exercises.

- [ ] **Bring a laptop**
  With a modern browser (Chrome, Firefox, Safari, or Edge)

#### Optional (recommended)

- [ ] ChatGPT Plus for comparison exercises
- [ ] Perplexity Pro for research demos

### Meeting Point

**Location:** {{session_location}}
**Time:** {{session_date}}, {{session_time}}

Questions? Reach out anytime.

Best regards,
{{instructor_names}}

---

## Usage with n8n

1. Store participants in CSV: `name,email,company`
2. Read CSV with n8n "Read Binary File" or "Spreadsheet" node
3. Loop through rows with "Split In Batches" node
4. Replace variables in template with "Set" node
5. Convert Markdown to HTML with "Markdown" node (or custom code)
6. Send via "Gmail" or "SMTP" node
