# Lecture as Code — The Playbook

A Claude Code-executable playbook for building a university lecture from scratch. Every prompt is copy-pasteable. Every decision has a branch. Every template is inline.

Built from the actual process behind the HWZ "AI Productivity Hacks for Executives" lecture (Feb 7, 2026). Two weeks of side-project time. ~$15 in API calls. 3.5 hours of delivered content with 5 slide decks, 3 hands-on exercises, bilingual docs, and a post-lecture recap website.

---

## How to Use This Playbook

Open Claude Code in your project directory. Paste the prompts from each phase. Fill in the `{{variables}}`. Claude Code will generate the files, and you review/iterate.

**Variables you'll set once and reuse:**

```
{{LECTURE_TITLE}}     = e.g., "AI Productivity Hacks for Executives"
{{INSTITUTION}}       = e.g., "HWZ Zürich"
{{COURSE}}            = e.g., "CAS AI in Finance"
{{DATE}}              = e.g., "2026-02-07"
{{TIME}}              = e.g., "13:00-16:45"
{{DURATION_HOURS}}    = e.g., "3.5"
{{LANGUAGE}}          = e.g., "German (Swiss orthography: ss not ß)"
{{AUDIENCE}}          = e.g., "21 finance executives, mid-career, CAS program"
{{INSTRUCTOR}}        = e.g., "Thomas Winter"
{{GITHUB_USER}}       = e.g., "thwinter-ch"
{{REPO_NAME}}         = e.g., "ai-lectures"
{{FOLDER}}            = e.g., "2026_02_07_AIF"
```

---

## Phase 0: Bootstrap the Repo

> Skip this phase if you already have a lecture repo. Jump to Phase 1.

### Prompt 0.1 — Create repo and structure

Paste into Claude Code:

```
Create a public GitHub repo called {{REPO_NAME}} for {{GITHUB_USER}}.

Then create this folder structure:

{{FOLDER}}/
├── segments-de/          # Primary language content
├── segments-en/          # English translations (optional)
├── input/                # Research, reference docs
├── docs.gitignore/       # PII — gitignored
├── recap/                # Post-lecture deliverables
│   └── linkedin-series/
├── summary/              # Transcripts — gitignored
├── README.md
├── TIMETABLE.md
└── BUILD_LOG.md
templates/
├── prereqs-email-template.md
└── day-of-email-template.md
README.md                 # Repo-level

Create a .gitignore with these patterns:
- **/docs.gitignore/  (PII folders)
- .mcp.json and **/.mcp.json  (API keys)
- *.gdoc *.gsheet *.gslides  (Google Drive artifacts)
- *.ogg *.mp3 *.mp4 *.m4a *.wav *.webm *.mov  (audio/video)
- *participants* *teilnehmer* *Studiengruppenliste* *transcript*  (sensitive filenames)
- **/temp-gamma-*.json  (temp build files)
- **/summary/  (transcripts)
- .DS_Store Thumbs.db desktop.ini  (OS artifacts)
- .env .env.local *.log  (env files)
- HANDOFF.md  (internal notes)

Initialize BUILD_LOG.md with a template entry for today.
Commit and push.
```

---

## Phase 1: Plan the Lecture

### Prompt 1.1 — Brainstorm to structure

Do this BEFORE opening Claude Code. Walk. Talk. Use Wispr Flow or any voice recorder.

Record yourself answering:
1. Who is in the room? What do they care about?
2. What's the one thing they must walk away knowing?
3. What are 3 things they should be able to DO after the lecture?
4. What will surprise them? What's contrarian?
5. What existing tools/frameworks can I teach hands-on?

Save the transcript as `{{FOLDER}}/input/brainstorm-raw.md`.

### Prompt 1.2 — Structure into segments

Paste into Claude Code:

```
Read {{FOLDER}}/input/brainstorm-raw.md.

Design a segment structure for a {{DURATION_HOURS}}-hour lecture for {{AUDIENCE}}.

Rules:
- Alternate lecture and exercise segments
- Never more than 2 lectures in a row without a hands-on exercise
- Each exercise must produce a REAL deliverable the student keeps and uses after the lecture
- Include a 15-min break roughly at the midpoint
- Last segment: demos of advanced capabilities + honest reality check/caveats
- Budget 5 min buffer between each segment

Output a table:
| # | Segment Name | Type (lecture/exercise) | Duration | What students get |

Then output a TIMETABLE.md with minute-by-minute schedule including:
- Exact times for a start time of {{TIME}}
- Buffer slots between segments
- A "what to cut" fallback plan for each segment if it runs over
- An on-site checklist section
```

### Decision point: How many segments?

| Duration | Segments | Structure |
|----------|----------|-----------|
| 2 hours | 5-6 | 3 lectures + 2 exercises |
| 3-4 hours | 7-9 | 4-5 lectures + 3 exercises |
| Full day (6+ hours) | 12-15 | 6-8 lectures + 4-6 exercises |

---

## Phase 2: Research & Write Content

### Prompt 2.1 — Research each lecture segment

For each lecture segment, use Perplexity Pro (or paste this into Claude Code if you have web search):

```
Research the following topic for a lecture segment:

Topic: {{SEGMENT_TOPIC}}
Audience: {{AUDIENCE}}
Duration: {{SEGMENT_DURATION}} minutes

I need:
1. 3-5 key statistics with sources (studies, not blog posts)
2. 1-2 frameworks or models that explain the concept
3. 2-3 real-world examples or case studies
4. 1 contrarian or surprising angle
5. Specific numbers I can put on slides (big, visual callouts)

Output as markdown. Cite every claim.
```

Save each result to `{{FOLDER}}/input/research-segment-NN.md`.

### Prompt 2.2 — Write all lecture scripts

Paste into Claude Code:

```
Read all files in {{FOLDER}}/input/ (brainstorm + research files).
Read {{FOLDER}}/TIMETABLE.md for the segment structure.

For each LECTURE segment, create {{FOLDER}}/segments-de/NN-name-lecture/script.md.

Script format:
# Segment NN: [Title]
**Type:** Lecture | **Duration:** XX Min

## Key Data Points
- [Stat with source — these go on slides as big callouts]

## Core Concepts
### [Concept Name]
[Write this as spoken text. How I'd actually say it in front of the room.
Use {{LANGUAGE}}. Keep it conversational. No academic language.
Include the actual phrases and analogies I'd use.]

### [Concept Name]
[Same approach]

## Audience Interaction
- [Where to ask a question]
- [Where to pause for reaction]
- [Where to take a poll]

## Transition to Next Segment
[The exact bridge sentence to the next segment]

Rules:
- Write how a speaker talks, not how a paper reads
- Each concept = 2-3 minutes max
- Include at least one moment of honest admission ("here's what doesn't work yet")
- Every slide-worthy stat gets its own callout
- The transition must connect logically to whatever comes next
```

### Prompt 2.3 — Write all exercise guides

Paste into Claude Code:

```
Read all files in {{FOLDER}}/input/.
Read {{FOLDER}}/TIMETABLE.md for segment structure.

For each EXERCISE segment, create {{FOLDER}}/segments-de/NN-name-exercise/README.md.

Exercise guide format:
# [Exercise Name]

## Was Sie erstellen
[One sentence: the deliverable. Not what they'll "learn" — what they'll HAVE.]

## Voraussetzungen
- [Tool 1 + link]
- [Tool 2 + link]

## Schritt 1: [Action Verb]
[Clear instruction. Then the exact prompt to copy-paste in a code block.]

```
[THE ACTUAL PROMPT — complete, ready to paste into the AI tool.
No placeholders except for personal details like company name.
Must produce useful output on first try.]
```

**Erwartetes Ergebnis:** [What good output looks like. Length, format, content.]

## Schritt 2: [Action Verb]
[Same structure]

## Schritt 3: [Action Verb]
[Same structure]

## Fehlerbehebung
| Problem | Lösung |
|---------|--------|
| [Common issue 1] | [Fix] |
| [Common issue 2] | [Fix] |
| [Common issue 3] | [Fix] |

Rules:
- Every prompt must work on first paste. Test it mentally.
- Students should produce a real deliverable in {{SEGMENT_DURATION}} minutes
- Include expected output descriptions so students know if theirs is good
- Troubleshooting section: the 3 things that WILL go wrong
- Write in {{LANGUAGE}}
```

### Prompt 2.4 — Write Gamma slide prompts

Paste into Claude Code:

```
Read each script.md in {{FOLDER}}/segments-de/*/

For each LECTURE segment, create a gamma-prompt.md in the same folder.

Format — one section per slide, separated by ---:

## Slide 1: Title Slide
**Title:** [Max 8 words]
**Subtitle:** [Max 12 words]
**Visual:** [Describe the image/icon/diagram you want]
**Speaker Note:** [What I'll say while this slide is up — 2-3 sentences]

---

## Slide 2: [Topic]
**Title:** [Max 8 words]
**Layout:** [Choose: stat-cards | two-column-comparison | single-quote | diagram | numbered-list | image-left-text-right]
**Key Text:** [The actual words on the slide — MAX 25 WORDS. Less is better.]
**Data Callout:** [If applicable: the big number, e.g., "80%" or "+40%"]
**Visual:** [Describe what you want]
**Speaker Note:** [2-3 sentences]

Rules:
- Max 25 words of text per slide. Slides are visual, not documents.
- Data callouts: huge font, high contrast
- 6-10 slides per segment (roughly 1 slide per 1.5-2 minutes)
- Every stat from script.md gets its own slide or callout
- Speaker notes contain what I'll actually SAY — not a repeat of slide text
- Last slide: transition/teaser for next segment
```

### Prompt 2.5 — Generate Gamma JSON payloads

Paste into Claude Code:

```
For each gamma-prompt.md in {{FOLDER}}/segments-de/*/,
create a temp-gamma-NN.json file in {{FOLDER}}/ with this structure:

{
  "textMode": "preserve",
  "cardSplit": "inputTextBreaks",
  "themeId": "7tjaturvprr6xac",
  "sharingOptions": { "externalAccess": "view" },
  "imageOptions": { "source": "aiGenerated" },
  "cardOptions": { "dimensions": "16x9" },
  "textOptions": { "language": "de" },
  "additionalInstructions": "Swiss German: NEVER use ß, always ss. Umlauts (ä, ö, ü) are correct. Dark professional design. Monoline icons, blueprint style. Deck title starts with 'NN - '. Minimal text per slide, max 25 words. Data callouts large and high-contrast. Executive aesthetic.",
  "inputText": "[PASTE THE FULL gamma-prompt.md CONTENT HERE, escaped for JSON]"
}

These files are gitignored (temp-gamma-*.json pattern).
I'll submit them to Gamma manually or via API.
```

Then submit each JSON to Gamma. Save the resulting deck URLs in BUILD_LOG.md and README.md.

---

## Phase 3: Translation (If Bilingual)

### Prompt 3.1 — Translate all content

Paste into Claude Code:

```
For each file in {{FOLDER}}/segments-de/*/,
create a translated version in {{FOLDER}}/segments-en/*/ (same folder structure).

Translation rules:
- Translate script.md, README.md, gamma-prompt.md
- Keep technical terms in English (they're usually better known)
- Exercise prompts: translate the FULL prompt text, not just the instructions around it
- Maintain the same conversational tone — don't make it more formal
- Keep all formatting, headers, code blocks identical

DO NOT translate: BUILD_LOG.md, TIMETABLE.md (these stay in primary language)
```

---

## Phase 4: Pre-Lecture Admin

### Prompt 4.1 — Extract student data from PDF

Paste into Claude Code:

```
Read the file {{FOLDER}}/docs.gitignore/[participant-list-file].

Extract a CSV with columns: first_name, last_name, company, function, email
Save to {{FOLDER}}/docs.gitignore/students.csv

This file is gitignored. Never commit it.
Count the students and tell me the total.
```

### Prompt 4.2 — Draft intro email

Paste into Claude Code:

```
Draft an intro email for the lecture.

Details:
- Lecture: {{LECTURE_TITLE}}
- Date/Time: {{DATE}}, {{TIME}}
- Location: {{INSTITUTION}}
- Audience: {{AUDIENCE}}
- Prerequisites: [list the tools students need — accounts, subscriptions]
- Materials link: https://github.com/{{GITHUB_USER}}/{{REPO_NAME}}/tree/master/{{FOLDER}}

Tone: informal du-Form (German), friendly but direct.
Include: why they need the paid subscription (be specific about what it enables).
Include: your contact info (phone, LinkedIn).
Save to {{FOLDER}}/{{DATE}}-intro-email.md

Format it so I can copy everything below a --- line directly into Outlook.
```

### Prompt 4.3 — Write README.md

Paste into Claude Code:

```
Create {{FOLDER}}/README.md — the student-facing lecture overview.

Include:
1. Title, course, institution, date, time, instructor
2. Segment table (linked to Gamma decks for lectures, linked to README.md for exercises)
3. "What you'll build" section — list the deliverables from exercises
4. Prerequisites table (tool, cost, purpose, signup link)
5. "After the lecture" section — link to recap page (will be created later)

Write in {{LANGUAGE}}.
Keep it clean. This is what students see when they open the repo.
```

---

## Phase 5: Deliver the Lecture

No Claude Code prompts here. This is you in the room.

### Checklist

- [ ] Gamma decks in browser tabs (one per lecture segment)
- [ ] Claude Code open on laptop for live demo / bug fixes
- [ ] Exercise links ready to share via screen / chat
- [ ] Optiverse running for transcription
- [ ] Gemini auto-transcription running (Google Meet)
- [ ] WiFi credentials for students
- [ ] Your accounts logged in: Claude, Notion, Perplexity, Gamma

### During delivery

- If something breaks, fix it live with Claude Code. Push to repo. This IS the demo.
- Watch for the best Q&A moments — they'll go in the recap.
- Note which exercises students struggled with — that's troubleshooting content.

---

## Phase 6: Post-Lecture Recap

This phase turns a delivered lecture into a student resource and a content series. Total time: ~4-5 hours. Cost: ~$8 in API calls.

### Prompt 6.1 — Gather and synthesize

Place your transcript files in `{{FOLDER}}/summary/` (gitignored), then paste into Claude Code:

```
Read ALL of the following files:

Source materials:
- All scripts: {{FOLDER}}/segments-de/*/script.md
- All exercise guides: {{FOLDER}}/segments-de/*/README.md
- {{FOLDER}}/TIMETABLE.md
- {{FOLDER}}/BUILD_LOG.md

Transcript/summary (in {{FOLDER}}/summary/):
- [Gemini transcript filename]
- [Optiverse summary filename]

Cross-reference what was PLANNED (scripts) with what was ACTUALLY SAID (transcript).
The transcript is messy voice-to-text — that's fine. It contains the gold: Q&A, tangents, honest admissions, anecdotes, live demonstrations not in scripts.

Create {{FOLDER}}/recap/LECTURE-RECAP.md with these sections:

1. **Session Overview** (3-4 sentences, key thesis)
2. **Segment-by-Segment Recap** — for each segment:
   - Type badge (Lecture/Exercise), duration, link to Gamma deck or exercise guide
   - What happened (enriched with transcript — not just the script)
   - "Highlights from the live session" — quotes, anecdotes, extended discussions
   - Key concepts with one-line explanations
3. **Q&A Highlights** — the best discussions, anonymized (NO student names)
4. **Exercise Quick Reference** — table with links
5. **Slide Decks** — table with Gamma links
6. **Tools & Resources** — table: tool, role, link
7. **Recommended Next Steps** — this week / this month / ongoing
8. **Practical Tips** — "What I wish I'd known" section from delivery experience
9. **Key Quotes** — the best lines from the session (blockquotes)

Write in {{LANGUAGE}}.
Verify every link works before outputting.
```

### Prompt 6.2 — Build recap web page

Paste into Claude Code:

```
Read {{FOLDER}}/recap/LECTURE-RECAP.md.

Create {{FOLDER}}/recap/index.html — a self-contained web page.

Requirements:
- ALL CSS inline in a <style> block. No external stylesheets except Google Fonts (Inter).
- Vanilla JS only. No frameworks, no build step, no dependencies.
- Mobile-responsive. Test at 375px and 1200px widths.
- Fixed nav bar at top with section links. Include a "GitHub Repo" link pointing to:
  https://github.com/{{GITHUB_USER}}/{{REPO_NAME}}/tree/master/{{FOLDER}}

Design:
- Hero section: dark gradient (deep blue/navy), lecture title, date, instructor
- Cards for each segment: number badge, type label (Vortrag/Übung), duration, "Open slides" button
- Blockquotes styled with left border accent
- Stat callouts: large numbers in cards (e.g., "80%", "+40%", "-19 Pp.")
- SVG diagrams for 2-3 key concepts (inline SVG, not external files)
- Smooth scroll navigation
- Fade-in animations on scroll (IntersectionObserver)
- Footer: institution, date, repo link

Color palette: navy/deep blue professional. Not startup-bright. Executive financial services aesthetic.

The page must open in any browser. No build step. Students click the link and it works.
```

### Prompt 6.3 — Write LinkedIn series

Paste into Claude Code:

```
Read {{FOLDER}}/recap/LECTURE-RECAP.md.
Read the brand voice file at ~/.claude/skills/_shared/brand-narrative.md
Read the LinkedIn formatting rules at ~/.claude/skills/linkedin-post/skill.md

Extract 10-12 standalone insights from the lecture content.

For each, write a LinkedIn post following these rules:
- Hook: first 1-2 lines must earn the "see more" click (under 210 chars)
- Voice: direct, operator-grade, first-person, present tense. No fluff.
- Never preachy, never motivational, never "thought leader"
- 800-1,300 characters per post
- Short paragraphs (1-3 lines), white space between
- Every post must work for someone who WASN'T at the lecture
- Concrete artifact or system behind every insight
- End with series tag: "AI x Leadership | N/12"
- Hashtags: use #FieldAI #BoardToBot #AIinProduction #BuildInPublic
- NEVER use: #AI #Leadership #Innovation #Motivation

Post 1: Link to the recap page (the "student experience" story)
Post 2: Link to this manual and the repo (the "lecture as code" story)
Posts 3-10: Knowledge posts (research findings, frameworks, exercises)
Posts 11-12: Meta posts (workflow, methodology)

Save each as {{FOLDER}}/recap/linkedin-series/NN-kebab-title.md
Include scheduling metadata in HTML comments at top:
<!-- Post N/12 | Schedule: Day X, AM/PM | Topic: ... | Pillar: ... -->
```

### Prompt 6.4 — Draft student recap email

Paste into Claude Code:

```
Draft a recap email for students.

Details:
- Lecture: {{LECTURE_TITLE}}
- Recap page: https://{{GITHUB_USER}}.github.io/{{REPO_NAME}}/{{FOLDER}}/recap/index.html
- Repo: https://github.com/{{GITHUB_USER}}/{{REPO_NAME}}/tree/master/{{FOLDER}}
- Exercise links: [list the GitHub URLs for each exercise README.md]

Include:
1. Link to recap page (primary CTA)
2. Quick links table for each exercise
3. Recommended next steps (this week / this month / ongoing)
4. Contact info

Tone: same as intro email. Informal, {{LANGUAGE}}, du-Form.
Save to {{FOLDER}}/{{DATE}}-recap-email.md
Format for direct copy into Outlook.
```

### Prompt 6.5 — Enable GitHub Pages and push

Paste into Claude Code:

```
Enable GitHub Pages for {{GITHUB_USER}}/{{REPO_NAME}} serving from master branch root.
Then commit all recap content and push.
Verify the recap page is accessible at:
https://{{GITHUB_USER}}.github.io/{{REPO_NAME}}/{{FOLDER}}/recap/index.html
```

---

## Phase 7: Next Lecture

### Prompt 7.1 — Start a new lecture

Paste into Claude Code:

```
I'm building a new lecture in the same repo.

Details:
- Title: {{NEW_LECTURE_TITLE}}
- Institution: {{NEW_INSTITUTION}}
- Date: {{NEW_DATE}}
- Time: {{NEW_TIME}}
- Duration: {{NEW_DURATION}} hours
- Audience: {{NEW_AUDIENCE}}
- Language: {{NEW_LANGUAGE}}

Create the folder structure under {{NEW_FOLDER}}/ (same pattern as {{FOLDER}}/).
Start a BUILD_LOG.md entry for today.
Update the repo-level README.md to add this lecture to the lectures table.

I'll start with a voice brainstorm. Read LECTURE-AS-CODE-MANUAL.md and
walk me through Phase 1 when I'm ready.
```

---

## Appendix A: File Naming Conventions

| Pattern | Example | Rule |
|---------|---------|------|
| Lecture folder | `2026_02_07_AIF` | `YYYY_MM_DD_INSTITUTION` |
| Lecture segment | `04-ai-managerial-skill-lecture/` | `NN-kebab-case-lecture` |
| Exercise segment | `03-writing-profile-exercise/` | `NN-kebab-case-exercise` |
| Script | `script.md` | Always this name, inside segment folder |
| Gamma prompt | `gamma-prompt.md` | Always this name, inside segment folder |
| Exercise guide | `README.md` | Always this name, student-facing |
| Email | `2026-02-05-intro-email.md` | `YYYY-MM-DD-purpose-email.md` |
| Build log | `BUILD_LOG.md` | One per lecture folder |
| Timetable | `TIMETABLE.md` | One per lecture folder |

## Appendix B: Cost Breakdown

| Item | Cost | Notes |
|------|------|-------|
| Claude Code API (content production) | ~$5-8 | Scripts, exercises, gamma prompts |
| Claude Code API (recap production) | ~$5-8 | Recap, web page, LinkedIn posts |
| Optiverse transcription | Included | Subscription ~CHF 30/mo |
| Gemini transcript | Included | Google Meet auto-transcription |
| Gamma slide decks | Included | Subscription |
| GitHub + GitHub Pages | Free | Hosting and version control |
| Typefully | Included | LinkedIn scheduling subscription |
| **Total per lecture** | **~$10-15** | Incremental cost |

## Appendix C: The Gamma JSON Template

```json
{
  "textMode": "preserve",
  "cardSplit": "inputTextBreaks",
  "themeId": "{{GAMMA_THEME_ID}}",
  "sharingOptions": {
    "externalAccess": "view"
  },
  "imageOptions": {
    "source": "aiGenerated"
  },
  "cardOptions": {
    "dimensions": "16x9"
  },
  "textOptions": {
    "language": "{{LANGUAGE_CODE}}"
  },
  "additionalInstructions": "{{LANGUAGE_RULES}}. Dark professional design. Monoline icons, blueprint style. Deck title starts with 'NN - '. Minimal text per slide, max 25 words. Data callouts large and high-contrast. Executive aesthetic.",
  "inputText": "{{PASTE_GAMMA_PROMPT_CONTENT}}"
}
```

## Appendix D: Common Pitfalls

| Pitfall | Prevention |
|---------|------------|
| Committing API keys | Gitignore `.mcp.json` BEFORE first commit. If leaked: rotate key, `git filter-repo`, force push. |
| Exercise links → wrong language | Always verify `segments-de` vs `segments-en` in HTML and markdown |
| Exercises run over time | Budget +5 min per exercise. Have a "demo instead of do" fallback for each. |
| Gamma fullscreen issues | Test presentation mode before lecture. Download PDF as backup. |
| Notion connector fragile | Budget +10 min for setup. MCP auth flow trips people up. Have mobile app as fallback. |
| ChatGPT can't write to Notion | Only Claude Pro and Perplexity Pro have native write. Say this in prereqs email. |
| Recap links point to repo root | Always link to lecture folder: `/tree/master/{{FOLDER}}` |
| Posts in wrong voice | Load brand-narrative.md and linkedin-post skill BEFORE writing any posts |

---

*This playbook is open source. Fork the repo, swap your content, build your lecture.*
*Repository: https://github.com/thwinter-ch/ai-lectures*
