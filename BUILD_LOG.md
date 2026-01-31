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

3. **Created module structure:**
   ```
   modules/
   ├── governance-frameworks/
   │   ├── house-model/        # Tech investment validation
   │   └── board-questions/    # Armour-piercing questions
   ├── ai-governance/          # Placeholder
   ├── hands-on-tools/         # Placeholder
   └── prompting-basics/       # Placeholder
   ```

4. **Created templates:**
   - `templates/prereqs-email-template.md` — DE/EN email for participant preparation

5. **Renamed folders** (partial — Drive sync blocked some):
   - `2025 04 12 AIF` → `2025-04_AIF`
   - `2026 02 ZFU` → `2026-02_ZFU`
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

- [ ] Validate Notion write capabilities for ChatGPT/Claude/Perplexity
- [ ] Confirm lecture date (Feb 7 vs Feb 8)
- [ ] Get participant list
- [ ] Build lecture content via GSD workflow

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
