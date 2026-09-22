<h1 align="center">🚀 launch-kit</h1>

<p align="center"><b>You built it. Nobody knows. Fix that in one command.</b></p>

<p align="center">
An open-source skill for AI coding agents that reads your repo and writes your entire launch:<br>
Hacker News · Product Hunt · Reddit · X · LinkedIn · README · demo script · 14-day plan.
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/Barbhuiya12/launch-kit?style=flat" alt="License"></a>
  <a href="https://github.com/Barbhuiya12/launch-kit/stargazers"><img src="https://img.shields.io/github/stars/Barbhuiya12/launch-kit?style=flat" alt="Stars"></a>
  <img src="https://img.shields.io/badge/Claude%20Code-supported-D97757" alt="Claude Code">
  <img src="https://img.shields.io/badge/Codex-supported-000000" alt="Codex">
  <img src="https://img.shields.io/badge/Cursor-supported-3B82F6" alt="Cursor">
</p>

---

## The problem

Most side projects don't fail in the code. They fail on launch day.

You spend weeks building, then an hour writing *"I made a thing, check it out! 🙏"*. It gets 2 upvotes, and the project quietly dies. Writing launch posts is a separate skill, and every platform has its own unwritten rules.

## The solution

```text
/launch-kit
```

launch-kit reads what you actually built (README, manifest, landing page, commits), finds the strongest angle, and writes a `launch/` folder with a post for every channel, each in that platform's native voice.

```
launch/
├── show-hn.md        Title + the maker's first comment HN actually rewards
├── product-hunt.md   Tagline, description, maker comment, gallery captions
├── reddit.md         3–5 subreddits where your users are, a unique post for each
├── x-thread.md       Hook-first thread, every tweet character-counted
├── linkedin.md       Hook above "see more", lessons-learned story
├── readme.md         Above-the-fold README: hook, badges, demo, quickstart
├── demo.md           20-second demo GIF storyboard
└── plan.md           Dated 14-day checklist: when, where, what to measure
```

👉 **[See a real, complete example](examples/launch-kit/)**: launch-kit run on itself.

## Before / after

<table>
<tr>
<td width="50%">

**Typical launch post**

> Show HN: I made an amazing AI-powered tool that will change how you ship 🚀🔥
>
> Check it out!! Would love your support 🙏

</td>
<td width="50%">

**With launch-kit**

> Show HN: Launch-kit – an agent skill that writes your repo's launch posts
>
> *Maker comment:* why I built it → how it works → what's still rough → one specific question for HN.

</td>
</tr>
</table>

## Install

The quickest way is to paste this into your coding agent:

```text
Install the launch-kit skill from https://github.com/Barbhuiya12/launch-kit, see the repo's README for instructions.
```

<details><summary><b>Claude Code</b></summary>

```bash
claude plugin marketplace add Barbhuiya12/launch-kit
claude plugin install launch-kit@launch-kit
```
Use it in any repo: `/launch-kit`
</details>

<details><summary><b>Codex</b></summary>

```bash
codex plugin marketplace add Barbhuiya12/launch-kit --ref main
codex plugin add launch-kit@launch-kit
```
Use it: `$launch-kit`
</details>

<details><summary><b>Cursor & other agents</b></summary>

Copy `skills/launch-kit/` into `.cursor/skills/` (or your agent's skills folder). Or tell any agent:

```text
Read https://github.com/Barbhuiya12/launch-kit/blob/main/skills/launch-kit/SKILL.md and follow it on this repo.
```
</details>

**Options:** `/launch-kit ../other-repo` targets another folder. `/launch-kit only:hn,reddit` writes just those channels.

## How it works

1. **Recon.** Reads your repo and builds a fact sheet: what it does, who it's for, the pain, what's different, proof, how to try it.
2. **Angle.** Writes 3 hooks (contrast, pain, proof) and picks the strongest.
3. **Write.** One file per channel, following each platform's culture and limits.
4. **Self-check.** Runs a script: character limits, a banned hype-word list, no duplicate Reddit posts, every claim traceable to the repo.
5. **Report.** The chosen hook, what's missing before launch, and your single next action.

## Principles

| | |
|---|---|
| 🧾 **Never invents** | No fake users, stars, benchmarks or testimonials. If it's not in your repo, it's not in your posts. |
| 🔧 **Shows the mechanism** | "Runs Whisper on WebGPU" beats "AI-powered" every time. |
| 🙋 **Admits one limitation** | Honesty earns more trust than any adjective. |
| 🌍 **Native to each platform** | HN: technical. PH: a story. Reddit: a peer asking. X: punchy. LinkedIn: lessons. |
| ✋ **Never posts for you** | It writes files. You review and hit publish. |

The full ruleset is in [`SKILL.md`](skills/launch-kit/SKILL.md), plain Markdown you can fork and tune.

## FAQ

**Does it need an API key or a paid service?** No. It's a set of instructions for the coding agent you already use.

**Will the posts sound AI-written?** It bans the usual hype phrases, writes in the first person, and forces concrete details from your code. Always edit in your own voice before posting.

**What if my README is thin?** Output quality follows input quality. It will tell you what's missing (demo link, install command, proof) in its report.

## Contributing

Ideas, new channels (newsletters, dev.to, Discord) and better platform rules are welcome. Open an issue or PR.

## License

[MIT](LICENSE)

<p align="center">⭐ <b>Star it if it saved you from writing "would love your support 🙏"</b></p>
