# Writing Profile Interview: Platform Guide

Run the 100-question interview on your preferred AI platform. Each has trade-offs.

---

## Quick Comparison

| Platform | Best For | Memory | Export | Session Limit |
|----------|----------|--------|--------|---------------|
| **Claude Pro** | Workshop default | Projects (persistent) | Copy/download | ~100K tokens |
| **ChatGPT** | Existing subscribers | Limited memory | Copy/export chat | ~128K tokens |
| **Perplexity** | Quick sessions | None | Copy only | ~32K tokens |
| **Gemini** | Google ecosystem | None | Copy only | ~1M tokens |

**Recommendation:** Claude Pro (best memory + export), ChatGPT (solid alternative).

---

## 1. Claude (claude.ai)

### Starting the Interview

**Option A: Projects (Recommended)**
1. Go to **Projects** in left sidebar
2. Create new project: "Writing Profile"
3. Paste the interview prompt into **Project Instructions**
4. Start new chat within project
5. Benefit: Prompt persists across sessions; you can continue tomorrow

**Option B: Standard Chat**
1. Start new chat
2. Paste full interview prompt
3. Begin answering questions
4. Risk: If session breaks, you lose context

### Tips
- Use **Artifacts** view to see the compiled profile as a formatted document
- If Claude generates partial profile mid-interview, ask it to continue questions
- Say "compile the profile now" when done (even before 100 questions if satisfied)

### Export
- Click the profile Artifact > **Copy** or **Download**
- Or select all text > copy to your markdown editor
- Save to: `your-repo/profiles/writing-profile.md`

### Limitations
- Long interviews may hit context limits (~100K tokens)
- If context fills: export progress, start new chat, paste "continue from Q45"
- Projects don't carry conversation history, only instructions

---

## 2. ChatGPT (chat.openai.com / mobile app)

### Starting the Interview

**Web:**
1. Click **New chat**
2. Paste interview prompt
3. Start answering

**Mobile App:**
1. Tap **+** for new chat
2. Paste prompt (or use voice input)
3. Dictate answers for faster completion

### Tips
- **Memory feature** (if enabled): ChatGPT may remember fragments, but unreliable for full profile
- Use **GPT-4o** model (default for Plus subscribers)
- Voice mode works well for answering questions naturally
- Request "create a canvas with the profile" for side-by-side editing

### Export
- Click **Share** > **Copy link** (for reference)
- Or manually copy the final profile text
- For full chat export: **Settings** > **Data controls** > **Export data** (takes hours)

### Limitations
- No persistent project memory like Claude
- Memory feature is hit-or-miss
- Long conversations may truncate older context
- Canvas not available on mobile

---

## 3. Perplexity (perplexity.ai)

### Starting the Interview

1. Start new **Thread**
2. Paste interview prompt
3. Note: Perplexity will try to search the web — tell it "this is a personal interview, no web search needed"

### Tips
- Best for quick, focused sessions
- Turn off **Pro Search** to avoid unnecessary web lookups
- Perplexity's strength (research) is irrelevant here — you're using it as a chat interface

### Export
- Copy text manually
- No native export feature
- Consider: Screenshot key sections as backup

### Limitations
- **No memory between sessions** — must complete in one sitting
- Shorter context window (~32K) — may struggle with full 100 questions
- No artifacts or side panels
- Not recommended for this exercise unless it's your only option

---

## 4. Gemini (gemini.google.com)

### Starting the Interview

1. Go to gemini.google.com
2. Start new conversation
3. Paste interview prompt
4. Select **Gemini Advanced** (1.5 Pro) for longer context

### Tips
- **Massive context window** (1M tokens) — can handle very long interviews
- Integration with Google Docs: Ask Gemini to "export to Google Docs" (hit or miss)
- Good voice input via mobile app

### Export
- Copy/paste to Google Docs or markdown file
- No direct download feature
- Use browser print-to-PDF as fallback

### Limitations
- **No memory between sessions**
- No project/folder system
- Responses can be verbose — you may need to prompt for concise output
- Formatting less reliable than Claude/ChatGPT

---

## Troubleshooting

### "The AI stopped asking questions"
Prompt: `"Continue the interview from question [X]. We have [Y] more to go."`

### "Context is getting too long"
1. Ask for current progress summary
2. Copy the compiled profile so far
3. Start new session
4. Paste: "Continue this writing profile interview. Here's progress so far: [paste profile]"

### "Answers are being summarized too much"
Prompt: `"Preserve my exact words. Don't paraphrase or summarize my answers."`

### "AI is being too polite / not pushing back"
Prompt: `"Remember: push back on vague answers. Challenge me. Don't accept surface-level responses."`

---

## Quick Start Checklist

- [ ] Choose your platform
- [ ] Start new chat/project
- [ ] Paste the interview prompt
- [ ] Block 45-60 minutes (uninterrupted)
- [ ] Answer honestly — the AI can't judge you
- [ ] Export final profile to markdown
- [ ] Save to your GitHub repo

---

## File Locations

| What | Where |
|------|-------|
| Interview prompt | `input/me-in-a-doc.md` |
| Your completed profile | `profiles/writing-profile.md` (create this) |
| This guide | `exercises/writing-profile/platform-guide.md` |

---

*Last updated: January 31, 2026*
