# Context Handoff

**Last updated:** 2026-01-31
**Session:** Repository initialization and structure setup

---

## Current State

### Repository
- **GitHub:** https://github.com/thwinter-ch/ai-lectures
- **Local:** `c:\Users\tw\My Drive\BlizzardVentures\edu\AI lectures`
- **Branch:** `master`
- **Status:** Clean, 2 commits pushed

### Structure
```
ai-lectures/
├── .gitignore              # Privacy patterns configured
├── README.md               # Overview + prerequisites
├── BUILD_LOG.md            # This session's work documented
├── HANDOFF.md              # This file
├── modules/                # Reusable content blocks
│   └── governance-frameworks/  # House model, board questions
├── templates/              # Email templates (DE/EN)
├── lectures/               # Empty - for future lectures
├── 2025-04_AIF/           # Past lecture
├── 2025_12_HWZ_CAS_VR/    # Past lecture (summaries moved to docs.gitignore/)
├── 2026 02 07 AIF/        # NEEDS RENAME → 2026-02_AIF
├── 2026 Sovereignty/      # NEEDS RENAME → 2026_Sovereignty
└── 2026-02_ZFU/           # Current project brief
```

---

## Immediate Next Steps

### 1. Build HWZ CAS Lecture
**Priority:** High — Monday deadline for participant emails

Location: Create new folder `lectures/2026-XX_HWZ_CAS/` (get exact date)

Tasks:
- [ ] Get lecture date and create folder
- [ ] Define learning objectives
- [ ] Assemble content from modules
- [ ] Create participant exercises
- [ ] Prepare slides or outline

### 2. Participant Email System
**Priority:** High — needed before lecture

Tasks:
- [ ] Get participant list (CSV format)
- [ ] Set up n8n workflow OR simple script
- [ ] Send prerequisite emails (GitHub account, Claude Pro)

### 3. Folder Renames (Low Priority)
When Google Drive sync allows:
```bash
cd "c:\Users\tw\My Drive\BlizzardVentures\edu\AI lectures"
mv "2026 02 07 AIF" "2026-02_AIF"
mv "2026 Sovereignty" "2026_Sovereignty"
git add -A && git commit -m "Rename remaining folders"
git push
```

---

## Key Files to Read

| File | Purpose |
|------|---------|
| [BUILD_LOG.md](BUILD_LOG.md) | Session work documentation |
| [README.md](README.md) | Repo overview, participant prereqs |
| [templates/prereqs-email-template.md](templates/prereqs-email-template.md) | Email templates |
| [modules/governance-frameworks/](modules/governance-frameworks/) | Reusable frameworks |
| [2026-02_ZFU/ZFU_Project_Brief.md](2026-02_ZFU/ZFU_Project_Brief.md) | Seminar teasers, context |

---

## Conventions

| Item | Convention |
|------|------------|
| Lecture folders | `YYYY-MM_INSTITUTION_TOPIC` |
| Private content | Always in `docs.gitignore/` subfolder |
| Build logs | Update `BUILD_LOG.md` after each session |
| Modules | `kebab-case` names |

---

## Resume Instructions

**User intent:** Use GSD workflow to plan and build the HWZ CAS lecture.

Start next session with:
```
/gsd:new-project
```

Or if continuing existing work:
```
/gsd:progress
```

### Info to gather at start:
- Lecture date
- Topic/focus
- Participant list (for docs.gitignore/)
- Duration (half-day, full-day, etc.)

---

## Plan File Reference

Full planning context saved at:
`C:\Users\tw\.claude\plans\lazy-squishing-hejlsberg.md`
