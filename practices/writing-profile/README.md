# Writing Profile (Schreibprofil)

**Duration:** 20 min (lite) | 2-3 hours (full)
**Tools:** Claude Pro, ChatGPT Plus, Gemini -- any AI that can hold a conversation
**Deliverable:** A voice profile document that teaches any AI how you write
**Status:** proven
**Used in:** 2026_02_07_AIF, 2026_02_14_Chicks_AI

---

## What this is

An AI interviews you about your writing style. At the end, you have a document -- your voice profile -- that you can feed to any AI so it writes like you.

**Why this matters:** Without a profile, every AI conversation starts from zero. You explain your tone, your preferences, your pet peeves -- again and again. The profile makes that knowledge **portable**:

- Switch from Claude to ChatGPT? Paste the profile.
- New AI tool launches next month? Paste the profile.
- Hand off writing to a colleague or freelancer? Give them the profile.

Your voice is not locked into one platform. The profile is a `.md` file that works everywhere.

---

## Which version to do

| Level | Time | File | When to use |
|-------|------|------|-------------|
| **Lite** | 20 min | [lite-interview.md](lite-interview.md) | **Start here.** 10 questions, ~70% of the signal. Enough for most people. |
| **Bridge** | +90 min | [bridge-to-full.md](bridge-to-full.md) | You already did lite and want to go deeper. Adds ~90 questions without repeating. |
| **Full** | 2-3 hours | [full-interview.md](full-interview.md) | Skip lite, do 100 questions from scratch. Only if you want a fresh start. |

**Always start with lite.** You can upgrade later -- nothing is lost.

---

## Which AI to use

| Platform | Recommended? | Session persistence | Notes |
|----------|-------------|-------------------|-------|
| **Claude Pro** | Best | Projects (persistent instructions) | Profile goes into Project Instructions -- persists across chats |
| **ChatGPT Plus** | Good | Custom Instructions / GPT memory | Use Custom Instructions, not memory (memory is unreliable) |
| **Gemini** | Works | None | Big context window, but no persistent storage |
| **Perplexity** | Not ideal | None | Designed for search, not interviews |

**Bottom line:** Use whatever you already pay for. The profile itself is a text file -- once exported, it works in any AI.

---

## How to do it

1. Pick your version from the table above
2. Open the prompt file
3. Copy the **entire** prompt
4. Open a new conversation in your AI of choice
5. Paste the prompt and press Enter
6. Answer the questions one at a time -- be honest and specific
7. The AI generates your voice profile at the end
8. Save it (see below)

> **Tipp:** Vage Antworten wie "Ich halte es gerne einfach" produzieren generische Profile. Was zahlt: konkrete Beispiele, echte Argernisse, spezifische Worter die du hasst. Je ehrlicher, desto besser das Ergebnis.

---

## What to do with your profile

### Save it

1. Copy the entire profile text the AI generates
2. Save as `stimmprofil.md` (or whatever name you prefer)
3. This file is your portable voice -- keep it somewhere you can find it

### Make it persistent (so the AI remembers)

**Claude Pro:**
1. Go to **Projects** -> create a project (e.g., "Mein Schreibstil")
2. Open **Project Instructions**
3. Paste your entire voice profile there
4. Every conversation in this project now knows your style

**ChatGPT Plus:**
1. Go to **Settings** -> **Personalization** -> **Custom Instructions**
2. Paste your profile in the "How would you like ChatGPT to respond?" field
3. Or: create a GPT with the profile as its instructions

**Gemini:**
1. No persistent storage -- paste the profile at the start of each conversation
2. Or: create a Gem with the profile as its instructions

**Any other AI:**
1. Paste the profile at the beginning of your conversation
2. Say: "This is my writing style. Use it for everything you write for me."

### Use it across AIs

This is the portability point: the same `.md` file works in Claude, ChatGPT, Gemini, or whatever comes next. You are not locked in. When you switch tools, your voice goes with you.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| AI stopped asking questions | Say: "Setze das Interview ab Frage [X] fort." |
| Context window too long | Export progress, start new chat, paste: "Setze fort. Bisheriger Stand: [profile]" |
| Answers get summarized | Say: "Bewahre meine exakten Worte. Nicht paraphrasieren." |
| AI is too polite / doesn't push back | Say: "Hake bei vagen Antworten nach. Fordere mich heraus." |
| Profile feels generic | Your answers were probably too vague. Redo the questions where you gave "I like to keep it simple" type answers. Give concrete examples instead. |
