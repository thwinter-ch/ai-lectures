# Signal Filter

**Status:** stub
**Deliverable:** Signal extracted from noise across your information streams

The same core idea applied to different channels: cut through the volume, surface what matters, ignore the rest.

## Variants

| Channel | Best tool (as of Feb 2026) | Execution modes |
|---------|---------------------------|-----------------|
| [newsletter/](newsletter/) | Gemini (native Gmail) | Manual, scheduled task, n8n, OpenClaw |
| [youtube/](youtube/) | Gemini (native YouTube) | Manual, scheduled task |

## Why execution variants matter

Each channel has different tool capabilities that **change frequently**. Every instruction file is dated. What works in Gemini today may work in Claude tomorrow. The variants capture:

- **Manual:** You run it in a conversation when you need it
- **Scheduled task:** The AI runs it on a schedule (e.g. Gemini daily task)
- **n8n automation:** Workflow-based, runs without you
- **OpenClaw agent:** Autonomous agent variant

## Tool landscape (Feb 2026)

| Tool | Gmail access | YouTube access | Scheduled tasks | Notes |
|------|-------------|----------------|-----------------|-------|
| **Gemini** | Native | Native | Yes (Gems) | Best for both channels right now |
| **Claude Pro** | Via connector | No | No | Good for analysis, not native access |
| **ChatGPT Plus** | Via connector | No | No | Similar to Claude |
| **Perplexity** | No | No | No | Web research only |
| **n8n** | Via API/IMAP | Via API | Yes (cron) | Full automation, requires setup |
| **OpenClaw** | Via tools | Via tools | Yes (scheduled) | Agent-based, most autonomous |

> **This table will be outdated.** Check the date on each variant file and update when capabilities change.
