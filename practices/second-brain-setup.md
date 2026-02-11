# Second Brain Setup Guide

One-time setup to connect Claude to Notion. Takes ~15 minutes. Once done, see [second-brain.md](second-brain.md) for how to use it.

---

## Which AI Platforms Support Notion?

As of February 2026, the connector landscape changes fast. Here's what works today:

| Platform | Read from Notion | Write to Notion | Notes |
|----------|:---:|:---:|-------|
| **Claude** (Pro/Max) | Yes | Yes | Full read + write via MCP integration |
| **Perplexity** | Yes | Yes | Works at time of writing |
| **ChatGPT** | Yes | **No** | Can read from Notion but cannot write back |

This guide uses Claude because it has the most complete integration. If you prefer another platform, verify its current Notion capabilities before starting -- these connectors evolve quickly and what's true today may change.

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Claude Pro or Max** | Free tier does not include MCP integrations. Verify at [claude.ai/settings](https://claude.ai/settings) |
| **Notion account** | Free tier works fine; any paid tier also works |
| **Desktop browser** | Chrome, Edge, Safari, or Firefox (mobile not supported for initial setup) |

---

## Step 1: Connect Claude to Notion

### 1.1 Enable the Notion Integration in Claude

1. Open [claude.ai](https://claude.ai) and sign in
2. Click your **profile icon** (bottom-left corner)
3. Select **Settings**
4. Navigate to **Integrations** or **Connected Apps** in the left sidebar
5. Find **Notion** in the available integrations list
6. Click **Connect**

You should see a toggle or "Connect" button next to the Notion logo. Status will show "Not connected" initially.

### 1.2 Authorize Claude in Notion

After clicking Connect, Notion's authorization page opens:

1. **Sign in to Notion** if prompted
2. Review the permissions Claude is requesting:
   - Read content from pages and databases
   - Insert content
   - Update content
3. **Select pages to share:**
   - Click **"Select pages"** (NOT "Allow access to all pages" unless you specifically want that)
   - Check the specific pages or databases you want Claude to access
   - You can always add more later
4. Click **Allow access**

**Recommended starting selection:**
- A dedicated "AI Notes" or "Second Brain" page
- Any databases you want Claude to query (e.g., projects, reading list)
- **NOT:** sensitive financial, HR, or confidential pages

### 1.3 Verify the Connection

Back in Claude:

1. Return to **Settings > Integrations**
2. Notion should now show **"Connected"** with a green indicator
3. You may see the specific pages/databases listed

### 1.4 Test Read Access

Start a new Claude conversation and try:

```
Search my Notion for pages about [topic you know exists]
```

**Expected result:** Claude retrieves and summarizes relevant content from your connected pages.

If Claude says it cannot access Notion or finds nothing:
- Verify the page is in your shared selection
- Check that the page contains the search terms
- Try a more specific page name

### 1.5 Test Write Access

Try creating a simple test note:

```
Create a new page in my Notion called "Claude Test Note" with the content:
"This is a test note created by Claude."
```

**Expected result:** Claude confirms creation and may provide a link to the new page.

**Verify in Notion:**
1. Open Notion
2. Check your sidebar or search for "Claude Test Note"
3. Confirm the content appears correctly (check your "Private" section if you don't see it immediately)

### Connection Troubleshooting

| Problem | Fix |
|---------|-----|
| "Claude cannot access Notion" | Settings > Integrations > Notion > Manage Access > Add the page |
| Page created but can't find it | Check your Notion "Private" section; search for the exact page title |
| Claude can read but cannot write | Re-authorize the connection; ensure "Insert content" permission is granted |
| Integration not appearing in Claude settings | Confirm you have Claude Pro or Max (not free tier). Log out and back in. Clear browser cache. |
| Connection expired | Disconnect and reconnect the integration |
| Page is in a different workspace | Ensure you authorized the correct Notion workspace |
| Sync delays | Notion changes can take 1-2 minutes to reflect in Claude. Tell Claude to "refresh" or "re-check" the page. |

### Security Notes

- Claude only accesses pages you explicitly share
- You can revoke access anytime: Settings > Integrations > Notion > Disconnect
- Notion's workspace permissions still apply -- Claude cannot bypass them
- Review shared pages periodically; remove what you no longer need Claude to access

---

## Step 2: Create Your Second Brain Database

Start a new Claude conversation and say:

> "Create a Second Brain database in Notion with fields for Title, Date, Key Insights, Source, Tags, Action Items, and Confidence. Give me the database ID."

Claude will create the database and return the ID. **Copy this ID -- you need it for Step 3.**

Here is the database schema Claude will create:

| Property | Type | Purpose |
|----------|------|---------|
| **Title** | Title | Brief topic description (max 60 characters) |
| **Date** | Date | Auto-filled conversation date |
| **Key Insights** | Text (long) | 3-5 bullet points of learnings |
| **Source** | Select | `Claude Chat`, `Research`, `Meeting`, `Brainstorm` |
| **Tags** | Multi-select | Domain tags for filtering |
| **Action Items** | Text | Next steps, if any |
| **Confidence** | Select | `High`, `Medium`, `Speculative` |

**Finding your database ID manually** (if needed): It is in the database URL:
```
https://notion.so/workspace/[DATABASE_ID]?v=...
```

---

## Step 3: Configure the Auto-Capture Project

1. Go to [claude.ai](https://claude.ai) and click **Projects** in the left sidebar
2. Click **New Project**
3. Name it something like "Second Brain"
4. Open the **Project Instructions** and paste the block below
5. Replace `[YOUR_DATABASE_ID]` with the database ID from Step 2

### Project Instructions (Copy-Paste Ready)

```
# Knowledge Capture Protocol

You have access to Notion via MCP. At the end of substantive conversations, you will push insights to my second brain.

## Notion Database
- Database ID: [YOUR_DATABASE_ID]

## Automatic Capture Triggers
Push to Notion when:
- I say "save this", "capture this", "push to Notion", or "end session"
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

## Step 4: Test It

1. Open a new conversation **within your Second Brain project** (not a regular conversation)
2. Have a short conversation -- e.g., ask Claude to explain a topic you care about
3. At the end, say: **"Save this to Notion"**
4. Check Notion for the new entry

If it works, you're done. Head to [second-brain.md](second-brain.md) for how to use it day-to-day.

---

## Adding Modes (Optional)

Once your basic setup works, you can extend it with specialized modes. Open your Second Brain project, go to **Project Instructions**, and append any mode blocks from [second-brain.md](second-brain.md#modes).
