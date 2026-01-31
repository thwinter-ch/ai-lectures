# Connecting Claude to Notion: Your Second Brain Setup

A practical guide for using Claude Pro/Max with Notion as an integrated knowledge system.

---

## Prerequisites

Before you begin, ensure you have:

| Requirement | Details |
|-------------|---------|
| **Claude Pro or Max subscription** | Free tier does not include MCP integrations. Verify at claude.ai/settings |
| **Notion account** | Free, Plus, or Business tier all work |
| **Desktop browser** | Chrome, Edge, Safari, or Firefox (mobile not supported for setup) |
| **10-15 minutes** | One-time setup |

---

## Step 1: Enable the Notion Integration in Claude

1. Open [claude.ai](https://claude.ai) and sign in
2. Click your **profile icon** (bottom-left corner)
3. Select **Settings**
4. Navigate to **Integrations** or **Connected Apps** in the left sidebar
5. Find **Notion** in the available integrations list
6. Click **Connect**

> **What you'll see:** A toggle or "Connect" button next to the Notion logo. Status will show "Not connected" initially.

---

## Step 2: Authorize Claude in Notion

After clicking Connect, Notion's authorization page opens:

1. **Sign in to Notion** if prompted
2. Review the permissions Claude is requesting:
   - Read content from pages and databases
   - Insert content
   - Update content
3. **Select pages to share:**
   - Click **"Select pages"** (not "Allow access to all pages" unless intentional)
   - Check the specific pages or databases you want Claude to access
   - You can always add more later
4. Click **Allow access**

> **What you'll see:** A Notion popup showing your workspace name, requested permissions, and a page selector tree.

### Recommended Starting Selection

For a "second brain" setup, grant access to:
- A dedicated "AI Notes" or "Claude Workspace" page
- Any databases you want Claude to query (e.g., meeting notes, projects, reading list)
- NOT: sensitive HR, financial, or confidential pages

---

## Step 3: Verify the Connection

Back in Claude:

1. Return to **Settings > Integrations**
2. Notion should now show **"Connected"** with a green indicator
3. Note: You may see the specific pages/databases listed

> **What you'll see:** Status changed to "Connected" with options to "Disconnect" or "Manage access."

---

## Step 4: Test Read Access

Start a new Claude conversation and try:

```
Search my Notion for pages about [topic you know exists]
```

**Expected result:** Claude retrieves and summarizes relevant content from your connected pages.

If Claude says it cannot access Notion or finds nothing:
- Verify the page is in your shared selection
- Check that the page contains the search terms
- Try a more specific page name

---

## Step 5: Test Write Access

Try creating a simple test note:

```
Create a new page in my Notion called "Claude Test Note" with the content:
"This is a test note created by Claude on [today's date]."
```

**Expected result:** Claude confirms creation and may provide a link to the new page.

**Verify in Notion:**
1. Open Notion
2. Check your sidebar or search for "Claude Test Note"
3. Confirm the content appears correctly

---

## Step 6: Practical Usage Examples

Once connected, try these high-value use cases:

| Use Case | Example Prompt |
|----------|----------------|
| **Meeting synthesis** | "Summarize all my meeting notes from last week and identify action items" |
| **Knowledge retrieval** | "What do my notes say about [client name] project timeline?" |
| **Content creation** | "Create a Notion page summarizing the key points from this document: [paste text]" |
| **Database queries** | "Show me all tasks in my Projects database marked as high priority" |
| **Cross-reference** | "Find connections between my notes on AI strategy and digital transformation" |

---

## Troubleshooting

### "Claude cannot access Notion" or "I don't have access to that"

| Cause | Fix |
|-------|-----|
| Page not in shared selection | Settings > Integrations > Notion > Manage Access > Add the page |
| Connection expired | Disconnect and reconnect the integration |
| Page is in a different workspace | Ensure you authorized the correct Notion workspace |

### "Page created but I can't find it"

- Check your Notion "Private" section (new pages default there)
- Search for the exact page title in Notion
- Specify a parent page in your prompt: "Create a page under [Parent Page Name]"

### "Claude can read but cannot write"

- Re-authorize the connection; ensure "Insert content" permission is granted
- Some Notion Enterprise workspaces restrict external app writes—check with your IT admin

### Integration not appearing in Claude settings

- Confirm you have Claude Pro or Max (not free tier)
- Try logging out and back in
- Clear browser cache and refresh

### Sync delays

- Notion changes can take 1-2 minutes to reflect in Claude
- For real-time needs, explicitly tell Claude to "refresh" or "re-check" the page

---

## Security Notes

- Claude only accesses pages you explicitly share
- You can revoke access anytime: Settings > Integrations > Notion > Disconnect
- Notion's sharing settings still apply—Claude cannot bypass your workspace permissions
- Review shared pages quarterly; remove what you no longer need Claude to access

---

## Next Steps

Once your connection is working:

1. **Create a dedicated Claude workspace page** in Notion for AI-generated content
2. **Set up a "Quick Capture" database** where Claude can log insights, ideas, or summaries
3. **Experiment with database queries** if you use Notion databases for projects or tasks

---

*Setup complete. Your second brain is now connected.*
