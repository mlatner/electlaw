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

## Session 2026-10-06 — Can US independents run as a formal slate? (scoping search)

Question: do any statewide or local US laws let **independent** candidates run together
as a formal slate or list? Searched state election codes. **Preliminary — statute text
read for Colorado and New York; Massachusetts and Rhode Island from secondary summaries
plus one fetch. Not exhaustive across 50 states.**

**Finding: US law gives independents a shared *label* but never a shared *list*.**
Three or four states supply a mechanism for several unaffiliated candidates to appear
under a common name, and none of them pool votes, allocate seats across the group, or
present the group as a single ballot unit.

- **Colorado, C.R.S. §1-4-802** — the petition "shall indicate the name of the minor
  political party or **designate in not more than three words the political or other name
  selected by the signers to identify an unaffiliated candidate**." But the same section
  forecloses the slate: "**Each petition must contain only the name of one candidate for
  one office**," excepting only president/vice-president and governor/lieutenant governor.
  So the designation can be shared across candidates while each files separately and
  nothing aggregates. Colorado separately defines a **"political organization"** as "any
  group of registered electors who, by petition for nomination of an unaffiliated
  candidate as provided in section 1-4-802, places upon the official general election
  ballot nominees for public office" — a group container with no list consequence.
  [`codes.findlaw.com/co/title-1-elections/co-rev-st-sect-1-4-802.html`]
- **Massachusetts political designation** — up to three words beside the name, created
  when 50 registered voters file with the Secretary; voters may themselves register under
  it. A label with a membership, still not a nomination vehicle. [secondary: sec.state.ma.us
  Candidates' Guide — **statute not yet pulled**]
- **Rhode Island, §17-19-9.1** — independents listed "in the vertical column below the
  title of the office they seek, following the listing of the political party candidates,"
  with a three-word descriptor or "independent" by default. **Correction to an earlier
  reading in session:** a search summary attributed ticket-column language to this section
  ("candidates listed as a ticket shall be given a column… and no other candidate shall
  appear in that column"). **Fetching the section did not find that language.** Treat the
  ticket-column claim as **unverified**; it may belong to another RI section.
- **New York, Election Law §6-138, "independent body"** — closest to a vehicle. The
  petition names an independent body, and that name is **exclusive per office**: it may not
  create "the possibility of confusion with… the emblem or name of an independent body
  selected by a previously filed independent nominating petition for the same office."
  **But the only joint nomination the section's text makes explicit is governor and
  lieutenant governor.** Whether one petition may carry a multi-office slate is **not
  settled by §6-138**; the petition-form section is **§6-140 and has not been read**.

**Negative finding, and the useful one: no US jurisdiction found that aggregates votes
across a group of independents.** Group voting tickets — the mechanism closest to a list —
now survive in exactly one jurisdiction worldwide, the City of Melbourne councillor ballot,
and that is Australia.

**Why this matters for the model statute.** The three-word designation is close to a
US-universal feature. It is the vestigial infrastructure for a non-party list: the label
exists, the membership can exist, the ballot already prints it. **What is missing is the
aggregation rule, not the label.** A model provision enabling independent lists therefore
does not need to invent a nomination vehicle — it needs to add vote-pooling and seat
allocation to a designation mechanism most states already have, and to relax the
one-candidate-per-petition rule that Colorado states expressly.

**Next, if pursued:** read NY §6-140; find the RI section carrying the ticket-column
language if it exists; check whether any home-rule charter in a cumulative- or
limited-voting jurisdiction groups independents; check territories (PR, GU) separately,
since their ballot structures differ from the states'.

**Distinguish from the earlier at-large/party-list work**: that line concerned whether
historical at-large *partisan* races functioned as lists. This is the unaffiliated case,
where the party vehicle is absent by definition.
