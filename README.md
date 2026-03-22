<div align="center">
  <h1>Human</h1>
  <p><em>Write like a human skill for Claude Code.</em></p>
  <a href="https://github.com/tw93/human/stargazers"><img src="https://img.shields.io/github/stars/tw93/human?style=flat-square" alt="Stars"></a>
  <a href="https://github.com/tw93/human/releases"><img src="https://img.shields.io/github/v/tag/tw93/human?label=version&style=flat-square" alt="Version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License"></a>
  <a href="https://twitter.com/AiTw93"><img src="https://img.shields.io/badge/follow-Tw93-red?style=flat-square&logo=Twitter" alt="Twitter"></a>
</div>

<br/>

A Claude Code skill that removes AI writing patterns from prose. Chinese output follows Tw93's natural conversational style; English output eliminates the tells that make AI writing recognizable.

## Install

Recommended, install globally for Claude Code:

```bash
npx skills add tw93/human -a claude-code -s human -g -y
```

Install only in the current project:

```bash
npx skills add tw93/human -a claude-code -s human -y
```

**Claude Plugin:**

```bash
claude plugin marketplace add tw93/human
claude plugin install human
```

## Usage

Restart Claude Code after installation. Then in any session, ask Claude to write or edit prose:

> "Write this in a more human style"
> "Edit this paragraph to remove AI patterns"

The skill activates automatically when writing or editing Chinese or English prose. No slash command needed.

## What Gets Checked

| Language | Rules |
| :--- | :--- |
| **Chinese** | Conversational tone (Tw93 style), vocabulary de-formalization, punctuation rules, heading design, AI pattern detection |
| **English** | Filler phrase removal, active voice, specificity, rhythm variation, word choice, sentence structure patterns |

### AI Patterns Removed

Chinese: upgrade sentences, contrast frames ("not X but Y"), repeated core points, over-formatted parallel summaries, transition bridges, isolated one-sentence paragraphs.

English: negative parallelism, rhetorical fragments, anaphora abuse, tricolon abuse, false agency, grandiose stakes inflation, pedagogical hand-holding, vague attributions.

## Scoring (English)

After editing English prose, the skill rates output 1-10 on five dimensions: Directness, Rhythm, Trust, Authenticity, Density. Below 35/50 triggers a revision.

## License

MIT License, feel free to enjoy and participate in open source.
