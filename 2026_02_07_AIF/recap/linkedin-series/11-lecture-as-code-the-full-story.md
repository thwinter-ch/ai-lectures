<!-- Post 11/12 | Bonus | Topic: Lecture as Code — The Full Story -->

My university lecture has a BUILD_LOG.md.

It has a .gitignore. A commit history. Pull requests. A README in two languages.

It lives in a GitHub repository, version-controlled like production software. Because that's what it is.

Here's what "Lecture as Code" actually means:

Every decision is documented. Not in my head — in a build log. Why we merged segments 08 and 09 into one closer. Why we upgraded the research exercise from 3,000 to 30,000 words. Why we dropped Perplexity from the prerequisites and standardized on Claude. It's all there. Timestamped. Reasoned.

Every change is tracked. When I restructured the folder hierarchy from slides/exercises to a unified segments/ directory, that's a commit. When a student found a broken link during the live session, Claude Code fixed it and pushed to the public repo in 2 minutes. That's a commit too. During the lecture. In front of 21 people.

Sensitive data is handled properly. Student lists, participant emails, API keys — they live in gitignored directories or environment files. Not because I'm paranoid, but because it's the obvious thing to do when your content is public infrastructure.

The slides are generated from text. Each Gamma deck starts as a markdown file — a gamma-prompt.md with structured slide descriptions. Text in, presentation out. Change the text, regenerate the deck. No manual formatting. No "can you move this box 2 pixels left."

Why does any of this matter?

Because it's repeatable. The next lecturer can fork the repo, swap their content in, and have the same infrastructure. The exercises link to live GitHub files — update the repo, the exercise updates. No "version 3 final FINAL (2).pptx" in anyone's inbox.

Because it's transparent. Students can see exactly how their lecture was built. The build log is public. The prompts are public. The methodology is public. "Lecture as Code" isn't a metaphor — it's a link they can click.

Because it compounds. Every lecture I build adds to the same codebase. Templates, email workflows, exercise patterns — they accumulate. The second lecture takes half the time. The third, less.

The parallel to "Infrastructure as Code" is deliberate. DevOps teams stopped manually configuring servers and started writing declarative configs. Same idea: stop manually assembling lectures and start writing content that generates them.

The total production cost for a 3.5-hour university lecture with 5 slide decks, 3 hands-on exercises, bilingual documentation, and a public recap page: about two weeks of side-project time and $15 in API calls.

The repo is public. The methodology is documented. Fork it if you want.

AI x Leadership | 11/12

#LectureAsCode #Education #AIProductivity #OpenSource #InfrastructureAsCode
