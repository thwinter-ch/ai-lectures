# Build Log

Documentation of how this repository and lectures are built. Updated as work progresses.

---

## 2026-01-31: Repository Initialization

**Session goal:** Organize existing lecture materials into a structured GitHub repository.

### Decisions Made

| Decision | Rationale |
|----------|-----------|
| Monorepo vs multi-repo | **Monorepo chosen** — enables module reuse across lectures |
| Private folder convention | `docs.gitignore/` — self-documenting name, already in use |
| Git in Google Drive | Accepted trade-off — convenience over stability, commit frequently |
| Folder naming | `YYYY-MM_INSTITUTION_TOPIC` for consistency |

### Work Completed

1. **Created `.gitignore`** with patterns for:
   - `**/docs.gitignore/` — per-lecture private folders
   - Google Drive artifacts (`.gdoc`, `.gsheet`)
   - Audio files (often contain PII transcripts)
   - Sensitive filename patterns (`*participants*`, `*Teilnehmer*`, `*Dossier*`)

2. **Moved PII content:**
   - `2025_12_HWZ_CAS_VR/summaries/` → `docs.gitignore/summaries/` (participant names in filenames)

3. **Created module structure** (later deleted — see 2026-02-01):
   ```
   modules/  # DELETED 2026-02-01 — empty scaffolding, never used
   ```

4. **Created templates:**
   - `templates/prereqs-email-template.md` — DE/EN email for participant preparation

5. **Renamed folders** (partial — Drive sync blocked some):
   - `2025 04 12 AIF` → `2025-04_AIF`
   - Still pending: `2026_02_07_AIF`, `2026 Sovereignty`

6. **Pushed to GitHub:**
   - https://github.com/thwinter-ch/ai-lectures

### Outstanding

- [ ] Rename remaining folders when Drive sync allows
- [ ] Build n8n workflow for participant emails
- [ ] Build HWZ CAS lecture content

### Tools Used

- Claude Code (Opus 4.5) for planning and execution
- Git for version control
- GitHub CLI (`gh`) for repo creation
- **Wispr Flow** for voice-to-text dictation (productivity tool demonstrated in lecture content)

---

## 2026-01-31: HWZ AIF Lecture Planning

**Session goal:** Clean up repo, plan Feb 7 "AI Productivity Hacks for Executives" lecture.

### Brainstorm Origin

The lecture brainstorm document (`2026_02_07_AIF/AI Productivity Hacks for Executives Barainstorm.md`) was created via:

1. **Perplexity AI voice conversation** (Jan 24, 2026)
   - Used Wispr Flow for voice-to-text during ideation
   - Iteratively refined structure through conversational AI
   - Generated comprehensive markdown briefing
2. **Process demonstrates the lecture content itself** — building with AI-assisted voice capture

### Work Completed

1. **Archived 2025 lectures:**
   - Added `2025-04_AIF/` and `2025_12_HWZ_CAS_VR/` to `.gitignore`
   - Removed from git tracking (files remain local)
   - Committed and pushed

2. **Clarified naming convention:**
   - `YYYY-MM_INSTITUTION` (dash for date, underscore for parts)
   - Documented in HANDOFF.md

3. **Folder renames still blocked** by Google Drive sync — documented for manual fix later

### Critical Validation — COMPLETED

**Notion Write Capabilities (Validated 2026-01-31):**

| Platform | Read Notion | Write Notion | Setup | Notes |
|----------|-------------|--------------|-------|-------|
| **Claude Pro** | ✓ | ✓ | Simple | Notion MCP one-click integration |
| ChatGPT Plus | ✓ (extensions) | ❌ native | Complex | Requires custom GPT + API |
| Perplexity Pro | ✓ | ❌ native | Complex | Requires Make/Zapier for writes |

**Conclusion:** The brainstorm doc incorrectly recommended Perplexity for bidirectional integration. **Claude Pro is the only platform with native web-based write capability to Notion.**

**Prereq recommendation change:**
- Primary: **Claude Pro** ($20/mo) — required for hands-on exercises
- Alternative: ChatGPT Plus only if participant already has it AND is willing to set up custom GPT
- Perplexity: Remove from prereqs (read-only without automation tools)

### Outstanding

- [x] Validate Notion write capabilities for ChatGPT/Claude/Perplexity
- [x] Confirm lecture date (Feb 7 vs Feb 8)
- [ ] Get participant list
- [x] Build lecture content via GSD workflow

---

## 2026-01-31: Lecture Content Build (Sessions 3-4)

**Session goal:** Build all lecture segments for Feb 7 session.

### Work Completed

1. **Created 5 lecture segments** with `script.md` + `gamma-prompt.md`:
   - 01: How I Built This (system demo)
   - 02: Technology Revolution (2026 agent breakthrough)
   - 04: AI as Managerial Skill (80% abandon AI)
   - 06: Information Overload (cognitive limits + pull vs push)
   - 08: Ausblick & Realitätscheck (demos, sovereignty, password hygiene)

2. **Created 3 exercise segments** with guides:
   - 03: Writing Profile (Ruben Hassid method)
   - 05: Company Research (deep research + strategy synthesis)
   - 07: Second Brain (Claude + Notion setup)

3. **YouTube extraction skill created** at `~/.claude/skills/youtube-extraction/skill.md`
   - Tested Gemini API for video processing
   - Documented reliability issues with hallucination

### Learnings

- Gemini 2.0 Flash can process YouTube but hallucinated on specific videos
- Agent failures often due to missing folders — create folders before spawning agents
- Always use explicit absolute paths in agent prompts

---

## 2026-02-01: Folder Restructure + ZFU Cleanup

**Session goal:** Unify folder structure for chronological delivery, remove confidential ZFU content.

### Decisions Made

| Decision | Rationale |
|----------|-----------|
| Unified `segments/` folder | Chronological delivery order, easier prep |
| Number + type suffix | `01-name-lecture/` or `03-name-exercise/` for clarity |
| Purge ZFU from history | Confidential content, force-push acceptable |

### Work Completed

1. **Migrated folder structure:**
   - `slides/` + `exercises/` → unified `segments/` (01-09)
   - Chronological order matching delivery sequence

2. **Removed ZFU from repo:**
   - Deleted folder and all references from tracked files
   - Used `git filter-repo` to purge from history
   - Force-pushed clean history

3. **Updated documentation:**
   - Both READMEs (DE/EN) with new segment structure
   - HANDOFF.md with current status
   - .gitignore and BUILD_LOG.md cleaned

### Outstanding

- [x] Translate all content to German (Swiss orthography)
- [ ] Validate gamma-prompts in Gamma.app
- [ ] Generate slide decks
- [ ] Send student prereq email (Feb 3)
- [ ] Package materials for HWZ (Feb 5)

---

## 2026-02-01: README + Email Prep (Session 6)

**Session goal:** Finalize README with "Lecture as Code" concept, prepare student email workflow.

### Decisions Made

| Decision | Rationale |
|----------|-----------|
| Delete `modules/` | Empty scaffolding, no real content — YAGNI |
| Delete `lectures/` | Empty directory, no purpose |
| Add n8n MCP to project | Enable workflow automation for email sending |
| Lecture as Code framing | Analogous to Infrastructure as Code — makes concept accessible to tech audience |

### Work Completed

1. **Updated README.md:**
   - Added "Lecture as Code" concept (EN/DE bilingual)
   - Links to BUILD_LOG.md for transparency
   - Removed modules/ reference (deleted)
   - Clean structure diagram

2. **Extracted student data:**
   - Parsed `Studiengruppenliste_MCA-AIF25-1.pdf` (21 students)
   - Created `docs.gitignore/students.csv` (gitignored, contains PII)
   - Fields: first_name, last_name, company, function, email

3. **Deleted unused directories:**
   - `modules/` — placeholder READMEs only, never used
   - `lectures/` — empty

4. **Added project-level n8n MCP:**
   - Created `.mcp.json` with n8n-mcp config
   - Enables workflow automation within this project

### Outstanding

- [ ] Build/adapt n8n workflow for prereqs email
- [ ] Send prereqs email (Feb 3 deadline)
- [ ] Validate gamma-prompts in Gamma.app
- [ ] Generate slide decks
- [ ] Package materials for HWZ (Feb 5)

---

## 2026-02-05: Security Breach Fix + Repo Cleanup

**Session goal:** Address security incident and clean up repository.

### Security Incident

**What happened:** Student discovered that `.mcp.json` files containing API keys (n8n-mcp and gamma-mcp) were committed to the public GitHub repository. The n8n API key provided access to automation workflows including "Milkee Support Ingestion".

**Resolution:**
1. Identified the leaked keys via JWT decoding
2. Rotated both n8n and Gamma API keys immediately
3. Added `.mcp.json` and `**/.mcp.json` to `.gitignore`
4. Used `git filter-branch` to purge `.mcp.json` from entire git history
5. Force-pushed clean history to GitHub
6. Verified repo is clean of secrets via grep scan

**Lesson learned:** Always gitignore MCP configuration files from the start — they contain API keys by design.

### Cleanup Work

1. **Deleted empty files:**
   - `jounrey.md` (empty, typo of "journey")
   - `segments/07-second-brain-exercise/Untitled.md` (empty)

2. **Renamed files:**
   - `student-email.md` → `intro-email.md` (with date added)
   - `AI Productivity Hacks for Executives Barainstorm.md` → `2026-01-24 AI Productivity Hacks Brainstorm.md`

3. **Added to .gitignore:**
   - `HANDOFF.md` — internal session notes, not for public repo

4. **Updated tech-stack.md:**
   - Reorganized into Visual Design, Content Production Chain sections
   - Added OpenClaw to Automation
   - Added Typefully, Miro, nanoBanana
   - Removed "Max" from Claude (sounds like bragging)

### Outstanding

- [ ] Delete prereqs-email-template.md (never sent, superseded by intro-email)
- [ ] Validate gamma-prompts in Gamma.app
- [ ] Generate slide decks
- [ ] Package materials for HWZ

---

## 2026-02-07: Final Content Pass + Segment Merge

**Session goal:** Final review of segments 05–09, merge 08+09 into combined closer, upgrade exercise prompts.

### Decisions Made

| Decision | Rationale |
|----------|-----------|
| Merge 08+09 into single closer | Two separate endings felt disjointed; combined "wow + warning" structure is stronger |
| Fold cognitive science into 06 | 06 and 08 argued the same thesis; Miller's 7±2 and judges study strengthen 06 |
| Upgrade 05 prompts to deep research | 3k words was too shallow; 30k + SWOT + Porter's + AI disruption for real value |
| Real images instead of Mermaid | Finance execs won't have Mermaid renderers; Claude generates actual visuals |

### Work Completed

1. **Merged segments 08+09** into "Ausblick & Realitätscheck":
   - Part A: Demos (Telegram classifier, OpenClaw live demo, personalized summary)
   - Part B: Reality check (data sovereignty, prompt privacy, password hygiene)

2. **Upgraded segment 06** — folded in Miller's 7±2 Law and Danziger judges study

3. **Upgraded segment 05 exercise prompts:**
   - Deep research: 3k → 30k words, added SWOT, Porter's Five Forces, AI Disruption Analysis
   - Strategy synthesis: 2k → 10k words, real image generation, strategic recommendations

4. **Fixed segment 07** — restructured auto-push-project.md (clear 3-step flow, copy-paste mode extensions)

5. **Regenerated Gamma decks** for 06 and 08

6. **Cleaned up references** — timetable, READMEs, build log updated for 8-segment structure

### Gamma Decks (Final)

| Seg | Title | URL |
|-----|-------|-----|
| 01 | How I Built This | https://gamma.app/docs/01-Wie-ich-diese-Vorlesung-erstellt-habe-atjj9amvea35m4a |
| 02 | Technology Revolution | https://gamma.app/docs/02-Die-Technologie-Revolution-myy1vq3y7d4x16s |
| 04 | AI as Managerial Skill | https://gamma.app/docs/v5gsyrz3bf5anxo |
| 06 | Information Overload | https://gamma.app/docs/e3131dy593gw4ai |
| 08 | Ausblick & Realitätscheck | https://gamma.app/docs/twkfm2mwi1334ud |

---

## 2026-02-08: Post-Lecture Package — Recap Page + LinkedIn Series

**Session goal:** Turn raw lecture transcript + materials into a student recap website and a 10-post LinkedIn knowledge series.

### Methodology: Lecture → Post-Production Pipeline

This documents the repeatable workflow for turning any delivered lecture into post-lecture deliverables.

#### Step 1: Capture (During Lecture)

| Tool | Output | Cost |
|------|--------|------|
| **Optiverse** | Meeting transcription + summary PDF | Subscription (~CHF 30/mo) |
| **Gemini (Google Meet)** | Full transcript with timestamps (.md) | Included with Workspace |

**Key:** Run both simultaneously. Optiverse handles Swiss German well; Gemini provides timestamped raw transcript. The transcript is messy (voice-to-text artifacts) but contains all actual delivered content, including Q&A and tangents.

#### Step 2: Content Synthesis (Claude Code, ~2 hours)

**Inputs:**
- Gemini transcript (~91KB, ~2h50m of content)
- Optiverse summary PDF
- All prepared lecture scripts (`segments-en/*/script.md`)
- Exercise instruction files (`segments-en/*/README.md`)
- Timetable, tech stack, build log

**Process:**
1. Read all source materials into context
2. Cross-reference transcript (what was *actually said*) with scripts (what was *planned*)
3. Extract Q&A highlights, anecdotes, and live demonstrations not in scripts
4. Anonymize all student references (no names from transcript)
5. Produce `LECTURE-RECAP.md` — the editorial backbone

**Output:** Single markdown file covering: session overview, segment-by-segment recap (enriched with live delivery), Q&A highlights, exercise quick-reference with links, tools & resources, practical tips.

**Quality check:** Every Gamma deck link verified. Every GitHub exercise link verified. No PII.

#### Step 3: Web Page Production (Claude Code + frontend-design, ~1 hour)

**Input:** `LECTURE-RECAP.md`

**Process:**
1. Transform markdown into self-contained HTML (all CSS inline, vanilla JS only)
2. Design: long-read article style, mobile-responsive, smooth scroll navigation
3. Create inline SVG diagrams for key concepts (jagged frontier, centaur/cyborg, 7±2, second brain flow)
4. Add image placeholder slots for AI-generated illustrations
5. Test in browser (desktop + mobile viewport)

**Output:** `recap/index.html` — opens in any browser, no build step, no dependencies.

**Hosting:** GitHub Pages from repo root or `/docs` folder. URL added to main README.

#### Step 4: LinkedIn Series Production (Claude Code, ~1 hour)

**Input:** `LECTURE-RECAP.md` + lecture scripts

**Process:**
1. Extract 10 standalone insights from lecture content
2. Write each as a LinkedIn-native post (hook → insight → takeaway → CTA)
3. Series branding: "AI x Leadership | X/10"
4. Schedule: 2 posts/day over 5 days
5. Review for standalone value — each post must work for someone who wasn't at the lecture

**Output:** 10 markdown files in `recap/linkedin-series/`

**Publishing:** Via Typefully API/interface for scheduling + analytics.

#### Step 5: Illustrations (Optional, Gemini API)

**Input:** Image prompts written during Step 3

**Process:**
1. Write precise image prompts for 4-6 key concept illustrations
2. Generate via Gemini (free tier or API ~$0.15/call via OpenRouter)
3. Review quality; retry or switch to Gemini chat interface if needed

**Output:** PNG files in `recap/images/`

**Budget:** ~$2 for ~10-15 API calls.

#### Step 6: Publish and Cross-Link

1. Enable GitHub Pages (Settings → Pages → Source: main branch)
2. Add recap URL to main `README.md`
3. Schedule LinkedIn posts via Typefully
4. Send recap link to students (via email or LMS)

### Decisions Made

| Decision | Rationale |
|----------|-----------|
| Self-contained HTML (no framework) | Zero dependencies = opens anywhere, perfect for GitHub Pages |
| LinkedIn posts as standalone knowledge | "Look at my lecture" posts get zero engagement; standalone insights get shared |
| Markdown first, HTML second | Editorial backbone in markdown makes content reusable across formats |
| Parallelize web page + LinkedIn series | Independent tasks, same source material, halves production time |
| SVG diagrams over generated images | Instant, free, sharp at any resolution, self-contained in HTML |

### Work Completed

1. **Created `recap/LECTURE-RECAP.md`** — Full editorial recap from transcript + scripts + exercise materials
2. **Created `recap/index.html`** — Production-quality web page with SVG diagrams and scroll animations
3. **Created 10 LinkedIn posts** in `recap/linkedin-series/` — "AI x Leadership" series
4. **Documented methodology** — This entry (repeatable for future lectures)

### Cost Breakdown

| Item | Cost | Notes |
|------|------|-------|
| Claude Code (Opus) | ~$5-8 in API | Content synthesis + web page + LinkedIn posts |
| Optiverse | Included in subscription | Meeting transcription |
| Gemini transcript | Included in Workspace | Google Meet auto-transcription |
| Gamma decks | Included in subscription | Created during lecture prep phase |
| GitHub Pages | Free | Static hosting |
| Typefully | Included in subscription | LinkedIn scheduling |
| **Total incremental cost** | **~$5-8** | The lecture itself is the expensive part |

### Learnings

- The Gemini transcript is messy but gold — it captures Q&A, tangents, and anecdotes that are absent from prepared scripts. The recap is dramatically richer for it.
- Cross-referencing "what was planned" (scripts) with "what was said" (transcript) reveals the most interesting content: the live digressions, the extended discussions, the honest admissions.
- Self-contained HTML is the right call for educational content. No build step = any student can view it on any device immediately.
- LinkedIn series should be written AFTER the recap, not in parallel with the recap. The recap crystallizes the insights; the posts extract them.
- 10 posts from a 3.5-hour lecture is easy — the constraint is making each one standalone, not finding enough material.

### Outstanding

- [ ] Generate illustrations via Gemini API (4-6 concept visuals)
- [ ] Enable GitHub Pages and verify public URL
- [ ] Schedule LinkedIn posts via Typefully
- [ ] Send recap link to enrolled students
- [ ] Add recap URL to main README.md

---

## Template for Future Entries

```markdown
## YYYY-MM-DD: [Session Title]

**Session goal:** [One sentence]

### Decisions Made
| Decision | Rationale |
|----------|-----------|

### Work Completed
1. ...

### Outstanding
- [ ] ...

### Learnings
- ...
```
