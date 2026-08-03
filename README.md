# Awesome Suno Prompting

A curated list of tools, guides and references for writing prompts that Suno actually follows.

Suno never shipped a prompting manual. What exists is scattered across forum threads, tool landing pages and people's private notes. This list collects the parts that hold up.

## Contents

- [Start here](#start-here)
- [Prompt anatomy](#prompt-anatomy)
- [Prompt tools](#prompt-tools)
- [Prompt libraries](#prompt-libraries)
- [Guides and references](#guides-and-references)
- [Communities](#communities)
- [Contributing](#contributing)

## Start here

Three complaints account for most "Suno ignored my prompt" reports, and they have different causes:

1. **The prompt gets overridden.** Usually a contradiction inside your own prompt, or a token Suno reads as flavour rather than instruction.
2. **The vocal drifts across sections.** Nothing pinned the register, so nothing holds it.
3. **An artist name gets refused.** Names are the fastest way to describe a sound and the one thing you cannot use.

Most tools address the first and ignore the other two. Keep that in mind while reading the table below.

## Prompt anatomy

A short field guide. These are working notes from repeated generation, not official documentation, so treat them as starting points and test against your own output.

| Field | What it controls | Common mistake |
|---|---|---|
| **Style** | Genre, mood, instruments, vocal character, production, era | Stuffing it with mood adjectives that carry no sonic information |
| **Lyrics** | Everything that gets sung, plus structure tags | Writing stage directions as plain text, so they get sung |
| **Exclude / negative** | What to keep out | Leaving it empty, which is the most common omission of all |
| **Title** | Nothing about the sound | Expecting it to influence the track |

Specific rules that survived testing:

- **Anything in the Lyrics field that is not inside `[ ]` gets sung.** Instrumental directions belong in bracketed form: `[Outro | fade out | tape stop]`, never as a bare line.
- **Do not write a numeric BPM.** `128 BPM` reads as a descriptor, not a tempo, and when it conflicts with the genre the genre wins. Describe the tempo instead: `driving four-on-the-floor`, `half-time`, `unhurried`.
- **Do not lock a musical key.** It constrains the model without improving anything you can hear.
- **Ambience goes in asterisks**, Suno's own sound-effect format: `*rain on a window*`. Written as an instrument, it comes back as a synth pad.
- **Section tags shape arrangement:** `[Intro]`, `[Verse]`, `[Pre-Chorus]`, `[Chorus]`, `[Bridge]`, `[Outro]`. Ordering them explicitly is the cheapest fix for a song that arrives at its hook too late.
- **Newer Suno models read plain descriptive sentences better than stacked keywords.** A prompt that needed a generator in 2024 may just need rewriting as a sentence.

## Prompt tools

| Tool | Free to start | Signup | Writes an exclude field | Starting point | Also makes audio |
|---|---|---|---|---|---|
| [Sunomarket](https://sunomarket.com) | Limited preview | For saving | Yes | 1,960 style recipes, 1,003 artist recipes | No |
| [SunoPrompt](https://sunoprompt.com) | Free credits | Not for prompts | Not stated | Blank box, plus image/video/audio input | Yes |
| [Suno Prompt Generator Pro](https://sunometatagcreator.com) | Free credits | Yes | Not stated | Blank box plus a metatag library | No |
| [SunoPrompter](https://www.sunoprompter.com) | Yes | No | Constraints field | Blank box | No |
| [Suno Prompt Builder](https://sunobuilder.com) | Yes | No | Not stated | 50+ genres, 200+ instruments | No |

Claims checked against each tool's own site on 2026-08-03. Pricing and limits in this niche change monthly; read the pricing page before paying.

Longer writeups comparing the same five tools:

- [Best Suno prompt generators in 2026, compared](https://sunomarket.com/blog/best-suno-prompt-generators-compared), written by the maintainer of this list. See the disclosure below.
- [Best Suno Prompt Generators & Lyrics Tools, ranked and tested](https://hookgenius.app/learn/best-suno-prompt-tools/), written by the makers of HookGenius, who rank themselves first and say so.

Reading both is more useful than reading either.

## Prompt libraries

Collections you can copy from instead of starting at a blank field.

- [Sunomarket catalog](https://sunomarket.com/catalog) - 1,960 style recipes, filterable by genre, mood, tempo and instrumentation. A free preview is open, the rest sits behind an account.
- [Sunomarket artist recipes](https://sunomarket.com/artists) - 1,003 recipes that describe an artist's sound in descriptors rather than the name, which is the workaround for refused names.
- [best-suno-ai-prompts](https://github.com/AlijeeWrites/best-suno-ai-prompts) - a free GitHub collection of prompts across 170+ genres and styles.

## Guides and references

- [Suno Wiki](https://www.suno.wiki/) - community-maintained reference on styles, genres and field behaviour.
- [Sunomarket guides](https://sunomarket.com/guides) - 12 guides on prompt structure, vocals, lyrics and section tags.
- [Suno](https://suno.com) - the product itself. Its own docs and changelog are the only authoritative source on model behaviour.

## Communities

- [r/SunoAI](https://www.reddit.com/r/SunoAI/) - the main hub. Most reproducible prompting advice originates here.
- [r/AI_Music](https://www.reddit.com/r/AI_Music/) - smaller, broader than Suno alone, occasionally more technical.

## Contributing

Pull requests welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). In short: one entry per PR, say what it does in a sentence, and disclose it if you built it.

## Disclosure

This list is maintained by the person who builds [Sunomarket](https://sunomarket.com), which appears in it. Competing tools are listed alongside it with their genuine advantages stated, links are unpaid, and no entry was included or excluded in exchange for anything. If you think the framing is unfair to a tool, open an issue and argue the case.

## License

[CC0 1.0](LICENSE). Take it, fork it, republish it.
