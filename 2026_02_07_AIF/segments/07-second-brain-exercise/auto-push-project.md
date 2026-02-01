# Claude Project + Notion Auto-Push Setup Guide

**Setup time: ~10 minutes**

Turn every Claude conversation into a persistent knowledge asset. This guide shows you how to configure a Claude project that automatically summarizes insights and pushes them to your Notion second brain.

---

## Prerequisites

- Claude Pro/Team subscription (for Projects feature)
- Notion workspace with API access
- Notion MCP integration configured in Claude Desktop

---

## Step 1: Create Your Notion Database

Create a new database in Notion with these properties:

| Property | Type | Purpose |
|----------|------|---------|
| **Title** | Title | Brief topic description |
| **Date** | Date | Auto-filled conversation date |
| **Key Insights** | Text (long) | 3-5 bullet points of learnings |
| **Source** | Select | `Claude Chat`, `Research`, `Meeting`, `Brainstorm` |
| **Tags** | Multi-select | Domain tags for filtering |
| **Action Items** | Text | Next steps, if any |
| **Confidence** | Select | `High`, `Medium`, `Speculative` |

**Grab your database ID** — you'll need it for the project instructions. Find it in your database URL:
```
https://notion.so/workspace/[DATABASE_ID]?v=...
```

---

## Step 2: Claude Project Instructions

Create a new Claude Project and paste these instructions:

### Base Instructions (Copy-Paste Ready)

```
# Knowledge Capture Protocol

You have access to Notion via MCP. At the end of substantive conversations, you will push insights to my second brain.

## Notion Database
- Database ID: [YOUR_DATABASE_ID]

## Automatic Capture Triggers
Push to Notion when:
- User says "save this", "capture this", "push to Notion", or "end session"
- Conversation contains actionable insights, decisions, or novel frameworks
- Research yields reusable findings

Do NOT push for:
- Quick Q&A with no lasting value
- Troubleshooting sessions (unless they reveal reusable patterns)
- Casual conversation

## Capture Format
When pushing to Notion, structure as:

**Title**: [Concise topic — max 60 chars]

**Key Insights** (3-5 bullets):
- Lead with the non-obvious
- Focus on "what changed my thinking" or "what I can use"
- Skip context that's Google-able

**Tags**: [Relevant domain tags]

**Source**: Claude Chat (or appropriate alternative)

**Confidence**:
- High = verified, well-reasoned
- Medium = plausible, needs validation
- Speculative = hypothesis, early thinking

**Action Items**: [Only if there are genuine next steps]

## Behavior
- Ask before pushing if uncertain about value
- Summarize what you're about to capture before executing
- Confirm successful push with the entry title
```

---

## Step 3: End-of-Conversation Prompt Pattern

Use these phrases to trigger capture:

| Phrase | Behavior |
|--------|----------|
| `"Save this to Notion"` | Push immediately |
| `"End session"` | Summarize + push + confirm |
| `"What's worth capturing?"` | Claude proposes, you approve |
| `"Push [specific insight] to Notion"` | Targeted capture |

### Example Interaction

```
You: "That framework for evaluating vendors is useful. Save this to Notion."

Claude: "Pushing to your second brain:

**Title**: Vendor Evaluation Framework — Build vs Buy
**Key Insights**:
- Total cost of ownership beats sticker price (include integration, training, switching costs)
- Red flag: vendor can't articulate their moat
- Decision heuristic: if you'd build it differently, don't buy it
**Tags**: #procurement #decision-frameworks
**Source**: Claude Chat
**Confidence**: High

Confirmed: Entry created successfully."
```

---

## Variation: Research Mode

For dedicated research sessions, add this to your project instructions:

```
## Research Mode

When I say "research mode", shift behavior:
- Capture all substantive findings, not just conclusions
- Include source URLs where relevant
- Tag with #research and the topic
- Create multiple entries if covering distinct subtopics

End research mode with "wrap up research" — consolidate into a summary entry linking to detail entries.
```

---

## Variation: Meeting Notes

For capturing meeting insights:

```
## Meeting Capture

When I say "meeting mode: [meeting name]":
- Focus on decisions made, not discussion
- Capture action items with owners
- Note disagreements or open questions
- Tag with #meeting and attendee names

Push format:
- Title: "[Date] [Meeting Name] — Key Decisions"
- Key Insights: Decisions only
- Action Items: Who does what by when
```

---

## Variation: Brainstorm Sessions

For creative sessions:

```
## Brainstorm Capture

When I say "brainstorm mode":
- Lower the confidence threshold — capture speculative ideas
- Tag with #brainstorm and #[topic]
- Include "kill criteria" for ideas (what would disprove this)

At end: rank ideas by potential impact before pushing.
```

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| "Can't access Notion" | Check MCP config in Claude Desktop settings |
| Push fails silently | Verify database ID is correct |
| Wrong database | Confirm you're using database ID, not page ID |
| Missing properties | Ensure Notion database has all required columns |

---

## Quick Reference Card

```
┌─────────────────────────────────────────────────────────────┐
│ TRIGGERS                                                     │
│ "save this" / "push to Notion" / "end session"              │
├─────────────────────────────────────────────────────────────┤
│ MODES                                                        │
│ "research mode" → capture more, consolidate at end          │
│ "meeting mode: [name]" → decisions + action items           │
│ "brainstorm mode" → lower bar, include speculative          │
├─────────────────────────────────────────────────────────────┤
│ QUERIES                                                      │
│ "what's worth capturing?" → Claude proposes                 │
│ "push [specific thing]" → targeted capture                  │
└─────────────────────────────────────────────────────────────┘
```

---

## What This Buys You

- **Conversations become assets** — insights persist beyond chat history
- **Searchable knowledge base** — Notion's filtering beats scrolling through chats
- **Lower friction** — no manual copy-paste, no reformatting
- **Consistent structure** — every insight captured the same way

The best second brain is one you actually use. This removes the friction that kills most knowledge management systems.
