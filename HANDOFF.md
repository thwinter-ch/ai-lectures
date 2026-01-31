# Context Handoff

**Last updated:** 2026-01-31 (evening session 4)
**Session:** Lecture content build — COMPLETE

---

## Lecture Details

| Field | Value |
|-------|-------|
| Date | **Saturday Feb 7, 2026** |
| Time | 13:00 - 16:45 (3.75 hours) |
| Audience | Financial services executives (CAS AI in Finance) |
| Location | HWZ, Zurich |
| Second session | **Saturday Apr 25, 2026** — "AI und Deep Tech Future Outlook" |
| Material due | Wednesday Feb 5 |
| Student email | Monday Feb 3 |

---

## Current Status: 100% Content Complete

**All lecture segments and exercises built.** Pending: folder structure decision + final README update.

### Slides (6 segments)

| Segment | Status | Files |
|---------|--------|-------|
| 01 - How I Built This | ✅ Complete | `script.md`, `gamma-prompt.md`, `tech-stack.md` |
| 02 - Technology Revolution | ✅ Complete | `script.md`, `gamma-prompt.md` |
| 03 - AI Managerial Skill | ✅ Complete | `script.md`, `gamma-prompt.md` |
| 04 - Information Overload | ✅ Complete | `script.md`, `gamma-prompt.md` |
| 05 - Cognitive Limits | ✅ Complete | `script.md`, `gamma-prompt.md` |
| 06 - Demo: Personalized Summary | ✅ Complete | `script.md`, `gamma-prompt.md`, `n8n-workflow.md` |

### Exercises (3 exercises)

| Exercise | Status | Files |
|----------|--------|-------|
| Writing Profile | ✅ Complete | `lite-interview.md`, `bridge-to-full.md`, `platform-guide.md`, `question-analysis.md`, `README.md` |
| Company Research | ✅ Complete | `01-deep-research.md`, `02-strategy-synthesis.md`, `README.md` |
| Second Brain | ✅ Complete | `claude-notion-setup.md`, `auto-push-project.md`, `README.md` |
| Exercises Index | ✅ Complete | `exercises/README.md` |

---

## Video Sources (Correct URLs)

Both videos are from **Nate B Jones** (AI News & Strategy Daily):

### Segment 02: Technology Revolution
- **URL:** `https://www.youtube.com/watch?v=LwKnvqVdUgA`
- **Title:** "The Skill Gap That Will Separate AI Winners from Everyone Else"
- **Thesis:** 2026 = breakthrough for personal AI agents. Technical pieces exist (MCP, skills, browser use). Missing: UX layer + task formulation skills. You need to be organized to delegate.

### Segment 03: AI as Managerial Skill
- **URL:** `https://www.youtube.com/watch?v=EZ4EjJ0iDDQ`
- **Title:** "Why Your Best Employees Quit Using AI After 3 Weeks"
- **Thesis:** 80% abandon AI tools. Success requires management skills, not prompting. BCG/Harvard jagged frontier. Centaurs vs Cyborgs. Six 201-level skills.

---

## YouTube Extraction Skill Created

**Location:** `C:/Users/tw/.claude/skills/youtube-extraction/skill.md`

**Key findings:**
- `google/gemini-2.5-flash` does NOT reliably process videos (hallucinated wrong content)
- `google/gemini-2.0-flash-001` works but ALSO hallucinated on these specific videos
- For these videos, manual extraction from YouTube page (title, description, chapters) was more reliable

**Skill documents the API pattern but notes reliability issues.**

---

## Resume Instructions

### If agents completed:
1. Check files exist:
   - `slides/02-technology-revolution/script.md`
   - `slides/02-technology-revolution/gamma-prompt.md`
   - `slides/03-ai-managerial-skill/script.md`
   - `slides/03-ai-managerial-skill/gamma-prompt.md`

2. If all files exist → Update main READMEs (Wave 3)
3. Commit and push

### If agents still running or failed:
1. Check with: `Glob 2026_02_07_AIF/slides/**/*.md`
2. Re-run agents for missing segments using the video content above
3. Agents need explicit absolute paths to write files

### Final integration (Wave 3):
- Update `2026_02_07_AIF/README.md` with complete structure
- Update `2026_02_07_AIF/README.en.md` with English version
- Commit all changes

---

## Key Learnings This Session

### What Fixed the Agent Failures:
1. **Create folders first** — Agents failed silently when target folders didn't exist
2. **Explicit absolute paths** — Full paths in prompts, not relative
3. **Clear deliverable specs** — Tell agent exactly what files to create

### YouTube Extraction:
- Gemini via OpenRouter CAN process YouTube but hallucinated on these specific videos
- Model `google/gemini-2.0-flash-001` is more reliable than `gemini-2.5-flash`
- Sometimes manual extraction (title + description + chapters) is more reliable than AI extraction

---

## File Structure (Current)

```
2026_02_07_AIF/
├── input/
│   ├── me-in-a-doc.md          # Full 100-question interview prompt
│   ├── company-research.md      # Deep research prompt
│   └── GC-BMC-VPC.md           # Strategy synthesis prompt
│
├── slides/
│   ├── 01-how-i-built-this/
│   │   ├── tech-stack.md       ✅
│   │   ├── script.md           ✅
│   │   └── gamma-prompt.md     ✅
│   ├── 02-technology-revolution/
│   │   ├── script.md           ✅
│   │   └── gamma-prompt.md     ✅
│   ├── 03-ai-managerial-skill/
│   │   ├── script.md           ✅
│   │   └── gamma-prompt.md     ✅
│   ├── 04-information-overload/
│   │   ├── script.md           ✅
│   │   └── gamma-prompt.md     ✅
│   ├── 05-cognitive-limits/
│   │   ├── script.md           ✅
│   │   └── gamma-prompt.md     ✅
│   └── 06-demo-personalized-summary/
│       ├── script.md           ✅
│       ├── gamma-prompt.md     ✅
│       └── n8n-workflow.md     ✅
│
├── exercises/
│   ├── README.md               ✅ Index
│   ├── writing-profile/
│   │   ├── README.md           ✅
│   │   ├── lite-interview.md   ✅
│   │   ├── bridge-to-full.md   ✅
│   │   ├── platform-guide.md   ✅
│   │   └── question-analysis.md ✅
│   ├── company-research/
│   │   ├── README.md           ✅
│   │   ├── 01-deep-research.md ✅
│   │   └── 02-strategy-synthesis.md ✅
│   └── second-brain/
│       ├── README.md           ✅
│       ├── claude-notion-setup.md ✅
│       └── auto-push-project.md ✅
│
├── README.md                    # German (needs update)
├── README.en.md                 # English (needs update)
└── .env.local                   # OpenRouter API key (gitignored)
```

---

## Outstanding Tasks

1. **Verify segments 02 + 03 complete** — Check agent output files exist
2. **Decide folder structure** — See "Pending Decision" below
3. **Review content quality** — Spot check a few files
4. **Commit and push** — All changes to GitHub

---

## Pending Decision: Folder Structure

Current structure separates `slides/` (lectures) and `exercises/`. User questioned if this is clear.

**Options:**

**A) Unified segments with type labels:**
```
segments/
├── 01-how-i-built-this-lecture/
├── 02-technology-revolution-lecture/
├── 03-writing-profile-exercise/
├── 04-ai-managerial-skill-lecture/
├── 05-company-research-exercise/
├── 06-information-overload-lecture/
├── 07-second-brain-exercise/
├── 08-cognitive-limits-lecture/
├── 09-demo-personalized-summary-lecture/
```

**B) Keep separate, just rename `slides/` → `lectures/`**

**C) Keep current structure** (slides + exercises separate)

Decision needed before finalizing READMEs.

---

## Fixes Applied This Session

- ✅ Fixed Perplexity/Notion claim in both READMEs — Perplexity Pro now shown as native Notion write capable

---

## Timeline

- ✅ Friday Jan 31: Lecture content built
- Monday Feb 3: Student prereq email
- Wednesday Feb 5: Materials to HWZ
- Saturday Feb 7: Lecture delivery
