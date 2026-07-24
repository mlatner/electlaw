---
title: electlaw — decisions log
maintained: append-only, chronological by session
---

Every drafting choice, comparative-jurisdiction selection, and statutory
construction decision for the electlaw model PR legislation. Newest
sessions at the bottom.

---

## Session 2026-06-18 — Logging convention adopted

Prior model: legislation drawn from comparative non-partisan list
administration in 12 countries. (memory: `project_electlaw.md`)

Future entries: every drafting revision, every jurisdiction added/dropped,
every comparative trade-off.

---

## Session 2026-07-24 — Return to active status; project marked TOP PRIORITY

Project marked **top-of-list priority** by user 2026-07-24 (see
`project_electlaw.md` memory banner). Framework and 12 comparative
cases substantively complete since 2026-05-20. Natural next phase is
the `models/` folder (draft model US statutes), which is currently
empty.

### Housekeeping this session

Committed a bundle of five pending items sitting in the tree since
2026-05-28 and 2026-06-18:

- `framework/components/02_ballot_structure.md` (+89 lines) — the
  *Empirical evidence base* section integrating Latner's March 2026
  systematic review on voter error.
- `comparisons/ballot_error_crosswalk.md` — 12-jurisdiction ×
  ballot-architecture × evidence-row table.
- `CLAUDE.md` — project-specific Claude instructions.
- `docs/decisions_log.md`, `docs/sources_log.md` — append-only logs
  per universal convention.
- `sources/literature/*.docx` — the review PDFs cited above.

### Ten citation-level corrections propagated from ~/error blog

Before committing, propagated ten citation corrections identified in
the 2026-07-22–23 fact-check pass on the `~/error` diagnostic blog
post (companion treatment of the same evidence base). Full ledger in
`sources_log.md`. The corrections most consequential for electlaw:

- Brazil row of crosswalk: **Cheibub & Sin 2020** removed from
  invalid-rate citations (paper is about intra-party competition
  dynamics only); note added flagging this and pointing at the Chile
  row where Cheibub & Sin is correctly used.
- NSW row of crosswalk and RCV/IRV-optional row of the
  `02_ballot_structure.md` rate table: **Santucci et al. 2025 →
  Pettigrew & Radley (2026)** *Political Behavior* (likely the same
  paper, defaulted to the confirmed author-ordering).
- NSW row: **Endersby & Towle 2014** reframed as generic Irish STV
  context, not an error-rate comparison claim.
- Sociodemographic gradient bullet: education monotonicity softened.
  Kouba & Lysek meta shows significant negative average effect
  (r = 0.42, p < 0.05) but individual-study directions are 4 opposite,
  8 null, 11 confirming across 23 tests. Directional claims in
  drafting narrative must reflect the *average* effect, not a
  uniform-effect assumption.
- Brazil row note: Colombia precedent added (Pachón et al.) — ballot
  redesign *inside* an open-list system reduced invalid rates.
  Corroborates the physical-ballot-design-as-independent-lever theme
  from Scotland 2007.
- Minority-Rep Specifics #3 of `02_ballot_structure.md`: same
  Colombia point added; Carman/Mitchell/Johns 2008 Scotland 2007
  spike cited explicitly.
- Approval-voting row of the rate table: added Balinski & Laraki 2007
  (French majority-judgment experimental, ~1% invalid) as a
  corroborating cite alongside Haase Formánková 2026 (0.1%).

### Two-axis design frame adopted for cross-referencing

Adopted from `~/error/CLAUDE.md` (the companion blog series): each
case profile sits on two independent axes — **Axis 1 (Inclusive ↔
Exclusive)** governed by district magnitude / threshold of exclusion
(component 1, seat product); **Axis 2 (Candidate-centered ↔
Party-centered)** governed by ballot structure (component 2, this
document). Frame noted in the crosswalk preamble and in the
`02_ballot_structure.md` empirical-evidence-base section. When
drafting model-statute prose, place each design choice on both axes
explicitly.

### Retired framings (do not reintroduce)

- **"Cancels the PR boost"** — user rejected as too system-advocacy-
  adjacent. Blog series retired it 2026-07-22–23. Not to be used in
  electlaw prose. Diagnostic finding ("PR blow" magnitude) remains;
  the trade-off framing does not.

### Next task (deferred to next session)

Begin the `models/` folder — draft model US statutes for state and
local list-PR implementation, drawing on the completed framework +
12 comparative cases. First model to draft: a state-level list-PR
statute with the user's one-vote MMP-with-party-or-candidate-options
baseline design.
