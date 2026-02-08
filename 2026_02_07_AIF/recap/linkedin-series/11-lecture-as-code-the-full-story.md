<!-- Post 2/12 | Schedule: Day 1, PM | Topic: Lecture as Code | Pillar: Building in the Open -->

My university lecture has a BUILD_LOG.md.

Every decision documented. Why I merged two segments into one closer. Why I upgraded the research exercise from 3k to 30k words. Why I dropped Perplexity from the prerequisites.

It has a .gitignore that handles PII. Student lists go in docs.gitignore/. API keys live in .env.local. The repo is public. The private data never leaves my machine.

Each slide deck starts as a gamma-prompt.md — structured text describing every slide. Text in, presentation out. No manual formatting.

During the live lecture, a student found a broken link. I told Claude Code to investigate. Fixed and pushed to the public repo in 2 minutes. During the lecture. That's not a party trick — that's what happens when your content is a living codebase.

I wrote a full manual for this: 7 phases, from repo setup to post-lecture recap pipeline. Detailed enough to feed into Claude Code and reproduce the whole thing.

Manual → https://github.com/thwinter-ch/ai-lectures/blob/master/2026_02_07_AIF/LECTURE-AS-CODE-MANUAL.md

Repo → https://github.com/thwinter-ch/ai-lectures/tree/master/2026_02_07_AIF

Fork it if you want.

AI x Leadership | 2/12

#BuildInPublic #FieldAI #AIinProduction
