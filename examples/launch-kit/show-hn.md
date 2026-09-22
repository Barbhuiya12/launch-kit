# Show HN

**Title** (73 chars)
Show HN: Launch-kit – an agent skill that writes your repo's launch posts

**Link:** https://github.com/Barbhuiya12/launch-kit

**Maker's first comment**

Most side projects die at launch, not in the code. I'd finish something, write a two-line "check it out!" post, and get nothing.

launch-kit is a skill (a Markdown instruction file) for Claude Code, Codex and Cursor. It reads your README, manifest, landing page and recent commits, builds a fact sheet, picks a hook out of three candidates, and writes a `launch/` folder: a Show HN title plus the maker comment, Product Hunt copy, per-subreddit posts, an X thread, a LinkedIn post, a README top section, a demo-GIF storyboard and a dated 14-day plan.

Two rules I cared about: it must never invent numbers, users or testimonials (every claim has to trace to the repo), and it runs a self-check script for character limits plus a banned-word list ("revolutionary", "unleash"…).

Rough edges: the output quality depends on how good your README is, and it can't know your real metrics unless they're written down somewhere.

Question for HN: what makes you click a Show HN, and what makes you close it immediately?
