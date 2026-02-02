# Context Handoff

**Last updated:** 2026-02-02 (session 6)
**Project:** Feb 7 HWZ Lecture — AI Productivity Hacks for Executives

---

## Quick Context

| Field | Value |
|-------|-------|
| Lecture date | **Saturday Feb 7, 2026, 13:00-16:45** |
| Location | HWZ Zurich |
| Audience | Financial services executives (CAS AI in Finance) |
| Language | **German (Swiss orthography)** |
| Material due | Wednesday Feb 5 |
| Student email | Monday Feb 3 |

---

## Current Status

**Translations complete. Ready for Gamma slide generation.**

```
2026_02_07_AIF/segments/
├── 01-how-i-built-this-lecture/
├── 02-technology-revolution-lecture/
├── 03-writing-profile-exercise/
├── 04-ai-managerial-skill-lecture/
├── 05-company-research-exercise/
├── 06-information-overload-lecture/
├── 07-second-brain-exercise/
├── 08-cognitive-limits-lecture/
└── 09-demo-personalized-summary-lecture/
```

---

## Session 6 Changes (Feb 2)

- ✅ Fixed Wispr Flow URL: `wispr.ai` → `wisprflow.ai` in READMEs
- ✅ Added OpenClaw (experimental) to READMEs
- ✅ Updated `auto-push-project.de.md`: Sie → du form
- ✅ Clarified DB ID workflow: Claude creates DB, user copies ID to project prompt
- ✅ Added Gamma MCP to `.mcp.json`
- ✅ Updated tech stack: Added Optiverse, fixed Google IDX → Google Anti-Gravity

---

## Outstanding Tasks

### 1. Validate Gamma prompts
- Test each `gamma-prompt.md` in Gamma.app (or use Gamma MCP)
- Verify slide generation works correctly
- Fix any prompt issues

### 2. Generate slide decks
- Run validated gamma-prompts through Gamma
- Export as PDF or PPTX
- Store in each segment folder

### 3. Student prereq email
- Draft email with prereqs (GitHub, Notion, Claude Pro accounts)
- Send by Monday Feb 3
- Template exists at `templates/prereqs-email-template.md`

### 4. Package materials for HWZ
- Compile final materials
- Send by Wednesday Feb 5

---

## MCP Servers Available

| Server | Purpose |
|--------|---------|
| `n8n-mcp` | Workflow automation |
| `gamma-mcp` | Slide generation via API |

---

## Translation Guidelines

**Swiss German orthography rules:**
- No ß — always use "ss" (Strasse, nicht Straße)
- Standard Hochdeutsch vocabulary and grammar
- **Informal register (du)** for exercise instructions
- Keep technical terms in English where appropriate (AI, GitHub, Notion)
- Audience: senior executives in finance

---

## Gamma Prompt Workflow

**Option 1: Manual (Gamma.app)**
1. Open [gamma.app](https://gamma.app)
2. Click "Create" → "Paste in text"
3. Copy entire content of `gamma-prompt.md`
4. Paste and generate

**Option 2: Via MCP (Claude Code)**
1. Use `generate_gamma` tool with inputText from gamma-prompt.md
2. Poll with `get_gamma_generation` for completion
3. Export URLs returned automatically

---

## Files by Segment

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

## Resume Instructions

1. Generate slides using Gamma (manual or MCP)
2. Draft student prereq email
3. Test exercise workflows end-to-end
4. Package and send to HWZ by Feb 5

---

## Timeline

- ✅ Jan 31: Content built (English)
- ✅ Feb 1: Folder restructure + ZFU cleanup
- ✅ Feb 1: German translations (complete)
- ✅ Feb 2: Fixes (URLs, tech stack, du-form)
- ⏳ Feb 2-3: Gamma slide generation
- ⏳ Feb 3: Student email sent
- ⏳ Feb 5: Materials to HWZ
- ⏳ Feb 7: Lecture delivery
