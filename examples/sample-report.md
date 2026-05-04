# Skill Candidates Report

**Generated**: 2026-05-03
**Workspace scanned**: `~/Novig-CEO/` (folders 01-07), Calendar snapshot, Sent email snapshot
**Time window**: 2026-01-01 to 2026-04-30 (90 days)
**Patterns analyzed**: 23 distinct clusters
**Recommended skills**: 5

---

## How to use this report

Below are skill candidates ranked by impact. Mark `[x]` next to each one you want built, then re-run skill-finder with the prompt "scaffold approved skills" and Claude will generate the SKILL.md files.

---

## Recommended skills

### 1. monthly-investor-update

- [ ] **APPROVE**

**What it does**: Drafts your monthly investor update for any of your 5 lead investors (Pantera, Forerunner, NFX, Perceptive, Lux) using this month's metrics, shipped work, regulatory state, hiring pipeline, and asks — preserving your voice and the recipient-specific framing you've used historically.
**When it fires**: First week of each month, when you say "draft the [investor] update" or open the investor folder.
**Inputs needed each run**: Current month's metrics (volume, traders, profitable rate, revenue), shipped product list, regulatory updates, hiring deltas, recipient name.
**Outputs**: Markdown draft in `01-Board-and-Investors/[Investor]-Monthly-Update-[YYYY-MM].md`, formatted to match your existing template, with recipient-specific sections (e.g., growth questions for Forerunner, regulatory framing for Pantera).
**Time saved per use**: ~25 minutes
**Frequency**: 5 sends/month (one per investor) → 20/quarter
**Confidence**: HIGH
**Underlying pattern**: 18 historical investor updates across 5 recipients in the 90-day window. Strong template match across instances. Recipient-specific framing detected (e.g., Forerunner asks always include consumer growth questions; Pantera asks always include regulatory + institutional liquidity).

---

### 2. quarterly-board-update

- [ ] **APPROVE**

**What it does**: Drafts the quarterly board update from monthly investor updates, weekly product reviews, friday wraps, and metrics — assembling the executive summary, financials, product, growth, regulatory, team, risks, and next-quarter sections in the format you've used the last 4 quarters.
**When it fires**: Two weeks before quarter-end, when you say "start the board update" or open the board folder.
**Inputs needed each run**: Three months of investor updates, three months of weekly product reviews, friday wraps, current metrics, hiring deltas.
**Outputs**: Markdown draft in `01-Board-and-Investors/Q[N]-[YYYY]-Board-Update.md` matching your historical structure.
**Time saved per use**: ~3 hours
**Frequency**: Quarterly
**Confidence**: HIGH
**Underlying pattern**: 2 historical board updates (Q4 2025, Q1 2026) with identical 9-section structure. Clear synthesis pattern from monthly artifacts. Highest time-saved per use of any candidate.

---

### 3. state-regulatory-monitor

- [ ] **APPROVE**

**What it does**: Refreshes your state regulatory tracker by scanning state legislative trackers, sweepstakes rulings, and recent inquiry/response correspondence — flagging changes vs. last month, classifying state status (permitted / restricted / inquiry / legislative review / prohibited), and surfacing strategic risks for the CFTC track.
**When it fires**: First week of each month, when you say "update the state tracker" or "run the regulatory monitor".
**Inputs needed each run**: Last month's tracker, any new inquiry correspondence, legislative bill numbers being watched.
**Outputs**: Markdown tracker in `02-Regulatory/State-Tracker-[YYYY-MM].md` with delta section showing changes vs. prior month.
**Time saved per use**: ~90 minutes
**Frequency**: Monthly
**Confidence**: HIGH
**Underlying pattern**: 3 monthly trackers in window with consistent structure (summary, table, prohibited, delta section). The "changes vs. prior month" section is the high-value synthesis work that gets repeated.

**Note**: This is the only skill candidate that needs ongoing external research (legislative trackers, news scans). Build with web research as a phase. Highest leverage candidate given your CFTC track.

---

### 4. interview-debrief-synthesizer

- [ ] **APPROVE**

**What it does**: Generates your interview debrief from your raw notes, populates the debrief template (strengths/concerns/hire decision/next-round tests), and updates a candidate-pipeline summary so you can see all final-round candidates side-by-side before deciding.
**When it fires**: After any final-round CEO interview, when you say "debrief [name]" or "log the debrief for [name]".
**Inputs needed each run**: Candidate name, role, raw notes from the interview, interview round number.
**Outputs**: Debrief file in `03-Hiring/Interview-debriefs/[YYYY-MM-DD]-[Name]-[Role]-R[N].md` plus an updated `03-Hiring/Pipeline-Summary.md` showing all open final-round candidates side-by-side.
**Time saved per use**: ~15 minutes
**Frequency**: ~6 final-round interviews/month based on hiring pace
**Confidence**: HIGH
**Underlying pattern**: 4 debrief files in window using consistent template, plus an explicit `_TEMPLATE.md` file. Pipeline-summary view doesn't currently exist — this skill creates it as a side effect.

---

### 5. friday-wrap-generator

- [ ] **APPROVE**

**What it does**: Drafts your weekly Friday Wrap from this week's product review, calendar (decisions/meetings), Slack activity, and any new hires/losses — populating wins, losses, open items, and a next-week focus section.
**When it fires**: Friday at 3pm, when you say "draft the wrap" or open the exec-cadence folder.
**Inputs needed each run**: This week's product review notes, recent hiring updates, regulatory updates, your gut sense of the energy score (skill leaves this for you to fill).
**Outputs**: Markdown draft in `05-Exec-Cadence/Friday-Wrap-[YYYY-MM-DD].md`.
**Time saved per use**: ~12 minutes
**Frequency**: Weekly
**Confidence**: HIGH
**Underlying pattern**: 3 friday wraps in window with identical 5-section structure (wins/losses/open/energy/next week). High consistency, low complexity — quick win.

---

## Considered but not recommended

Patterns we noticed but cut from the list, with one-line reasons:

- **Weekly product review compiler**: Strong recurring pattern but the meeting itself is where the synthesis happens. Skill would risk replacing the live discussion.
- **Press inquiry responder**: 7 instances detected but each response is too context-specific to template safely. Recommend a press-kit-link skill instead, but de-prioritized.
- **Candidate offer letter generator**: 11 instances but legal/comp/title sensitivity makes this high-stakes. Better handled by HR tooling.
- **Conference invite decliner**: 6 instances with simple template — too lightweight to need a skill. A saved canned response in Gmail does this.
- **CFTC application drafter**: Single high-value document, not recurring. Not a skill.
- **Q2 strategy refresh**: One-off strategic project, not a recurring workflow.
- **Weekly all-hands prep**: Pattern is real but the inputs (metrics + culture moments) are too varied to template safely.
- **Sprint summary generator**: Belongs to the eng/product team's tooling, not the CEO's.

---

## Open questions

- For the `monthly-investor-update` skill: do you want one skill that takes a `--recipient` flag, or 5 separate skills (one per investor)? One skill is cleaner; 5 lets you tune voice per recipient. Recommend one with a recipient flag, but defer to you.
- For `state-regulatory-monitor`: should this also generate a draft "update for Alex" (CLO) email summarizing the changes? Detected pattern is you forward the tracker to him each month, but only 2 instances in window.

---

## Next step

Mark `[x] APPROVE` next to the skills you want, then say **"scaffold approved skills"** and I'll generate the SKILL.md files in `~/skill-finder-output/skills/`.
