# Context Handoff

**Last updated:** 2026-01-31 (evening)
**Session:** Cleanup complete, ready for GSD project init

---

## Lecture Details (Gathered This Session)

### AI Productivity Hacks for Executives

| Field | Value |
|-------|-------|
| Date | **Saturday Feb 8, 2026** (confirm — user said "Saturday Feb 7" but Feb 7 is Friday) |
| Duration | 4 hours |
| Audience | Financial services executives (AIF program) |
| Location | HWZ / Financial Institution, Switzerland |
| Material due | Wednesday Feb 5 |
| Student email | Monday Feb 3 |

### Brainstorm Document

**Location:** `2026 02 07 AIF/HWZ briefing/AI Productivity Hacks for Executives Barainstorm.md`

**Origin:** Perplexity AI voice conversation (Jan 24) using Wispr Flow — the process itself demonstrates the lecture content.

### Module Structure (from brainstorm)

1. The Productivity Architecture (45 min)
2. Setting Up GitHub Knowledge Base (60 min)
3. Ruben Hassid Exercise — Writing Style Profile (45 min)
4. Building Second Brain in Notion (60 min)
5. Company Research & Analysis Frameworks (60 min)
6. Voice Capture with Wispr Flow (30 min)
7. Advanced Workflows (Optional, 20 min)
8. Wrap-up (20 min)

### Participant Deliverables

1. GitHub repository with knowledge base
2. Notion database as second brain
3. Personalized writing style profile (markdown)
4. Company research document with frameworks
5. Working integrations (GitHub, Notion, AI platform)
6. Master prompts for knowledge management

---

## Critical Finding: Notion Integration

**Validated 2026-01-31:**

| Platform | Read Notion | Write Notion | Setup |
|----------|-------------|--------------|-------|
| **Claude Pro** | ✓ | ✓ | Simple (Notion MCP one-click) |
| ChatGPT Plus | ✓ (extensions) | ❌ native | Complex (custom GPT + API) |
| Perplexity Pro | ✓ | ❌ native | Complex (requires Make/Zapier) |

**Conclusion:** The brainstorm doc incorrectly recommended Perplexity. **Claude Pro ($20/mo) is the only platform with native web-based write capability to Notion.**

**Prereq change:** Claude Pro is now the PRIMARY requirement for hands-on exercises.

---

## Current State

### Repository
- **GitHub:** https://github.com/thwinter-ch/ai-lectures
- **Local:** `c:\Users\tw\My Drive\BlizzardVentures\edu\AI lectures`
- **Branch:** `master`
- **Status:** Clean, pushed

### This Session Completed
- [x] Archived 2025 lectures (gitignored, removed from tracking)
- [x] Clarified naming convention (dash for date, underscore for parts)
- [x] Validated Notion write capabilities (Claude Pro wins)
- [x] Documented brainstorm origin in BUILD_LOG.md
- [ ] Folder renames still blocked by Google Drive

### Outstanding Questions (Ask User)
1. **Date confirmation:** Feb 7 (Friday) or Feb 8 (Saturday)?
2. **Participant list:** Do you have it? Needed for Monday email
3. **Material format:** What does HWZ expect by Feb 5?

---

## Key Files

| File | Purpose |
|------|---------|
| `BUILD_LOG.md` | Full session documentation + Notion validation |
| `2026 02 07 AIF/HWZ briefing/AI Productivity Hacks for Executives Barainstorm.md` | Comprehensive lecture brainstorm |
| `templates/prereqs-email-template.md` | Email templates (needs update for Claude Pro) |

---

## Conventions

| Item | Convention | Example |
|------|------------|---------|
| Lecture folders | `YYYY-MM_INSTITUTION_TOPIC` | `2026-02_AIF` |
| Date separator | dash `-` | `2026-02` |
| Part separator | underscore `_` | `HWZ_CAS_VR` |
| Private content | `docs.gitignore/` subfolder | |

---

## Resume Instructions

**Next session goal:** Initialize GSD project for the lecture build.

```
/gsd:new-project
```

**Context to provide:**
- Read this HANDOFF.md
- Read the brainstorm doc at `2026 02 07 AIF/HWZ briefing/AI Productivity Hacks for Executives Barainstorm.md`
- Answer the 3 outstanding questions (date, participant list, material format)

**Timeline:**
- Monday Feb 3: Student prereq email
- Wednesday Feb 5: Materials to HWZ
- Saturday Feb 8: Lecture delivery (pending date confirmation)
