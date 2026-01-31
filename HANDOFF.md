# Context Handoff

**Last updated:** 2026-01-31 (evening session 2)
**Session:** Lecture structure decision made

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

## NEW Lecture Structure (Decided This Session)

**Thesis:** Hybrid approach — teaching + exercises with reusable deliverables

| Block | Content | Deliverable |
|-------|---------|-------------|
| **Opening** | AI for productivity & value | Context setting |
| **Writing Profile** | Ruben Hassid LITE (shortened, not 100 questions) | Reusable profile for all AI work |
| **Company Research** | Prompts: Research → Golden Circle → BMC → VPC | Analysis framework (self or customer) |
| **Second Brain** | Claude/Perplexity → Notion push | Working knowledge capture system |

### Key Design Decisions

1. **Writing Profile exercise needs LITE version** — full Ruben Hassid is 100 questions (2+ hours). Create shortened version in `exercises/` folder with full version as optional.

2. **Company Research sequence:** Golden Circle → Business Model Canvas → Value Proposition Canvas (in that order)

3. **Second Brain simplified:** Just Claude project or Perplexity project → push to Notion database. No GitHub infrastructure.

4. **VALIDATE: Perplexity → Notion native write** — User claims they just built a Notion database from Perplexity. If true, this changes tool recommendation. Need to verify workflow.

---

## Reference: 2025 Lecture Structure

From `2025-04_AIF/2025 04 12 AI Productivity Hacks for Leaders.pdf`:

| Time | Type | Content |
|------|------|---------|
| 13:30 | Lecture | Welcome, Galloway quote, About me |
| 13:45 | Lecture | Confidential and Sovereign AI |
| 14:00 | Lecture | AI toolbox, Maturity model |
| 14:30 | Break | |
| 14:45 | Exercise | Golden Circle → HeyGen script |
| 15:15 | Exercise | HeyGen video creation |
| 15:45 | Break | |
| 16:00 | Exercise | Managing emotions with AI |
| 16:15 | Exercise | Boss email triage |
| 16:45 | Closing | 3 Superpowers |

**Ratio:** ~60min lecture / ~105min exercises / ~30min breaks

---

## This Session Completed

- [x] Renamed folder to `2026_02_07_AIF`
- [x] Created German README.md (primary) + English README.en.md
- [x] Moved brainstorm out of HWZ briefing (now public)
- [x] Renamed `HWZ briefing/` → `docs.gitignore/` (private)
- [x] Added `2026-02_ZFU/` to gitignore (separate project)
- [x] Analyzed 2025 lecture structure
- [x] Decided new lecture structure (hybrid approach)
- [x] Committed and pushed to GitHub

---

## Outstanding Tasks

### Immediate (before Monday Feb 3)
- [ ] **Validate Perplexity → Notion write** — user says it works natively now
- [ ] Update prereqs email based on tool validation
- [ ] Send prereq email to students

### Before Wednesday Feb 5
- [ ] Create `exercises/` folder structure
- [ ] Build Ruben Hassid LITE exercise
- [ ] Build Company Research prompts (Golden Circle, BMC, VPC)
- [ ] Build Second Brain setup guide
- [ ] Create Gamma slides for lecture

### Tool Validation Needed

| Platform | Read Notion | Write Notion | Status |
|----------|-------------|--------------|--------|
| Claude Pro | Yes | Yes (native) | Confirmed |
| Perplexity Pro | Yes | **NEEDS VALIDATION** | User claims native works |

---

## Key Files

| File | Purpose |
|------|---------|
| `2026_02_07_AIF/README.md` | German participant cookbook |
| `2026_02_07_AIF/README.en.md` | English version |
| `2026_02_07_AIF/AI Productivity Hacks for Executives Barainstorm.md` | Original brainstorm (public) |
| `2026_02_07_AIF/docs.gitignore/` | Private files (student list, schedule) |
| `2025-04_AIF/2025 04 12 AI Productivity Hacks for Leaders.pdf` | Reference: last year's slides |

---

## Resume Instructions

**Next session goal:** Build lecture content

1. Read this HANDOFF.md
2. **First:** Validate Perplexity → Notion write capability with user
3. Create `exercises/` folder with:
   - `writing-profile-lite.md`
   - `writing-profile-full.md` (optional)
   - `company-research.md`
   - `second-brain-setup.md`
4. Create `prompts/` folder with reusable prompts
5. Update README files with correct prereqs based on validation

**Timeline:**
- Monday Feb 3: Student prereq email
- Wednesday Feb 5: Materials to HWZ
- Saturday Feb 7: Lecture delivery
