<h1 align="center">🚀 launch-kit</h1>
<p align="center"><b>You built it. Nobody knows. Fix that in one command.</b><br>
A skill for Claude Code, Codex and Cursor that reads your repo and writes your whole launch:<br>
Show HN · Product Hunt · Reddit · X thread · LinkedIn · README glow-up · demo script · 14-day plan.</p>
<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/Barbhuiya12/launch-kit?style=flat" alt="License"></a>
  <img src="https://img.shields.io/github/stars/Barbhuiya12/launch-kit?style=flat" alt="Stars">
  <img src="https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Cursor-orange" alt="Works with">
</p>

## Install

Paste into your coding agent:

```text
Install the launch-kit skill from https://github.com/Barbhuiya12/launch-kit, see the repo's README for instructions.
```

<details><summary><b>Claude Code</b></summary>

```bash
claude plugin marketplace add Barbhuiya12/launch-kit
claude plugin install launch-kit@launch-kit
```
Then, in your repo: `/launch-kit`
</details>

<details><summary><b>Codex</b></summary>

```bash
codex plugin marketplace add Barbhuiya12/launch-kit --ref main
codex plugin add launch-kit@launch-kit
```
Then: `$launch-kit`
</details>

<details><summary><b>Cursor / anything else</b></summary>

Copy `skills/launch-kit/` into `.cursor/skills/` (or your agent's skills folder), or just tell your agent:
"Read https://github.com/Barbhuiya12/launch-kit/blob/main/skills/launch-kit/SKILL.md and follow it on this repo."
</details>

## What changes

<table>
<tr>
<td width="50%">

### Without launch-kit

> **Show HN: I made an amazing AI-powered tool that will revolutionize transcription 🚀🔥**
>
> Check it out!! Would love your support and upvotes 🙏

*Buried. Zero comments.*

</td>
<td width="50%">

### With launch-kit

> **Show HN: Hushscribe – Whisper transcription and subtitles, fully in-browser**
>
> *Maker comment:* why I built it → how it works (Whisper via Transformers.js in a Web Worker, WebGPU with WASM fallback) → what's rough (30s chunk boundaries can clip words) → one specific question for HN.

*Written the way HN actually reads.*

</td>
</tr>
</table>

See the **[full real example →](examples/hushscribe/)** (every file launch-kit wrote for a real project).

## What you get

`/launch-kit` reads your README, manifest, landing page and commits, then writes a `launch/` folder:

| File | What's inside |
|---|---|
| `show-hn.md` | ≤80-char title + the maker's first comment (why, how it works, what's rough, one ask) |
| `product-hunt.md` | ≤60-char tagline, description, maker comment, 5 gallery captions |
| `reddit.md` | 3–5 subreddits where your users actually are, each with its own title and body |
| `x-thread.md` | Hook tweet with no link, a 5–6 tweet story, character count on every tweet |
| `linkedin.md` | Hook in the first 210 chars, lessons-learned arc, link in comments |
| `readme.md` | Above-the-fold README: hook, badges, demo, why, 3-command quickstart, honest comparison |
| `demo.md` | A 20-second GIF storyboard that shows the payoff first |
| `plan.md` | A dated 14-day checklist: directories, awesome-lists, posting times, what to measure |

## The rules it follows

1. **Never invents anything.** No fake users, stars, benchmarks or testimonials. Every claim traces to your repo.
2. **Shows the mechanism.** "Runs Whisper on WebGPU" beats "AI-powered".
3. **Admits one limitation.** It buys more trust than any adjective.
4. **Adapts to each platform's culture.** HN is technical, PH is a story, Reddit is a peer asking, X is punchy, LinkedIn is lessons.
5. **Self-checks with a script.** Character limits, a banned hype-word list ("revolutionary", "game-changer", "unleash"…), and no duplicate Reddit posts.
6. **Never posts for you.** It writes files; you hit publish.

Full text: [SKILL.md](skills/launch-kit/SKILL.md).

## License

[MIT](LICENSE)

⭐ Star if it saved you from writing "Would love your support 🙏".
