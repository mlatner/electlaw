---
title: electlaw — sources log
maintained: append-only, chronological by session
---

Every statutory source, code citation, legal database lookup, and
comparative-law reference for the electlaw model PR legislation project.

Newest sessions at the bottom.

---

## Session 2026-06-18 — Logging convention adopted

Prior state from memory: model PR legislation drawn from comparative
non-partisan list administration in 12 countries. (memory: `project_electlaw.md`)

Pre-existing literature base: Latner's March 2026 systematic review on
ballot complexity, voter error, and invalid votes (30+ studies). Already
integrated into electlaw at `sources/literature/`. (memory:
`reference_voter_error_review.md`)

Future entries: every statutory text consulted, every comparative-law
citation added, every secondary-source citation.

---

## Session 2026-07-24 — Voter-error citation corrections propagated from ~/error

The `~/error/posts/2026-07-22-ballot-error-diagnostic/` blog post ran a
systematic fact-check pass on 2026-07-22–23 against primary PDFs
(logged at `~/error/docs/decisions_log.md`, session
2026-07-22 to 2026-07-23). Ten citation-level corrections were
identified. Those affecting electlaw have been propagated into
`comparisons/ballot_error_crosswalk.md` and
`framework/components/02_ballot_structure.md`:

1. **Aldashev & Mastrobuoni** — year standardized to **2019** (published
   PSRM version); earlier drafts used "2010" and "2013" inconsistently.
   Not yet cited in electlaw files; recorded for future use.

2. **Colombia timeline** — the ~13% invalid rate is under a specific
   ballot design used in 2006/2010, *after* the 2003 open-list reform,
   not pre-2003 (Pachón et al. p. 99–100). Ballot redesign *inside*
   the open-list era reduced rates. Corroborates the physical-ballot-
   design-as-independent-lever theme in the Scotland 2007 row. Applied
   in Brazil row of crosswalk and in Minority-Representation Specifics
   #3 of `02_ballot_structure.md`.

3. **"Education … always in the same direction"** — false. Kouba &
   Lysek 2019 Table 1 (p. 755): 11 hypothesized-direction tests break
   down as 4 opposite, 8 null, 11 confirming across 23 total. Overall
   meta effect r = 0.42, p < 0.05 (significant negative), but
   individual tests not uniformly directional. Applied in
   Sociodemographic Gradient bullet of `02_ballot_structure.md` and in
   Brazil-row note of crosswalk. **Rule for future drafting**:
   directional claims about education in drafting narrative should
   reflect the *average* meta-analytic effect, not a uniform-effect
   assumption.

4. **"Fifty-four studies" meta-analytic aggregation** — imprecise.
   Kouba & Lysek review 54 studies but meta-analyze 28 of them (37
   models, 129 tests). Applied in Sociodemographic Gradient bullet of
   `02_ballot_structure.md`.

5. **Balinski & Laraki 2011** — the "range or grading" generic
   citation was replaced with **Balinski & Laraki 2007** French
   majority-judgment experimental study (~1% invalid). Applied to
   Approval-voting row of the `02_ballot_structure.md` rate table.

6. **Alós-Ferrer & Granić 2012** — repositioned as *corroborating*
   approval-voting field-experiment cite, not the source of the 0.1%
   number (which is Haase Formánková 2026). Not currently cited by
   name in electlaw files; recorded for future use.

7. **Cheibub & Sin 2020** — the paper is about intra-party competition
   dynamics under open-list PR, **not** invalid-vote rates. The
   crosswalk previously cited Cheibub & Sin 2020 in the Brazil row's
   "key citations" for the invalid-rate figure — corrected to remove
   from that role. Cheibub & Sin correctly cited in the Chile row for
   intra-party competition dynamics, and flagged in the Brazil row's
   citations column as "not to invalid-vote rates — see Chile row."

8. **Kimball & Kropf 2005** — dropped from the FPTP-equipment
   sentence in the source review (their paper is about ballot design
   more than equipment). Ansolabehere & Stewart 2005 alone carries
   the 0.5–1.5% / 2–3% US residual number. `02_ballot_structure.md`
   FPTP-row already cites Ansolabehere & Stewart alone; verified
   consistent.

9. **Santucci et al. 2025 → Pettigrew & Radley 2026** — likely the
   same paper (Overvotes / overranks / skips) cited under two
   different author-orderings across sources. Defaulted to Pettigrew
   & Radley (2026) *Political Behavior* per Högström (2026) citation.
   Applied to NSW row of crosswalk and to RCV/IRV-optional row of
   `02_ballot_structure.md` rate table.

10. **Endersby & Towle 2014** — dropped the "Irish STV lower than U.S.
    RCV" synthesis claim (not verified in the primary paper).
    Reframed as generic Irish STV context. Applied to NSW row of
    crosswalk.

**Companion diagnostic post**: `~/error/posts/2026-07-22-ballot-error-diagnostic/`
is the parallel treatment of the same evidence base, organized by
*findings* rather than by ballot type. When drafting electlaw prose
that touches ballot error, cross-reference the blog's findings-keyed
structure. The retired **"cancels the PR boost"** framing (user
rejected as too advocacy-adjacent) does not appear anywhere in
electlaw; retirement noted for future sessions.

**Two-axis frame** adopted for cross-referencing: `~/error/CLAUDE.md`
uses (Axis 1 Inclusive ↔ Exclusive = component 1, seat product) ×
(Axis 2 Candidate-centered ↔ Party-centered = component 2, ballot
structure). Crosswalk preamble and `02_ballot_structure.md` header
note this frame explicitly.
