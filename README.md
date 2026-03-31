> Fork of [tw93/human](https://github.com/tw93/human). Thanks to [Tw93](https://twitter.com/AiTw93) for the original skill. Check the [original repo](https://github.com/tw93/human) for the Chinese writing scenario and English upstream updates.

<div align="center">
  <h1>AI Humanizer</h1>
  <p><em>Write like a human skill for Claude Code. v1.0.1</em></p>
  <a href="https://github.com/ceso/ai-humanizer/stargazers"><img src="https://img.shields.io/github/stars/ceso/ai-humanizer?style=flat-square" alt="Stars"></a>
  <a href="https://github.com/ceso/ai-humanizer/releases"><img src="https://img.shields.io/github/v/tag/ceso/ai-humanizer?label=version&style=flat-square" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License"></a>
</div>

<br/>

A Claude Code skill that enforces ceso's natural Rioplatense style for Spanish and removes AI writing patterns from prose in English and German.

## Install

**Repository cloning:**

```bash
git clone https://github.com/ceso/ai-humanizer.git ~/.claude/skills/ai-humanizer
```

**Claude Plugin:**

```bash
claude plugin marketplace add ceso/ai-humanizer
claude plugin install ai-humanizer
```

## Usage

Restart Claude Code after installation. Then in any session, ask Claude to write or edit prose:

> "Write this in a more human style"
> "Edit this paragraph to remove AI patterns"
> "Review the following text"
> "Could you help me to improve my text?"

The skill activates when writing or editing English, Spanish, or German prose. No slash command needed.

## What Gets Checked

| Language | Rules |
| :--- | :--- |
| **English** | Filler phrase removal, active voice, specificity, rhythm variation, word choice, sentence structure patterns |
| **Spanish** | Conversational tone (ceso style), filler phrase removal, active voice, vocabulary de-formalization, sentence structure patterns |
| **German** | Filler phrase removal, active voice, specificity, rhythm variation, word choice, sentence structure patterns, formal register reduction |

### AI Patterns Removed

All three languages: negative parallelism, rhetorical self-questions, anaphora abuse, tricolon abuse, false agency, grandiose stakes inflation, pedagogical hand-holding, vague attributions, false suspense transitions, invented concept labels, dramatic fragmentation, bold-first bullets, fractal summaries, signposted conclusions.

Spanish: additionally enforces ceso's natural Rioplatense vocabulary and conversational style (voseo, Uruguayan register).

German: additionally handles formal register reduction and German-specific AI jargon.

## Scoring

After editing prose, the skill rates output 1-10 on five dimensions: Directness, Rhythm, Trust, Authenticity, Density. Below 35/50 triggers a revision.

## Credits

Original skill by [Tw93](https://github.com/tw93/human). This fork replaces the Chinese scenario with Spanish and German while keeping the English rules intact.

## License

MIT License, feel free to enjoy and participate in open source.
