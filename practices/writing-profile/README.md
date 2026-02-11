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

This exercise is a long conversation -- 10 questions for lite, 100 for full. What matters:

1. **Can it hold a conversation?** The AI needs to ask follow-ups, push back on vague answers, and remember what you said 20 questions ago. Search tools (Perplexity) and short-context models aren't built for this.
2. **Will it burn your credits?** A 100-question interview can take 2-3 hours. If you're on a Pro plan with a top-tier model, you'll hit rate limits fast.
3. **Can you store the result?** The profile is most useful when the AI remembers it across conversations. Some platforms support this natively, others don't.

### Recommended setup per platform

**Claude**
- **Max plan ($200/mo):** Use Opus -- unlimited, best follow-up questions
- **Pro plan ($20/mo):** Use Sonnet -- Opus will hit your rate limit after 10-15 minutes of back-and-forth, which kills the interview flow
- After the interview: save the profile in **Project Instructions** (persists across all chats in that project)

**ChatGPT Plus**
- Use the latest model (currently o3) -- it's the default, no need to change anything
- Skip "thinking mode" / extended thinking -- unnecessary for an interview and eats your quota faster
- After the interview: paste the profile into **Custom Instructions** (Settings -> Personalization)
- Don't rely on ChatGPT's "memory" feature -- it's unreliable and summarizes unpredictably

**Gemini**
- Any mode works (Fast is fine for this)
- Big context window, so even the full 100-question version won't run out of space
- After the interview: create a **Gem** (Gemini's version of a custom chatbot -- you give it instructions and it remembers them across conversations). Paste your profile as the Gem's instructions. Alternative: just paste the profile at the start of each new conversation

**Perplexity -- not recommended**
- Perplexity is a search engine that can chat, not a chat AI that can search. It's optimized for "find me an answer," not "interview me for 2 hours"
- Shorter context window, tends to lose the thread after 15-20 exchanges
- No persistent storage for the result
- Use it for research, not for this

**Bottom line:** Use whatever you already pay for. The profile itself is a text file -- once exported, it works in any AI. But for the interview itself, pick a model that can hold a long conversation without eating your quota.

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

> **Tip:** Vague answers like "I like to keep things simple" produce generic profiles. What counts: concrete examples, real pet peeves, specific words you hate. The more honest you are, the better the result.

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
1. Create a **Gem** (Settings -> Gems -> New) and paste your profile as its instructions -- it remembers across conversations
2. Or: paste the profile at the start of each new conversation

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
