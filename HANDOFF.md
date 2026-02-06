# Context Handoff

**Last updated:** 2026-02-06 (session 7)
**Project:** Feb 7 HWZ Lecture — AI Productivity Hacks for Executives

---

## Quick Context

| Field | Value |
|-------|-------|
| Lecture date | **Saturday Feb 7, 2026, 13:00-16:45** |
| Location | HWZ Zurich |
| Audience | Financial services executives (CAS AI in Finance) |
| Language | **German (Swiss orthography)** |
| Student email | Sent |
| Materials | Link to repo shared |

---

## Current Status

**Segment 01 script + gamma prompt updated. Ready for Gamma MCP test.**

**Directory restructured:**
```
2026_02_07_AIF/
├── segments-de/          ← PRIMARY (lecture is in German)
│   ├── 01-how-i-built-this-lecture/       ✅ UPDATED
│   ├── 02-technology-revolution-lecture/   ⏳ reviewed, needs walk-through
│   ├── 03-writing-profile-exercise/       ⏳ pending
│   ├── 04-ai-managerial-skill-lecture/    ⏳ pending
│   ├── 05-company-research-exercise/      ⏳ pending
│   ├── 06-information-overload-lecture/   ⏳ pending
│   ├── 07-second-brain-exercise/          ⏳ pending
│   ├── 08-cognitive-limits-lecture/       ⏳ pending
│   └── 09-demo-personalized-summary-lecture/ ⏳ pending
├── segments-en/          ← English mirror (same structure)
```

Old `segments/` directory has been DELETED.

---

## Session 7 Changes (Feb 6)

- ✅ Restructured: `segments/` → `segments-de/` + `segments-en/` (25 files each)
- ✅ Deleted old `segments/` directory
- ✅ Segment 01 script rewritten with user input:
  - Removed Notion from stack (wasn't used)
  - Added "arguing with Claude" section (new employee analogy)
  - Added girlfriend/design school anecdote
  - Replaced "draft 7 vs 1" with Ovomaltine analogy
  - Timeline updated to match BUILD_LOG
  - Fixed transition (was pointing to segment 06, now points to 02)
- ✅ Segment 01 gamma prompt updated to match new script

---

## Next Steps (Resume Here)

### Immediate: Test Gamma MCP
1. Fire `generate_gamma` with segment 01 DE gamma-prompt.md content
2. Settings: format=presentation, textMode=preserve, language=de, numCards=10, cardOptions.dimensions=16x9, textOptions.amount=brief
3. Review output, adjust prompt if needed
4. Once pattern works → replicate for segments 02, 04, 06, 08, 09

### Then: Walk Through Remaining Segments
For each segment (02–09):
1. Read DE script in plain language — what are you saying on stage?
2. User says what works, what doesn't, what to change
3. Update script + gamma prompt
4. Generate slides

### Also Needed
- Exercise segments (03, 05, 07): make idiot-proof, consider email handout
- Check all segment transitions point to correct next segment
- Sovereignty content (`2026 Sovereignty/`) — possible caveat slide

---

## Segment Overview (9 segments, 3h 45m)

| # | Segment | Type | Duration | Slides Needed |
|---|---------|------|----------|---------------|
| 01 | How I Built This | Lecture | 15 min | Yes (gamma ready) |
| 02 | Technology Revolution | Lecture | 15 min | Yes |
| 03 | Writing Profile | Exercise | ~20 min | No |
| 04 | AI as Managerial Skill | Lecture | 15 min | Yes |
| 05 | Company Research | Exercise | ~25 min | No |
| 06 | Information Overload | Lecture | 15 min | Yes |
| 07 | Second Brain | Exercise | ~25 min | No |
| 08 | Cognitive Limits | Lecture | 15 min | Yes |
| 09 | Demo: Personalized Summary | Demo | 15 min | Yes |

---

## Translation Guidelines

**Swiss German orthography rules:**
- No ß — always use "ss" (Strasse, nicht Straße)
- Standard Hochdeutsch vocabulary and grammar
- **Informal register (du)** for exercise instructions
- **Formal register (Sie)** for lecture scripts
- Keep technical terms in English where appropriate (AI, GitHub, Notion)
- Audience: senior executives in finance

---

## Gamma MCP Settings (Tested Pattern)

```
format: presentation
textMode: preserve
numCards: 10
textOptions.language: de
textOptions.audience: Financial services executives
textOptions.amount: brief
cardOptions.dimensions: 16x9
imageOptions.source: aiGenerated
exportAs: pptx
```

---

## Files by Segment (in segments-de/)

| Segment | Files |
|---------|-------|
| 01-how-i-built-this | script.md, gamma-prompt.md, tech-stack.md |
| 02-technology-revolution | script.md, gamma-prompt.md |
| 03-writing-profile | README.md, lite-interview.md, bridge-to-full.md, platform-guide.md, question-analysis.md |
| 04-ai-managerial-skill | script.md, gamma-prompt.md |
| 05-company-research | README.md, 01-deep-research.md, 02-strategy-synthesis.md |
| 06-information-overload | script.md, gamma-prompt.md |
| 07-second-brain | README.md, claude-notion-setup.md, auto-push-project.md |
| 08-cognitive-limits | script.md, gamma-prompt.md |
| 09-demo-personalized-summary | script.md, gamma-prompt.md, n8n-workflow.md |

---

## MCP Servers Available

| Server | Purpose |
|--------|---------|
| `gamma-mcp` | Slide generation via API |
| `n8n-mcp` | Workflow automation |
| `notion` | Notion pages, databases |
| `perplexity` | Web search / research |
| `playwright` | Browser automation |
| `typefully` | Social media drafts |
