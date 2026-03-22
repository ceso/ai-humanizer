# Human

Write like a human skill for Claude Code.

## Communication

- Do not use em dashes (U+2014) in any output. Use commas, periods, colons, or semicolons instead.
- This also applies to skill templates, examples, and any example output embedded in `skills/human/`.

## Structure

```
skills/human/
└── SKILL.md    -- all writing rules: Chinese (Tw93 style) and English (AI pattern removal)
```

SKILL.md is the single source of truth. No sub-agents needed.

## Verification

```bash
# Word count: SKILL.md should stay under 4000 words
wc -w skills/human/SKILL.md

# Name field must be "human"
grep 'name:' skills/human/SKILL.md | head -1
```

## Commit Convention

`{type}: {description}` -- types: feat, fix, refactor, docs, chore

## Release Convention (tw93/miaoyan style)

- Title: `V{version} {Codename} {emoji}` -- e.g., V1.0.0 Natural
- Tag: `v{version}` (lowercase v)
- Body: HTML format, bilingual (English Changelog + 中文更新日志), one-to-one
- Each item: `<li><strong>Category</strong>: description.</li>` -- bold label summarizes the change, description is one concise sentence, no filler words
- Style: engineer-facing, no marketing language; lead with what changed, not why it matters
- Footer: update command `npx skills add tw93/human@latest` + star + repo link
