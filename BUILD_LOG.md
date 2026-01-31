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
   - Still pending: `2026 02 07 AIF`, `2026 Sovereignty`

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
