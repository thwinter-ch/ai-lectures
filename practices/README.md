# Practices

Wiederverwendbare Playbooks, die eigenständig oder als Teil einer Vorlesung funktionieren. Jede Practice enthält fertige Copy-Paste-Prompts und klare Tool-Empfehlungen.

## Index

| Practice | Dauer | Tools | Status |
|----------|-------|-------|--------|
| [writing-profile](writing-profile/) | 20 min | Claude Pro, ChatGPT, Gemini | proven |
| [company-research](company-research/) | 30 min | Perplexity Pro, Claude Pro | proven |
| [second-brain](second-brain/) | 25 min | Claude Pro + Notion | proven |
| [email-writing](email-writing/) | 10 min | Claude, ChatGPT, Gemini | proven |
| [document-summary](document-summary/) | 10 min | Claude, ChatGPT, Gemini | proven |
| [avatar-video](avatar-video/) | 15 min | HeyGen | testing |
| [drip-feed-engagement](drip-feed-engagement/) | -- | WhatsApp, HeyGen | testing |
| [podcast-from-doc](podcast-from-doc/) | 10 min | NotebookLM | testing |
| [newsletter-signal-filter](newsletter-signal-filter/) | 15 min | Gemini (Gmail), Claude, n8n | stub |
| [inbox-action-items](inbox-action-items/) | 15 min | Gemini (Gmail), Claude, n8n | stub |
| [prompt-extractor](prompt-extractor/) | 20 min | Perplexity Pro, Claude | stub |

## Status-Legende

- **proven** -- In mindestens einer Vorlesung eingesetzt und validiert
- **testing** -- Wird gerade getestet
- **stub** -- Struktur steht, Inhalt kommt noch

## Aufbau einer Practice

Jede Practice hat mindestens eine `README.md` mit:
- Was du am Ende hast (konkretes Ergebnis)
- Welches Tool und warum
- Copy-Paste-Prompt(s)
- Fehlerbehebung

Komplexere Practices haben zusätzlich `prompts/` und `guides/` Unterordner.

## Public vs. Private

Die generischen Versionen sind öffentlich auf GitHub. Persönliche Anpassungen (eigene Outputs, kundenspezifische Varianten) liegen in `docs.gitignore/` und sind nicht im Repo.
