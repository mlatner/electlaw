# Connected areas of law

The three primary components (Seat Product, Ballot Structure,
Allocation Formula) define the *mechanics* of PR. But the mechanics
are embedded in a wider statutory and administrative environment.
A model US implementation cannot ignore the connections.

This document catalogs the connected areas at the depth needed to
explain how each one bears on the three components. Within case
studies (`case_template.md`), connected areas receive shorter
treatment than the three primary sections; in the eventual guide,
they will be shorter chapters following the three component chapters.

For the temporal sequence of these areas, see `electoral_cycle.md`
(PEI eleven-stage cycle); for performance diagnostics applied to any
provision, see `performance.md`.

---

## A. Voter eligibility and registration

Determines the **denominator** for any threshold calculation, and
shapes the equity profile of outcomes.

**Statutory questions**:
- Eligibility criteria (citizenship, residency, age, felony
  disqualification).
- Registration model (active / automatic / hybrid).
- Day-of registration, online registration, voter ID requirements.
- For local elections specifically: do non-citizens, sub-residents,
  minors vote? (Several US localities have extended local voting
  rights to non-citizens.)

**Connection to components**:
- All three: defines who casts the votes that the system counts.
- Especially salient for Component 1 (Seat Product): registration
  friction can reshape who the seat product effectively serves.

---

## B. Candidate / party / list registration

Determines **who appears on the ballot** and is upstream of all of
Component 2. The most heavily-developed connected area in the guide,
because it spans both the standard partisan-list registration
question (familiar to US ballot-access lawyers) and the more novel
question of how to register non-party lists for formally non-
partisan jurisdictions. Working systems abroad have answered the
non-party question; US local law has not.

**Statutory questions**:

### Eligible list-bearing entities
- What kinds of entities may submit candidates / lists? Registered
  party? Voter grouping / association? Citizen committee?
  Independent? Other?
- For non-partisan lists specifically: what entity type can stand,
  and under what registration regime?
- Is the entity a **standing legal entity** (registered before the
  election cycle) or **per-election** (formed for one contest)?

### Ballot access mechanics
- Signature thresholds — absolute count or scaled to district
  population / registered voters.
- Geographic distribution of signatures (anti-concentration rules).
- Monetary deposit; refund threshold (vote share or seat won).
- Filing deadlines and curing procedures.
- Equal-treatment provisions between party and non-party entities.

### List composition rules
- Minimum and maximum number of candidates on a list.
- Ordering rules (submitter-chosen, alphabetical, random).
- Gender quotas (parity, zipper, percentage threshold).
- Residency or eligibility requirements.
- Restrictions on simultaneous candidacy (multiple lists, multiple
  districts, party + independent).

### Non-partisan list labeling
- What label / identifier may a list display on the ballot?
- Categories permitted: professional association, advocacy cause,
  geographic region, ethnic affiliation, generic placeholder
  (Group A, B, C…).
- Verification authority: who confirms a list's claim to a label?
- Anti-deception rules: protection against use of party names,
  government insignia, false geographic claims.

This is the area where the **comparative cases offer the most
direct US lessons**. Working systems abroad — *Wählergemeinschaft*
(DE), *agrupación de electores* (ES), *lokale partij* (NL),
*valitsijayhdistys* (FI), *kandidatliste* (DK), *agrupación
independiente* (CL) — each present a complete answer to the question
of how a list system functions in the absence of formal parties.

---

## C. Campaign finance and disclosure

Affects whether non-party lists can compete on equal footing with
parties and shapes candidate-vs-list spending dynamics.

**Statutory questions**:
- Public funding eligibility for non-party lists.
- Donation and spending caps; whether caps apply at candidate level,
  list level, or both.
- Disclosure thresholds and reporting cadence.
- Foreign donation rules.
- Coordination rules between candidates on the same list (when does
  joint activity become "in-kind" contribution?).

**Connection to components**:
- **Component 2**: candidate-centered ballots (open list, cumulative)
  generate candidate-level spending dynamics; coalition-centered
  ballots (closed list) push spending toward list infrastructure.
- **Component 1**: high-magnitude districts make list-level
  infrastructure decisive; low-magnitude districts make individual
  candidate spending decisive.

US-specific note: post-*Citizens United* and post-*McCutcheon*
constraints on campaign-finance regulation will shape what a model
statute can require, especially in the disclosure and coordination
areas.

---

## D. Election administration and EMB structure

Determines whether the rules in Components 1–3 are actually applied
as written.

**Statutory questions**:
- EMB model: independent / governmental (under a ministry) / mixed /
  judicial?
- Centralization: single statewide body, county-by-county, hybrid?
- Independence protections: appointment process, tenure, funding.
- Authority over redistricting (Component 1), ballot design
  (Component 2), and counting (Component 3).
- Statutory rule-making authority — what can the EMB regulate
  vs. what must be in primary legislation?

Use the **PROSeS framework** (`performance.md`) as the diagnostic
lens here: process design (probity, accountability), resource
investment (transparency, sustainability), output quality
(convenience, accuracy, enforcement), service outcomes (turnout,
equity, fraud, violence), stakeholder satisfaction.

US-specific note: the dominant US pattern is **decentralized,
elected, partisan election administration at the county level**. A
PR system requires more sophisticated implementation than a
plurality count, raising questions about whether EMB capacity is a
binding constraint on local PR reform.

---

## E. Vote counting, certification, and recounts

The point at which Component 3's formula meets administrative
practice.

**Statutory questions**:
- Counting authority and chain of custody.
- Recount triggers (margin, petition, automatic).
- Audit requirements (risk-limiting audits, hand recounts).
- Certification authority and timelines.
- Tie-breaking rules.
- Special handling for list-allocation arithmetic: who computes the
  formula, who verifies, and how are computational disputes
  resolved?

US-specific note: most US jurisdictions count at the precinct /
county level and aggregate up. List PR allocation is a *jurisdiction-
wide* arithmetic step that requires a different aggregation point.
This is a non-trivial implementation detail.

---

## F. Election dispute resolution

The forum in which the entire statutory edifice is enforced.

**Statutory questions**:
- Pre-election dispute forum (ballot access, list challenges).
- Post-election dispute forum (results, eligibility,
  irregularities).
- Standing rules (candidates only? voters? watchdogs?).
- Filing costs and accessibility.
- Timelines and standards of review.
- Appeals chain.

US-specific note: existing US election-contest jurisprudence is
mostly adapted to plurality elections. List-allocation contests will
present new question types (e.g., contests over a single seat that
turn on whether a specific ballot was correctly attributed to a
list).

---

## G. Media access

Less central to the mechanics but bears on Component 2 (ballot) and
list visibility.

**Statutory questions**:
- Public broadcaster equal-time rules.
- Treatment of party vs. non-party lists.
- Online and digital advertising regulation.
- Debate participation rules.

US-specific note: the *Equal Time* rule (47 USC §315) and FCC
regulations may need adjustment for non-party lists.

---

## H. Districting law

Strictly speaking, this is part of Component 1, but the body of law
governing how districts are drawn is dense enough to deserve a
connected-area note.

**Statutory questions**:
- Authority for drawing district lines (legislature, commission,
  charter body).
- Statutory criteria (population equality, contiguity, compactness,
  community of interest, partisan fairness, minority protection).
- Frequency and triggering events for redistricting.
- Public participation rules.
- Judicial review standards.

US-specific note: VRA Section 2 and *Reynolds v. Sims* dominate this
area. Redistricting reform is a substantial body of US law that
need not be reinvented for PR — but PR with varying magnitudes
introduces wrinkles that purely single-seat redistricting law has
not addressed.

---

## How connected areas appear in the deliverable

In **case studies** (`case_template.md`), each connected area gets
a short subsection with statutory citations and notes on how the
provision bears on the three primary components.

In the **eventual guide**, connected areas appear as shorter
chapters following the three component chapters, framed as "design
choices that interact with the mechanics." The guide's depth
allocation:

- **Heavy**: Components 1, 2, 3 — full chapters with US drafting
  recommendations and model language for federal, state, and local
  applications.
- **Substantial**: Connected B (list / candidate registration) —
  spans both standard partisan ballot access and the novel
  non-partisan list registration regime needed for many US local
  charters.
- **Moderate**: Connected D (EMB), E (counting / certification), H
  (districting) — each with US-specific implementation notes.
- **Brief**: Connected A (voter eligibility), C (campaign finance),
  F (dispute resolution), G (media) — each with cross-references
  to their dominant bodies of law.

The guide's **levels-of-government** treatment will appear within
each chapter, distinguishing federal, state, and local
implementation paths rather than as a separate section. Non-partisan
local elections are a subsection within Component 2 (ballot
structure) and Connected B (list registration), where the design
problem is most distinctive.
