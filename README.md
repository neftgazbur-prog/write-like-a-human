# write-like-a-human ✍️

![type](https://img.shields.io/badge/type-agent%20skill-blue) ![rules](https://img.shields.io/badge/rules-21-green) ![deps](https://img.shields.io/badge/dependencies-none-success) [![GitHub Repo stars](https://img.shields.io/github/stars/neftgazbur-prog/write-like-a-human?style=social)](https://github.com/neftgazbur-prog/write-like-a-human/stargazers)

> An agent skill that rewrites machine-flavored prose into text a human would actually own up to.

LLMs write recognizably. Everything matters enormously. Sources vaguely agree. Sentences march in threes. Every other clause is bolted on with an em dash, and the piece ends with "In conclusion, X continues to thrive." Human readers — and Wikipedia's editors, who maintain entire field guides on the subject — spot it within a paragraph.

**write-like-a-human** gives your coding or writing agent a repeatable de-AI pass: one regex sweep, 21 tell-and-fix rules, and a positive style pass that fills the vacuum with what human prose actually does.

If it cleaned up a draft of yours, **give it a star ⭐** — it helps other writers find the skill.

## What the skill does

1. **Sweeps** the draft with a search pattern of ~50 stock phrases and habits ("plays a pivotal role", "vibrant", "nestled in the heart of", "It's important to note", `utm_source=chatgpt.com`…).
2. **Decides**, hit by hit: does the phrase carry real information? Keep it. Is it filler in a stock shape? Rewrite it.
3. **Fixes** per rule — each tell comes with a concrete replacement strategy.
4. **Finishes** with a positive pass: concrete over general, uneven rhythm, attribution with a face, the deletion test.

## Example

*Fictional example for illustration.*

*A typical machine-flavored paragraph:*

> Nestled in the heart of the Pacific Northwest, the Salish Sea Institute stands as a testament to collaborative marine research. Its work is not just about studying the ocean — it's about securing its future. It's important to note that the Institute plays a pivotal role in regional conservation, from kelp forests to salmon runs. Ultimately, despite these challenges, its impact continues to grow.

*After the skill's pass:*

> The Salish Sea Institute conducts collaborative marine research in the Pacific Northwest and works on regional conservation, including kelp forests and salmon runs.

The rewrite preserves the concrete information without adding facts.

## Install

Copy the folder into your agent's skills directory:

| Runtime | Path |
|---------|------|
| Claude Code | `~/.claude/skills/write-like-a-human/` |
| Codex / Copilot CLI / Gemini CLI | `~/.agents/skills/write-like-a-human/` |
| OpenCode | your configured skills directory |

No dependencies, no scripts — it's one markdown file your agent reads.

Or paste the contents of [`SKILL.md`](SKILL.md) directly into any system prompt or project instructions.

## Usage

Ask for it explicitly:

- "Use the write-like-a-human skill to clean up this draft."
- "Write a bio of our founder — run it through write-like-a-human before returning."
- "Audit this text for AI-writing tells and fix what's real."

The skill also self-limits: it won't scrub a text into flat bureaucratic gray, and it treats pattern hits as candidates, with meaning deciding what changes.

## The 21 tells, briefly

| Group | Sample tells |
|-------|--------------|
| Hype voice | inflated stakes, adjective wallpaper, facts that act, insight theater |
| Hollow authority | notability by name-drop, vague consensus, cutoff disclaimers, chat residue |
| Rhythmic tics | the rule of three, the not-only pivot, merism sprawl, synonym carousel, participle pileups, em-dash addiction, conclusion gravity |
| Structure reflexes | the "challenges and future prospects" coda, title-as-thesis, the balanced-blur ending |
| Format fingerprints | Title Case headings, bold spam, Markdown pasted into wiki markup, tracking parameters on citation URLs |

Full table with fixes lives in [`SKILL.md`](SKILL.md).

## Files

- `SKILL.md` — the skill itself (frontmatter, workflow, regex, rules)
- `README.md` — this file
- `LICENSE` — CC BY-SA 4.0 notice and attribution

## Credits

Adapted from [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) by Wikipedia contributors (CC BY-SA 4.0), rewritten, reorganized, and extended for general-purpose prose. See [LICENSE](LICENSE). Not affiliated with the Wikimedia Foundation.

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) — inherited from the source material; see [LICENSE](LICENSE). You may share and adapt this work, including commercially, provided you attribute it, link the license, indicate changes, and license shared adaptations under CC BY-SA 4.0 or a license permitted by its ShareAlike terms. No additional legal or technological restrictions may prevent recipients from exercising the licensed rights. The linked legal code governs.
