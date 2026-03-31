# AI Humanizer

Write like a human skill for Claude Code. Eliminates AI writing patterns for English and German. Enforces ceso's natural Rioplatense style for Conversational Spanish and a controlled literary Spanish for General Spanish (modeled on Borges, Onetti, and Cortázar).

## Communication

- Do not use em dashes (U+2014) in any output. Use commas, periods, colons, or semicolons instead.
- This also applies to skill templates, examples, and any example output embedded in `skills/ai-humanizer/`.

## Language Modes

- English: apply 'English Scenario'
- German: apply 'Deutsches Szenario'
- Spanish:
  - Conversational: apply 'Escenario Español - Conversacional'
  - General: apply 'Escenario Español - General'

## Structure

```
skills/ai-humanizer/
└── SKILL.md    -- all writing rules: English and German (AI pattern removal), Spanish (ceso's Rioplatense style + AI pattern removal)
```

SKILL.md is the single source of truth. No sub-agents needed.

## Verification

```bash
# Word count: SKILL.md should stay under 6000 words
wc -w skills/ai-humanizer/SKILL.md

# Name field must be "ai-humanizer"
grep 'name:' skills/ai-humanizer/SKILL.md | head -1
```

## Commit Convention

`{type}: {description}` -- types: feat, fix, refactor, docs, chore

## Release Convention

- Title: `V{version} {Codename}` -- e.g., V1.0.0 Natural
- Tag: `v{version}` (lowercase v)
- Body: HTML format, English Changelog
- Each item: `<li><strong>Category</strong>: description.</li>` -- bold label summarizes the change, description is one concise sentence, no filler words
- Style: engineer-facing, no marketing language; lead with what changed, not why it matters
- Footer: install commands `git clone https://github.com/ceso/ai-humanizer.git ~/.claude/skills/ai-humanizer` + `claude plugin marketplace add ceso/ai-humanizer && claude plugin install ai-humanizer` + star + repo link
