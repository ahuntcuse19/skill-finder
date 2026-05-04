# Output format — skill candidates report

The report is the user-facing artifact. It must be skimmable in 90 seconds by a busy executive. Stick to this format exactly.

## Required structure

```markdown
# Skill Candidates Report

**Generated**: [ISO date]
**Workspace scanned**: [folder paths + connector list]
**Time window**: [date range]
**Patterns analyzed**: [count from discovery]
**Recommended skills**: [count, max 7]

---

## How to use this report

Below are skill candidates ranked by impact. Mark `[x]` next to each one you want built, then re-run skill-finder with the prompt "scaffold approved skills" and Claude will generate the SKILL.md files.

---

## Recommended skills

### 1. [skill-name]

- [ ] **APPROVE**

**What it does**: [one sentence]
**When it fires**: [trigger condition / user phrase]
**Inputs needed each run**: [list]
**Outputs**: [what gets produced]
**Time saved per use**: ~[N] minutes
**Frequency**: ~[N] times per [week/month/quarter]
**Confidence**: [high / medium / low]
**Underlying pattern**: [the discovery evidence — which files, calendar events, emails — that motivated this]

---

### 2. [skill-name]

[same structure]

---

[continue through max 7]

---

## Considered but not recommended

Patterns we noticed but cut from the recommendations list:

- **[pattern name]**: [one-line reason for cutting]
- **[pattern name]**: [one-line reason for cutting]

---

## Open questions

If any patterns were ambiguous or the user could clarify:

- [question 1]
- [question 2]

---

## Next step

Mark `[x] APPROVE` next to the skills you want, then say "scaffold approved skills".
```

## Tone and language conventions

- **No fluff.** Every line has to earn its place. Cut all "I noticed that..." and "It seems like..." preambles.
- **Use the user's language.** If they call it a "weekly board update", call it that. If they call it a "shareholder note", call it that. Discovery output should give you their vocabulary.
- **Lead with impact.** First sentence of "What it does" should describe the *outcome*, not the mechanism. "Drafts your monthly Pantera update from this month's metrics and qualitative notes" not "Reads files in /pantera-monthly and produces a markdown document."
- **Be honest about confidence.** A "medium confidence" candidate with strong impact is worth surfacing; mark it medium and let the user judge.
- **Show evidence.** The "Underlying pattern" line is non-negotiable. The user has to be able to verify why each candidate was promoted.

## What NOT to include

- Generic productivity tips
- Long explanations of what a skill is
- Caveats about limitations of LLMs
- Comparisons to other tools
- Anything that doesn't help the user decide which boxes to tick
