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

**Session goal:** Build all 9 lecture segments (6 lectures + 3 exercises) for Feb 7 session.

### Work Completed

1. **Created 6 lecture segments** with `script.md` + `gamma-prompt.md`:
   - 01: How I Built This (system demo)
   - 02: Technology Revolution (2026 agent breakthrough)
   - 04: AI as Managerial Skill (80% abandon AI)
   - 06: Information Overload (the problem)
   - 08: Cognitive Limits (human-AI systems)
   - 09: Demo Personalized Summary (n8n workflow)

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
