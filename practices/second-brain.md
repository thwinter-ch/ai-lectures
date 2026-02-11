# Second Brain: Claude + Notion

**Duration:** 25 min (setup) + ongoing use
**Tools:** Claude Pro/Max + Notion
**Deliverable:** Auto-capture system that saves Claude conversations to Notion
**Status:** proven
**Used in:** 2026_02_07_AIF, 2026_02_10_Biedermann

Your external memory. Every conversation with Claude can become a searchable, tagged knowledge asset in Notion -- no copy-paste, no friction.

**First time?** See [second-brain-setup.md](second-brain-setup.md) to connect Claude to Notion (~15 minutes, one-time).

**Already set up?** This page is your reference for how to use it.

---

## How It Works

```mermaid
flowchart LR
    CONV[Conversations] -->|"save this"| CAPTURE[Capture]
    CAPTURE --> NOTION[(Notion DB)]
    NOTION --> REVIEW[Review Cycles\nWeekly · Monthly · Quarterly]
    REVIEW --> INSIGHTS[Insights &\nPatterns]
    INSIGHTS --> RETRIEVE[Retrieve\non demand]
    RETRIEVE --> CONV

    style NOTION fill:#4a90d9,stroke:#fff,color:#fff
    style REVIEW fill:#2ea043,stroke:#fff,color:#fff
    style RETRIEVE fill:#d29922,stroke:#fff,color:#fff
    style CAPTURE fill:#8b5cf6,stroke:#fff,color:#fff
    style CONV fill:#333,stroke:#fff,color:#fff
    style INSIGHTS fill:#e05d44,stroke:#fff,color:#fff
```

The loop: you have conversations, capture the valuable parts to Notion, review them on a regular cadence, and retrieve your own knowledge when you need it. Each cycle makes the next conversation smarter.

---

## Quick Reference Card

```
┌──────────────────────────────────────────────────────────────┐
│  SECOND BRAIN: CLAUDE + NOTION                               │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  REVIEW CYCLES                                               │
│  Weekly (15 min)  →  top insights, patterns, open threads    │
│  Monthly (30 min)  →  themes, gaps, action item audit        │
│  Quarterly (60 min)  →  evolution, connections, strategy     │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  RETRIEVAL                                                   │
│  "What do I know about [topic]?"                             │
│  "Before I decide on [X], what have I learned?"              │
│  "Prepare me for a meeting about [topic]"                    │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  CAPTURE                                                     │
│  "save this" / "capture this" / "push to Notion"            │
│  "end session"  →  summarize + push + confirm                │
│  "what's worth capturing?"  →  Claude proposes               │
│  "push [specific thing]"  →  targeted capture                │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  MODES                                                       │
│  "research mode"  →  capture more, consolidate at end        │
│  "meeting mode: [name]"  →  decisions + action items only    │
│  "brainstorm mode"  →  lower bar, include speculative ideas  │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  CONFIDENCE LEVELS                                           │
│  High  =  verified, well-reasoned                            │
│  Medium  =  plausible, needs validation                      │
│  Speculative  =  hypothesis, early thinking                  │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│  IMPORTANT: Always start conversations from inside           │
│  the Second Brain project, not from a regular chat.          │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## Review Cycles

The capture side runs itself. The review side is where the value compounds. Without reviews, your second brain becomes a graveyard of good ideas.

### Weekly Review (~15 min, every Friday or Monday)

```
Weekly review: Look through my Notion second brain entries from the past 7 days.

Give me:
1. **What I learned** -- the 3-5 most valuable insights added this week
2. **Patterns** -- anything that connects across multiple entries
3. **Open threads** -- speculative ideas or action items that deserve follow-up
4. **One surprise** -- something I captured that I've probably already forgotten

Keep it to one page. No fluff.
```

### Monthly Review (~30 min, first week of each month)

```
Monthly review: Analyze my Notion second brain entries from the past 30 days.

Give me:
1. **Theme of the month** -- what topic or question dominated my thinking?
2. **Top 5 insights** -- the entries with the highest lasting value
3. **Confidence shifts** -- anything I marked "Speculative" that now looks confirmed (or dead)?
4. **Gaps** -- what am I NOT capturing? Where am I learning but not recording?
5. **Action item audit** -- which action items from this month are still open?

End with: "Based on this month, here's what I'd focus on next month."
```

### Quarterly Review (~60 min, every 3 months)

```
Quarterly review: Analyze my Notion second brain entries from the past 90 days.

Give me:
1. **Evolution** -- how has my thinking shifted across the quarter? What did I believe in month 1 that I've revised?
2. **Knowledge inventory** -- what domains am I building depth in? Where am I shallow?
3. **Best decisions** -- which insights actually led to action and results?
4. **Dead weight** -- entries that turned out to be noise, not signal
5. **Connections** -- insights from different weeks/topics that combine into something bigger
6. **Next quarter focus** -- based on trajectory, what should I prioritize capturing?

This is the strategic review. Be honest about what's working and what's just hoarding.
```

---

## Retrieval Patterns

Beyond scheduled reviews, use your second brain as a thinking partner:

| You say... | What it does |
|------------|-------------|
| "What do I know about [topic]?" | Searches your Notion and synthesizes your own captured knowledge |
| "Before I decide on [X], what have I learned that's relevant?" | Decision support from your own experience |
| "Find contradictions in my thinking about [topic]" | Surfaces entries where you held opposing views |
| "What would past-me say about this?" | Uses your captured beliefs and frameworks to stress-test a new idea |
| "Prepare me for a meeting about [topic]" | Pulls relevant entries + action items into a briefing |

---

## Capture Triggers

Use these phrases inside your Second Brain project:

| You say... | Claude does... |
|------------|----------------|
| "Save this to Notion" | Pushes immediately |
| "End session" | Summarizes + pushes + confirms |
| "What's worth capturing?" | Claude proposes what to save, you approve |
| "Push [specific insight] to Notion" | Targeted capture of one thing |
| "Capture this" | Same as "Save this to Notion" |

**Example interaction:**

```
You: "That framework for evaluating vendors is useful. Save this to Notion."

Claude: "Pushing to your second brain:

Title: Vendor Evaluation Framework — Build vs Buy
Key Insights:
- Total cost of ownership beats sticker price (include integration, training, switching costs)
- Red flag: vendor can't articulate their moat
- Decision heuristic: if you'd build it differently, don't buy it
Tags: #procurement #decision-frameworks
Source: Claude Chat
Confidence: High

Confirmed: Entry created successfully."
```

---

## Modes

Add these to your project instructions (see [setup guide](second-brain-setup.md)) to unlock specialized capture behavior.

### Research Mode

For dedicated research sessions where you want to capture more granular findings:

```
## Research Mode

When I say "research mode", shift behavior:
- Capture all substantive findings, not just conclusions
- Include source URLs where relevant
- Mark confidence per finding (High/Medium/Speculative)
- Tag with #research and the topic
- Create multiple entries if covering distinct subtopics

End research mode with "wrap up research" — consolidate into a summary entry linking to detail entries.
```

### Meeting Capture

For capturing decisions and action items from meetings:

```
## Meeting Capture

When I say "meeting mode: [meeting name]":
- Focus on decisions made, not discussion
- Capture action items with owners and deadlines
- Note disagreements or open questions
- Ignore small talk and background info
- Tag with #meeting and attendee names

Push format:
- Title: "[Date] [Meeting Name] — Key Decisions"
- Key Insights: Decisions only
- Action Items: Who does what by when (as checklist)

End with "meeting done" — push immediately.
```

### Brainstorm Mode

For creative sessions where you want to capture speculative and unfinished ideas:

```
## Brainstorm Mode

When I say "brainstorm mode":
- Lower the confidence threshold — capture speculative ideas
- Always set confidence to "Speculative"
- Tag with #brainstorm and #[topic]
- Include "kill criteria" for each idea (what would need to be true for this to work?)

At end: rank ideas by potential impact before pushing. Push all ideas as a single entry sorted by potential.
```

---

## Tips

- **The weekly review is non-negotiable.** Skip it and the system dies. 15 minutes is enough.
- **Tag consistently.** Your future self searches by tags. Inconsistent tagging = invisible entries.
- **Don't just capture -- annotate.** When something shifts your thinking, say why. "This changed my mind because..." is 10x more useful than the raw insight.
- **Review before creating.** Before starting a research session, ask "what do I already know about this?" You'll be surprised how often you've already captured the answer.
- **Always work inside the project.** Regular Claude conversations don't have your capture instructions. Start from the Second Brain project every time.

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| "Can't access Notion" | Check Settings > Integrations > verify Notion is connected. Re-authorize if needed. |
| Push fails silently | Verify the database ID in your project instructions is correct |
| Wrong database | Confirm you are using the **database ID**, not a page ID |
| Push not triggered | Make sure you are working **inside the project**, not in a regular Claude conversation |
| Claude summarizes but doesn't push | The Notion connection may have expired. Go to Settings > Integrations and reconnect. |
| Entry appears but fields are empty | The database schema may not match the project instructions. Verify column names match exactly. |
| Sync delays | Notion changes can take 1-2 minutes to show in Claude. Say "refresh" or "re-check" to force a new read. |
