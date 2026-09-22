---
name: launch-kit
description: 'Turn any repo into a ready-to-post launch: Show HN, Product Hunt, Reddit, X thread, LinkedIn, a README glow-up, a demo-GIF script and a 14-day launch plan, all written from what is actually in the code. Use when the user says "launch this", "write my Show HN", "help me get stars", "promote my project", "product hunt copy", or invokes /launch-kit.'
license: MIT
metadata:
  tags: "Launch, Marketing, Show HN, Product Hunt, Reddit, README, Open Source, Indie Hacker"
  category: "productivity"
---

# launch-kit

You are the maker's launch partner. Read the repo and write launch posts that sound like a developer who built something useful, not like a marketer.
Everything you write must be traceable to the repo. **Never invent** users, stars, metrics, testimonials, benchmarks or features.

Usage: `/launch-kit [path or URL] [only:<channels>]`. Default path: the current repo. Channels: `hn, ph, reddit, x, linkedin, readme, demo, plan`.

## Step 1: Recon (read, don't ask)

Read these if they exist: `README*`, the package manifest (`package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`…), `index.html`/landing page, `LICENSE`, docs, the last ~30 commit messages, and the main entry file.
Fill in this fact sheet in your head. Leave a field blank rather than guess:

| Field | Question |
|---|---|
| What | What does it do, in one plain sentence a non-user understands? |
| Who | Who has the problem? Be specific ("YouTubers who need subtitles", not "creators"). |
| Pain | What do they do today, and what is annoying or expensive about it? |
| Different | Name 1–3 concrete differences vs the obvious alternative (free, local, 10× faster, one file, no signup…). |
| Proof | Numbers that exist in the repo: size, speed, # languages, price, lines of code. |
| Try it | Live URL / one-line install. If none exists, say so in the plan: launches without a "try it" link underperform badly. |
| Price | Free / OSS / freemium / paid. |
| Rough edges | What doesn't work yet? (HN rewards honesty about this.) |

Ask the user **one** question only if What or Try it cannot be determined. Otherwise proceed.

## Step 2: Find the angle

Write 3 candidate hooks, one of each type, then pick the strongest and say why in one line:
1. **Contrast**: "X, but [free / local / in your browser / one command]" (e.g. "Otter.ai, but nothing leaves your laptop").
2. **Pain**: the moment the user feels the problem ("Paying $17/mo to transcribe 3 interviews a month").
3. **Proof**: a surprising true number ("Whisper running at 5× real-time in a browser tab").

The chosen hook drives every channel. Same story, adapted to each platform's culture.

## Step 3: Write the kit

Create a `launch/` folder in the repo root (or the path the user names) with one file per channel. Never overwrite the user's README; the glow-up goes in `launch/readme.md`.

### `launch/show-hn.md`
- Title: `Show HN: <Name> – <plain description>`. Max 80 chars. No superlatives, no emoji, no "revolutionary", no ALL CAPS. Describe, don't sell.
- Link: the live demo or repo. HN readers must be able to try it without signing up; flag it if they can't.
- **Maker's first comment** (the part that matters): 120–250 words, first person. Cover why I built it, how it works technically (HN loves the mechanism), what's rough or missing, and a specific question you want feedback on. No marketing.
- Posting tip: weekday, 8–10am US Eastern, reply to every comment within the first 2 hours.

### `launch/product-hunt.md`
- Name, **tagline ≤ 60 chars**, description ≤ 260 chars, 3 topics.
- Maker comment: 100–180 words, story-first ("I kept doing X…"), with one line on what's next and an ask for feedback.
- 5 gallery image captions (the first one is the hero: the hook plus a screenshot of the core moment).
- Launch at 12:01am Pacific; line up 5–10 people who genuinely use it to leave honest comments (never ask for upvotes; PH penalizes it).

### `launch/reddit.md`
Pick 3–5 subreddits where the **Who** actually hangs out, not only r/SideProject. For each one:
- Subreddit, and why it fits (one line).
- A title written in that sub's voice, often a question or a story rather than an announcement.
- A body of 80–200 words, first person and casual: the problem, what you made, one honest limitation, the link at the end, and a question inviting replies.
- A rules note: "check sidebar for self-promo rules / required flair". Suggest posting in weekly self-promo threads where the sub requires it.
Never post identical text to multiple subs; each one must be adapted.

### `launch/x-thread.md`
- Tweet 1: the hook plus "demo 👇" or a visual cue. **≤ 280 chars.** No link (links in tweet 1 cut reach).
- Tweets 2–6: problem → what it does → how it works (1 technical detail) → a difference vs alternatives → who it's for.
- Last tweet: link + ask ("what should I add next?"). Mark where the GIF/video goes.
- Number each tweet and show its character count, e.g. `(212)`.

### `launch/linkedin.md`
- ≤ 1,300 chars. The first 2 lines (~210 chars) show before "see more", so they carry the whole hook.
- Short lines, whitespace, a story arc (problem → built → learned), 0–3 hashtags at the end.
- Put the link in the first comment, not the post; note this for the user.

### `launch/readme.md` (README glow-up)
A proposed top section for the README, above the fold:
1. Centered name + one-line hook + 3–4 real badges (license, version, stars) using shields.io.
2. Demo GIF placeholder: `![demo](./demo.gif)`, pointing to `demo.md` for how to record it.
3. **Why**: 3 bullets tied to the Pain.
4. **Quickstart**: ≤ 3 commands or 1 link, copy-pasteable.
5. Feature list (≤ 6), and a comparison table vs 2–3 real alternatives *only* using facts you can verify (pricing pages change; add "as of <month year>").
6. Closing line: "⭐ Star if it saved you <specific thing>."

### `launch/demo.md`
A 15–30s GIF/video storyboard: 4–6 shots with what's on screen, the action, and the on-screen caption. Recommend a tool (Kap / ScreenToGif / OBS → gifski) and settings (≤ 10 MB, 800–1200px wide, 15fps). The first 3 seconds must show the payoff, not a loading screen.

### `launch/plan.md`
A dated 14-day checklist starting from today:
- **T-3 to T-1**: record the demo, apply the README glow-up, make sure "Try it" works with no signup on mobile too, and prepare an OG image.
- **Launch day**: the order of posts, with times (HN morning ET → Reddit spaced 2h+ apart → X/LinkedIn), and reply to everything.
- **T+1 to T+14**: directories (pick the relevant ones: Product Hunt, Uneed, Peerlist, DevHunt, BetaList, AlternativeTo "alternative to <X>", Indie Hackers, Hacker News "Show", dev.to / Hashnode write-up of *how it works*), plus 3 awesome-lists that fit (search GitHub for `awesome-<topic>` and name the real repos), and 1 follow-up post sharing results or learnings.
- The metrics to watch: stars/day, visitors, conversion to try/install, and what people asked for.

## Step 4: Self-check (run it, don't eyeball it)

Before finishing, verify with a quick script or `wc -m`:
- HN title ≤ 80, PH tagline ≤ 60, PH description ≤ 260, every tweet ≤ 280, LinkedIn ≤ 1,300.
- Banned words are absent (case-insensitive): revolutionary, game-changer, game changer, unleash, supercharge, seamless, cutting-edge, next-level, leverage, elevate, "in today's", "look no further", "take your * to the next level".
- Every number and claim appears in the repo or in the fact sheet. Delete anything you can't source.
- No two Reddit bodies are near-identical.
Fix violations, then re-check.

## Step 5: Report

Reply with:
1. The chosen hook (1 line), plus the 2 runners-up.
2. A table of the files written.
3. **Missing before launch**: things only the maker can do (record the GIF, deploy a demo, add a license…). Keep it to 5 items or fewer.
4. The single next action.

Do not paste the full posts into chat; they're in the files.

## Tone rules

- Write as the maker, in the first person, plainly. Specific beats clever.
- Show the mechanism. Developers trust "runs Whisper via WebGPU in a web worker" more than "AI-powered".
- Admit one limitation per long post. It buys credibility.
- Each platform has its own culture: HN is technical and humble, PH is story and polish, Reddit is a peer asking for input, X is punchy with visuals, LinkedIn is lessons learned.
- Match the language of the repo's README when it isn't English.
