# Reddit

Check each sidebar for self-promo rules and flair. Space posts 2h+ apart.

## r/ClaudeAI
Why: Claude Code users actively install skills and plugins.
**Title:** I made a Claude Code skill that writes your whole launch (Show HN, PH, Reddit, X) from your repo
**Body:**
Built this after too many projects died at "check it out!" posts. `/launch-kit` reads your README, manifest and commits, then writes a `launch/` folder: Show HN title + maker comment, Product Hunt copy, subreddit-specific posts, X thread, LinkedIn, README glow-up and a 14-day plan.

It's told never to invent stats or testimonials, and it runs a script to check character limits and ban hype words.

Install: `claude plugin marketplace add Barbhuiya12/launch-kit`
Repo: https://github.com/Barbhuiya12/launch-kit

Limitation: garbage README in, mediocre posts out. What would you want it to generate next?

## r/SideProject
Why: this is the audience's exact pain.
**Title:** My side projects kept getting 0 upvotes, so I automated the part I'm bad at
**Body:**
I can build things, but I write launch posts like a robot: "I made X, check it out!" Nobody cares.

So I wrote a skill for AI coding agents that reads the project and writes the launch the way each community actually likes it: technical and humble for HN, a story for Product Hunt, a question for Reddit.

It's free and open source: https://github.com/Barbhuiya12/launch-kit

I'd honestly love for someone to run it on their project and tell me if the output is usable or cringe.

## r/ChatGPTCoding
Why: Codex and Cursor users in one place.
**Title:** Open-source skill for Codex/Cursor/Claude Code: turns a repo into launch posts
**Body:**
Works as a plain SKILL.md, so any agent that can read a file can use it. Codex: `codex plugin marketplace add Barbhuiya12/launch-kit --ref main`. Cursor: drop the folder into `.cursor/skills/`.

Output: 8 files in `launch/`, each self-checked for platform limits. It never makes up numbers.

https://github.com/Barbhuiya12/launch-kit

Which platform's post do you find hardest to write?

## r/indiehackers
Why: founders who launch repeatedly.
**Title:** What I learned writing a checklist for launching on HN, PH and Reddit (turned it into an AI skill)
**Body:**
Things I baked in after reading a lot of successful launches:
- The HN maker comment matters more than the title: why, how it works, what's rough, one question.
- Never put the link in tweet 1.
- LinkedIn: the hook has to fit in the first ~210 characters, and the link goes in the comments.
- Reddit: each sub gets its own post. Identical cross-posts get flagged.

I packaged all of it as a free skill for coding agents: https://github.com/Barbhuiya12/launch-kit

What rule would you add?
