# Demo Script: Personalized Summary Workflow

**Duration:** ~15 minutes (including Q&A)
**Companion:** See `n8n-workflow.md` for technical reference

---

## 1. Setup (What the Audience Sees)

### Pre-Demo Preparation

| Item | State | Notes |
|------|-------|-------|
| n8n workflow | Open in browser tab | Zoomed to fit screen |
| Notion profile DB | Second tab | One sample user profile visible |
| Sample transcript | Ready to paste | 500-800 words, meeting notes format |
| Notion output DB | Third tab | Empty or with one prior summary |
| Email client | Optional fourth tab | To show delivery if configured |

### Screen Layout

```
+------------------------+------------------------+
|                        |                        |
|   n8n Workflow         |   Notion Profile DB    |
|   (main focus)         |   (context)            |
|                        |                        |
+------------------------+------------------------+
```

### Hook Line (First 30 Seconds)

> "Every executive I know has the same problem: you leave a meeting, your notes exist somewhere, and then... nothing. They rot. This workflow turns raw meeting content into something you'd actually read — formatted the way *you* want it, focused on what *you* care about. Let me show you how it works."

---

## 2. Walkthrough (Step-by-Step)

### Step 1: Show the User Profile (~2 min)

**Switch to Notion profile tab**

> "Before the AI touches anything, it needs to know who it's working for. Here's my profile."

Point out:
- **Summary style:** "Bullets, not prose — I scan, I don't read"
- **Focus areas:** "Revenue impact, decisions needed, blockers"
- **Tone preference:** "Direct, no filler"
- **Delivery:** "Notion + email"

**The punch:** "This isn't configuration buried in code. It's a Notion database you update anytime. Change your mind? Change a field. The workflow adapts."

---

### Step 2: Trigger the Workflow (~1 min)

**Switch to n8n**

> "Watch what happens when content enters the system."

- Paste the sample transcript into the input node (or trigger webhook)
- Click **Execute Workflow**

**While running:** "Notice it's fetching my profile before doing anything else. Context first, then action."

---

### Step 3: Walk Through the Flow (~4 min)

**Move through each node as it executes:**

| Node | Say This |
|------|----------|
| **Trigger** | "This can be manual, scheduled, or fired by another system — Slack bot, email parser, whatever." |
| **Input** | "Raw content in. Could be transcript, document, email thread. Doesn't matter — text is text." |
| **Notion Get** | "Here's the magic: we fetch the user's preferences *at runtime*. Not hardcoded. Not static." |
| **Merge** | "Transcript meets preferences. This is where personalization happens — before the AI ever sees it." |
| **AI Agent** | "The prompt is *constructed*, not written. Style, focus, length — all injected from your profile." |
| **Notion Create** | "Output goes straight to your second brain. Tagged, dated, searchable." |
| **Email** | "Optional notification — because some of you live in your inbox." |

---

### Step 4: Show the Output (~2 min)

**Switch to Notion output DB**

> "Here's what just landed."

Show:
- Summary matches requested style (bullets, not paragraphs)
- Focus areas are emphasized (revenue, decisions, blockers)
- Tone matches preference
- Metadata captured (source, date, linked user)

**If time:** Open email to show parallel delivery.

---

### Step 5: Live Variation (~2 min)

> "Let's change something."

1. Switch to profile DB
2. Change one preference (e.g., "Summary style" → "Executive brief paragraph")
3. Re-run the same transcript
4. Show different output format

**The point:** "Same content, different person, different output. That's what 'personalized' actually means."

---

## 3. Key Points to Emphasize

### Why This Matters

| Point | What to Say |
|-------|-------------|
| **AI alone isn't enough** | "GPT can summarize anything. But a summary nobody reads is worthless. Personalization is the difference between 'working' and 'useful'." |
| **Separation of concerns** | "User preferences live in Notion. Workflow logic lives in n8n. AI does one job. Each piece is replaceable." |
| **No-code doesn't mean no architecture** | "This looks simple, but it's designed. The merge node isn't an accident — it's the pattern." |
| **Runtime > build time** | "Preferences aren't baked in. They're fetched fresh every execution. You can serve 50 different people with one workflow." |

### The Business Case

> "I built this in an afternoon. It runs for free on a $5 VPS. It saves me 20 minutes per meeting — times 10 meetings a week, times 50 weeks... that's 160+ hours a year. What's your hourly rate?"

---

## 4. Variations (What Else Can You Do?)

### Same Pattern, Different Inputs

| Input Source | Use Case |
|--------------|----------|
| Email forward | Auto-summarize newsletters |
| Slack message | Team update digest |
| RSS feed | Industry news briefing |
| Calendar API | Pre-meeting context prep |
| Document upload | Contract/report summary |

### Same Pattern, Different Outputs

| Output | Use Case |
|--------|----------|
| Slack DM | Real-time notification |
| Todoist/Things | Extract action items |
| CRM note | Client meeting log |
| Weekly digest | Aggregated summary email |
| Voice file (ElevenLabs) | Listen while commuting |

### Same Pattern, Different Profiles

> "You can serve a whole team with one workflow. Each person has their profile. The CEO gets strategic bullets. The PM gets action items. The analyst gets full detail."

---

## 5. Q&A Prompts (If Audience Is Quiet)

Use these to seed discussion:

1. "What content do you generate or receive that could use this treatment?"
2. "Where do summaries die in your organization right now?"
3. "What would you put in your personal profile that I didn't?"
4. "Who else on your team would need a different output format?"

---

## Backup: If n8n Fails

| Problem | Pivot |
|---------|-------|
| API timeout | Walk through the Mermaid diagram in `n8n-workflow.md`, explain each step conceptually |
| Notion auth issue | Show screenshot of expected output, focus on "why" not "how" |
| Email fails | Skip it — "Email is optional anyway, the Notion output is the core" |

---

## Timing Guide

| Section | Time |
|---------|------|
| Hook + setup context | 0:00 - 0:30 |
| Show user profile | 0:30 - 2:30 |
| Trigger workflow | 2:30 - 3:30 |
| Walk through flow | 3:30 - 7:30 |
| Show output | 7:30 - 9:30 |
| Live variation | 9:30 - 11:30 |
| Key points | 11:30 - 13:00 |
| Variations overview | 13:00 - 14:00 |
| Q&A | 14:00 - 15:00 |

---

## Presenter Notes

- **Energy:** This is a *show* — let the workflow run, let people see the magic happen
- **Pacing:** Don't rush the merge node explanation. That's where the architecture lives.
- **Audience connection:** Make eye contact when switching profiles. "What would *your* profile say?"
- **Technical questions:** Park deep n8n questions for the workshop. "Good question — let's build it together in the hands-on session."

---

*Script version: 2026-01-31*
