# Lecture as Code — Instruction Manual

A step-by-step playbook for building a university lecture using AI tools and version control. Written so you (or Claude Code) can reproduce the entire workflow.

This documents the exact process used to build the HWZ "AI Productivity Hacks for Executives" lecture (Feb 7, 2026). Total production: ~2 weeks side-project, ~$15 API costs.

---

## Phase 0: Prerequisites

### Tools You Need

| Tool | Role | Cost |
|------|------|------|
| **Claude Code** (CLI) | Orchestrator — writes content, manages files, runs agents | API usage (~$5-10/lecture) |
| **Git + GitHub** | Version control, hosting, transparency | Free |
| **Gamma.app** | Slide generation from text prompts | Subscription or free tier |
| **Perplexity Pro** | Deep research with citations | $20/mo |
| **Notion** | Knowledge capture (exercise output) | Free |
| **Wispr Flow** | Voice-to-text for brainstorming | Subscription |
| **Optiverse** | Meeting transcription (Swiss German capable) | ~CHF 30/mo |
| **Typefully** | LinkedIn post scheduling | Subscription |

### Accounts & API Keys

- GitHub account with `gh` CLI authenticated
- Gamma API key (store in `.mcp.json`, gitignored)
- n8n API key if using automation workflows (store in `.mcp.json`, gitignored)

---

## Phase 1: Repository Setup

### 1.1 Create the repo

```bash
mkdir ai-lectures && cd ai-lectures
git init
gh repo create <username>/ai-lectures --public --source=. --push
```

### 1.2 Create .gitignore

Critical patterns — add these before your first commit:

```gitignore
# Per-lecture private folders (PII, speaker notes)
**/docs.gitignore/

# MCP configuration (contains API keys)
.mcp.json
**/.mcp.json

# Google Drive artifacts
*.gdoc
*.gsheet
*.gslides

# Audio/video (often PII in transcripts)
*.ogg *.mp3 *.mp4 *.m4a *.wav *.webm *.mov

# Sensitive filename patterns
*participants*
*teilnehmer*
*Teilnehmer*
*Studiengruppenliste*
*transcript*

# Temp files
**/temp-gamma-payload.json
**/temp-gamma-*.json

# OS artifacts
.DS_Store
Thumbs.db
desktop.ini
```

### 1.3 Create folder structure

```
ai-lectures/
├── YYYY_MM_DD_INSTITUTION/    # One folder per lecture
│   ├── segments-de/           # Content in primary language
│   │   ├── 01-topic-lecture/
│   │   │   ├── script.md
│   │   │   └── gamma-prompt.md
│   │   ├── 02-topic-lecture/
│   │   ├── 03-topic-exercise/
│   │   │   ├── README.md      # Student-facing exercise guide
│   │   │   └── (supporting files)
│   │   └── ...
│   ├── segments-en/           # Translations (optional, can gitignore)
│   ├── input/                 # Reference materials, research docs
│   ├── docs.gitignore/        # PII: student lists, grades (gitignored)
│   ├── recap/                 # Post-lecture deliverables
│   │   ├── index.html         # Recap web page
│   │   ├── LECTURE-RECAP.md   # Editorial recap (markdown source)
│   │   └── linkedin-series/   # LinkedIn post files
│   ├── summary/               # Transcripts, meeting notes (gitignored)
│   ├── README.md              # Lecture overview (student-facing)
│   ├── TIMETABLE.md           # Minute-by-minute schedule (instructor only)
│   ├── BUILD_LOG.md           # Decision log (public)
│   └── .env.local             # Local config (gitignored)
├── templates/                 # Reusable across lectures
│   ├── prereqs-email-template.md
│   └── day-of-email-template.md
├── README.md                  # Repo-level overview
└── .gitignore
```

### 1.4 Create BUILD_LOG.md

Start this immediately. Every session gets an entry with:
- Session goal (one sentence)
- Decisions made (table: Decision | Rationale)
- Work completed (numbered list)
- Outstanding items (checkbox list)
- Learnings (bullet list)

This becomes the institutional memory of the project. It's public and it's the backbone of the "Lecture as Code" transparency story.

---

## Phase 2: Brainstorm & Research

### 2.1 Voice brainstorm

Use Wispr Flow or any voice-to-text tool. Walk and talk. Capture:
- Target audience and their pain points
- Key concepts you want to teach
- Exercises that build real deliverables (not toy exercises)
- Time constraints and segment structure

Save the raw transcript as a markdown file in the lecture folder.

### 2.2 Structure into segments

Design a delivery sequence that alternates lectures and exercises:

```
01 - Lecture (context/credibility)
02 - Lecture (theory)
03 - Exercise (apply theory from 01+02)
04 - Lecture (deeper theory)
05 - Exercise (apply theory from 04)
-- BREAK --
06 - Lecture (bridge to next exercise)
07 - Exercise (build something lasting)
08 - Lecture (demos + reality check + close)
```

Rules:
- Exercises produce real deliverables the student keeps
- Each lecture sets up the next exercise
- No more than 2 lectures in a row without an exercise
- Last segment is always demos + honest caveats

### 2.3 Research each segment topic

For each lecture segment, use Perplexity Pro to research:
- Key statistics and studies (with citations)
- Frameworks and models
- Real-world examples

Save research notes in `input/` or directly in the segment folder.

---

## Phase 3: Content Production

### 3.1 Write lecture scripts

For each lecture segment, create `script.md`:

```markdown
# Segment XX: [Title]

**Type:** Lecture | **Duration:** XX Min

## Key Data Points
- [Statistic 1 with source]
- [Statistic 2 with source]

## Core Concepts
### [Concept Name]
[Explanation. Keep it conversational. Write how you'd actually say it.]

### [Concept Name]
[...]

## Speaker Notes
- [Timing cues, audience interaction prompts, transition lines]

## Transition
[How this connects to the next segment]
```

Guidelines:
- Write how you speak, not how you write papers
- Include the actual quotes you'll say
- Mark audience interaction points explicitly
- Keep each concept to 2-3 minutes max

### 3.2 Write exercise guides

For each exercise, create `README.md` (student-facing):

```markdown
# [Exercise Name]

## What You'll Build
[One sentence: the deliverable they walk away with]

## Prerequisites
- [Tool 1]
- [Tool 2]

## Steps

### Step 1: [Action]
[Instructions. Include the exact prompt to copy-paste.]

### Step 2: [Action]
[...]

## Expected Output
[What a good result looks like]

## Troubleshooting
[Common issues and fixes]
```

Rules:
- Every prompt must be copy-pasteable
- Include expected output descriptions
- Add troubleshooting for the 3 most common failures
- Time-box each step

### 3.3 Write Gamma prompts

For each lecture segment, create `gamma-prompt.md` — a structured slide description:

```markdown
## Slide 1: Title Slide
**Title:** [...]
**Subtitle:** [...]
**Visual:** [Describe the visual element]
**Speaker Note:** [What you'll say]

---

## Slide 2: [Topic]
**Title:** [...]
**Layout:** [e.g., two-column comparison, stat cards, single quote]
**Key Text:** [The actual words on the slide — max 25 words]
**Visual:** [Describe the visual]
**Speaker Note:** [What you'll say]
```

Rules:
- Max 25 words per slide
- Data callouts large and high-contrast
- Describe the visual you want (Gamma will generate or suggest)
- Every slide has a speaker note

### 3.4 Generate Gamma decks

Create a JSON payload per segment:

```json
{
  "textMode": "preserve",
  "cardSplit": "inputTextBreaks",
  "themeId": "[your-theme-id]",
  "sharingOptions": { "externalAccess": "view" },
  "imageOptions": { "source": "aiGenerated" },
  "cardOptions": { "dimensions": "16x9" },
  "textOptions": { "language": "de" },
  "additionalInstructions": "Swiss German: never use ß, always ss. Dark professional design. Minimal text per slide, max 25 words. Executive aesthetic.",
  "inputText": "[paste gamma-prompt.md content here]"
}
```

Submit via Gamma API or paste into Gamma.app. Save the resulting deck URL in the BUILD_LOG and README.

### 3.5 Translation (if bilingual)

If you need a second language version:
- Translate all `script.md` and `README.md` files
- For Swiss German: never use ß (always ss), keep Umlauts
- Exercise prompts: translate the full prompt text, not just instructions
- Gamma prompts: create separate payloads per language

---

## Phase 4: Pre-Lecture Admin

### 4.1 Extract student data

If you receive a participant list (PDF/Excel):
- Parse into `docs.gitignore/students.csv` (fields: first_name, last_name, company, function, email)
- This file is gitignored — never commit PII

### 4.2 Send intro email (1 week before)

Template in `templates/prereqs-email-template.md`. Include:
- Date, time, location
- Tool prerequisites (accounts to create, subscriptions to buy)
- Link to the GitHub repo (why not — build in public)
- Your contact info

### 4.3 Send day-of email (morning of)

Template in `templates/day-of-email-template.md`. Include:
- Quick links to materials
- Prereq reminder
- "See you at [time]"

### 4.4 Create timetable

`TIMETABLE.md` — minute-by-minute schedule with:
- Buffer time between segments (5 min each)
- Explicit fallback plan: what to cut if a segment runs over
- On-site checklist (projector, WiFi, accounts logged in, tabs open)

---

## Phase 5: Deliver the Lecture

### 5.1 Recording setup

Run simultaneously:
- **Optiverse** for meeting transcription + summary PDF
- **Gemini (Google Meet)** for timestamped raw transcript

Both are automatic. No manual work during delivery.

### 5.2 During the lecture

- Present Gamma decks in fullscreen (or download as PDF)
- Share exercise links via chat/screen
- If a bug is found, fix it live with Claude Code and push — this IS the demo

---

## Phase 6: Post-Lecture Recap (Same Day or Next Day)

This is where the "student experience" differentiator lives. Total time: ~4-5 hours. Cost: ~$8 API.

### 6.1 Gather inputs

Collect into `summary/` (gitignored):
- Gemini transcript (timestamped markdown)
- Optiverse summary PDF
- Your own notes from delivery

### 6.2 Write LECTURE-RECAP.md

Read all source materials into Claude Code context:
- All scripts from `segments-de/*/script.md`
- All exercise guides from `segments-de/*/README.md`
- The transcript (what was actually said)
- Timetable, tech stack, build log

Cross-reference transcript with scripts. The transcript captures:
- Q&A highlights
- Tangents that became the best discussions
- Honest admissions and live anecdotes
- Things that went wrong

Produce a single markdown file:
- Session overview with key thesis
- Segment-by-segment recap (enriched with live delivery)
- Q&A highlights (anonymized — no student names)
- Exercise quick-reference table with links
- Tools & resources table
- Practical tips / "what I wish I'd known"
- Key quotes from the session

### 6.3 Build recap web page

Transform LECTURE-RECAP.md into `recap/index.html`:
- Self-contained HTML (all CSS inline, vanilla JS only)
- No framework, no build step, no dependencies
- Mobile-responsive, smooth scroll navigation
- Fixed nav bar with section links
- SVG diagrams for key concepts (inline, not external files)
- Cards for each segment with Gamma deck links
- Exercise quick-reference section
- Footer with repo link (pointing to lecture folder, not repo root)

Test in browser: desktop + mobile viewport.

### 6.4 Write LinkedIn series

From LECTURE-RECAP.md + scripts, extract standalone insights:

- Each post must work for someone who wasn't at the lecture
- Format: hook (1-2 lines) → insight → evidence → takeaway → CTA
- Series branding: "AI x Leadership | X/N"
- Write AFTER the recap (the recap crystallizes the insights)

Save as numbered markdown files in `recap/linkedin-series/`.

### 6.5 Send recap email

Draft in lecture folder as `YYYY-MM-DD-recap-email.md`. Include:
- Link to recap web page
- Quick links to all 3 exercises
- Recommended next steps (this week / this month / ongoing)
- Your contact info

### 6.6 Enable GitHub Pages

```bash
gh api repos/<username>/<repo>/pages -X POST --input - << 'EOF'
{"source":{"branch":"master","path":"/"}}
EOF
```

The recap page URL will be:
`https://<username>.github.io/<repo>/<lecture-folder>/recap/index.html`

### 6.7 Commit and push everything

```bash
git add recap/ BUILD_LOG.md README.md
git commit -m "feat: add post-lecture recap page and LinkedIn series"
git push
```

### 6.8 Schedule LinkedIn posts

Use Typefully or your preferred scheduler. Suggested cadence:
- Day 1: Opener post (student experience / value story)
- Days 2-6: 2 knowledge posts per day
- Day 7: Closer (meta-story — how the lecture was built)

---

## Phase 7: Iterate for Next Lecture

### 7.1 What carries forward

- `.gitignore` patterns
- `templates/` email templates
- Repo structure and conventions
- The BUILD_LOG methodology
- The recap production pipeline (Phase 6)

### 7.2 What's lecture-specific

- All content in `segments-*/`
- Gamma decks (new theme or reuse)
- Student data
- Timetable
- Recap

### 7.3 Starting a new lecture

```bash
mkdir YYYY_MM_DD_INSTITUTION
# Copy structure from previous lecture
# Update README.md with new lecture details
# Start a new BUILD_LOG entry
# Begin at Phase 2
```

---

## Appendix: File Naming Conventions

| Pattern | Example | Rule |
|---------|---------|------|
| Lecture folder | `2026_02_07_AIF` | `YYYY_MM_DD_INSTITUTION` |
| Segment folder | `04-ai-managerial-skill-lecture` | `NN-kebab-case-type` where type = `lecture` or `exercise` |
| Scripts | `script.md` | Always this name |
| Gamma prompts | `gamma-prompt.md` | Always this name |
| Exercise guides | `README.md` | Student-facing, always this name |
| Emails | `2026-02-05-intro-email.md` | Date-prefixed |
| Build log | `BUILD_LOG.md` | One per lecture folder |

## Appendix: Cost Breakdown (Per Lecture)

| Item | Cost | Notes |
|------|------|-------|
| Claude Code API | $5-10 | Content production + recap |
| Optiverse | Included | Meeting transcription |
| Gemini transcript | Included | Google Meet feature |
| Gamma decks | Included | Subscription |
| GitHub Pages | Free | Static hosting |
| Typefully | Included | LinkedIn scheduling |
| **Total incremental** | **$5-10** | Per lecture cycle |

## Appendix: Common Pitfalls

1. **Committing API keys.** Always gitignore `.mcp.json` from the start. If leaked, rotate immediately and use `git filter-repo` to purge history.
2. **Exercise links pointing to wrong language.** Double-check `segments-de` vs `segments-en` in all HTML and markdown files.
3. **Exercises running over.** Budget +5 min per exercise for setup issues. Have a fallback plan for each.
4. **Gamma fullscreen issues.** Test presentation mode before the lecture. Download as PDF as backup.
5. **Notion connector fragility.** Budget extra time for Claude-to-Notion setup. The MCP authorization flow trips people up.
6. **ChatGPT can't write to Notion.** Only Claude Pro and Perplexity Pro have native write connectors. Communicate this clearly in prereqs.
7. **Root-level GitHub Pages URL.** Not a problem — nobody types the root URL. Students get the direct recap link.
