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

**Correction, same session (owner): New York is a fusion state, and that changes what the
"independent body" is.** Under fusion the organizing unit on a New York ballot is the
**line**, not the candidacy — a candidate may occupy several lines at once, and a line may
carry candidates across multiple offices. So §6-138's independent body is properly
characterized as a **non-party ballot line**, not as a slate mechanism. The right
comparison is to a party line (Working Families, Conservative), not to a group of
independents filing together.

Two consequences, pulling in opposite directions:

1. **It weakens the independent-slate reading.** An independent body in practice is often a
   vehicle for cross-endorsement — giving an existing major-party candidate an additional
   line — rather than for genuinely unaffiliated candidates running as a group. The
   exclusivity rule in §6-138 (no confusing name "for the same office") is line-protection,
   which is what fusion requires; it is not evidence of slate formation.
2. **It strengthens the structural point.** New York already prints **ballot lines that are
   not parties and that carry multiple candidates across offices as a visual unit.** That
   is structurally the closest thing in US law to a list. The line exists; the membership
   exists; the ballot already groups by it. What is still absent is **vote-pooling and seat
   allocation across the line** — the same gap as in Colorado, Massachusetts, and Rhode
   Island, but reached from a different direction.

**Revised summary of the finding.** Two distinct US mechanisms get partway to a non-party
list, and neither aggregates:
- the **three-word designation** (CO, MA, RI) — a shared label attached to individually
  nominated candidates;
- the **fusion ballot line** (NY) — a genuine multi-candidate grouping, printed as a unit,
  available to non-parties.

The fusion line is the better model for a US list-PR statute, because the grouping already
exists in law and on the ballot. The statutory work is to attach an allocation rule to a
line, not to invent a vehicle. **Worth checking the other fusion states — Connecticut,
Delaware, Idaho, Mississippi, New York, South Carolina, Vermont** — for whether any
already pools votes by line in a multi-seat context. [list of fusion states **unverified**,
from general knowledge; confirm before relying on it]

### Follow-up: do any fusion states pool by line in a multi-seat context? **No — and the reason is structural.**

**Fusion-state list confirmed** (Brennan Center, *More Choices, More Voices*; Ballotpedia;
Wikipedia, *Electoral fusion in the United States*): **Connecticut, Delaware, Idaho,
Mississippi, New York, South Carolina, Vermont**, plus **Oregon**. Active in practice only
in **New York and Connecticut**; not practiced in Idaho or Mississippi. The earlier
unverified list was correct but omitted Oregon.

**There are two different mechanisms under the word "fusion," and the difference is the
whole answer:**

1. **Line-based fusion (CT, NY, SC).** "A cross-endorsed candidate's name appears on the
   ballot as many times as he or she is chosen as a party's nominee, with the candidate's
   **votes on each party's ballot added together**." Separate lines, **separately tallied**,
   then summed for the candidate.
2. **Dual-labeling (OR, VT).** The candidate appears on **one** line with all endorsing
   party names printed beside the name. No separate lines, therefore no line-level tally.

**Vermont is the decisive test, and it fails.** Vermont is the one fusion-list state with
substantial multi-member districts — **41 two-member House districts, 82 of 150
representatives** — elected by **block voting**. But Vermont is a *dual-labeling* state, so
it has no ballot lines to pool. Conversely the states that do have real lines (NY, CT, SC)
elect legislators from **single-member** districts, where there is nothing to allocate.

**So the multi-seat case and the ballot-line case never coincide in US law.** That is the
gap, stated precisely, and it is a structural accident rather than a prohibition.

**The genuinely useful corollary.** Line-based fusion means **New York and Connecticut
already tally votes by line and already report line-level totals** — the ballot design, the
canvass, and the reporting all support it, because summing across lines requires counting
each line separately first. The administrative machinery for a list vote therefore
**already exists and is already in production** in two states.

What a list-PR statute would have to add is **only the allocation step**: instead of summing
a line's votes into one candidate, apportion the line's votes into seats among the
candidates carried on that line. Nothing about nomination, ballot printing, or canvassing
would need inventing.

**This is the strongest available US hook for a model statute.** It should be checked
against the actual CT and NY canvass statutes and against a real returns file before being
relied on. **Not yet done:** NY Election Law §6-140 (petition form); the CT and NY canvass
provisions governing line-level tallies; whether any municipality in a line-based fusion
state uses multi-seat at-large council elections, which would put both halves in one
jurisdiction.

### Follow-up 2: straight-ticket voting — the US *did* have a closed-list multi-seat ballot, and repealed it in 2016

**Straight-ticket voting + a multi-seat race is, mechanically, a closed-list vote**: one
mark casts votes for a party's entire slate in that contest. This is the closest thing in
US law to a list ballot, and it is not hypothetical.

**Six states retain straight-ticket voting** (NCSL, updated 2025-12-09): **Alabama,
Indiana, Kentucky, Michigan, Oklahoma, South Carolina**.

**Indiana is the case.** Indiana **abolished the straight-ticket vote for at-large
elections in 2016**, retaining it for all other partisan races. Before that change, a
single straight-ticket mark cast votes for a party's **whole at-large slate** on county
and town councils — a closed-list vote in all but name, in a US jurisdiction, within the
last decade. After 2016 a straight-ticket mark "no longer records any votes in races where
the voter is required to choose multiple candidates," and voters must mark each at-large
candidate individually.

**The stated reason for the repeal is directly in our wheelhouse.** Counties reported
ballots where voters selected straight-ticket **and then also marked individual at-large
candidates**, creating ambiguity about intent and potential overvotes. That is a ballot-
complexity and invalid-vote problem of exactly the kind catalogued in the March 2026
systematic review (see `sources/literature/`, memory `reference_voter_error_review`).
**The US abandoned its one working list-style multi-seat ballot on voter-error grounds,
not on representational ones.** That is a finding the model statute has to answer, because
the same interaction will recur in any list ballot that coexists with single-seat races on
the same sheet.

**It is live.** A bipartisan Indiana effort is pushing to **restore** straight-ticket votes
to at-large races (Rep. Payne; Senate Elections committee testimony pressing for clearer
ballot instructions). Worth tracking: the instruction-design question is the same one a
list ballot faces.

**New Jersey's "county line"** is the strongest *visual* list analog — the primary ballot
grouped county-party-endorsed candidates into a single row or column **regardless of
office**, with unbracketed candidates pushed to separate columns ("Ballot Siberia"). But it
is placement, not aggregation: votes were never pooled. It was enjoined as a severe First
Amendment burden, **Kim v. Hanlon**, D.N.J., aff'd **3d Cir. No. 24-1594 (Apr. 17, 2024)**.
A cautionary precedent: organizational grouping on a ballot can itself be held
unconstitutional when it confers advantage without a vote-aggregation rationale.

**Revised bottom line across all three follow-ups.** US law has supplied every component of
a list ballot at some point, in some jurisdiction — a shared non-party label (CO, MA, RI),
a multi-candidate ballot line with line-level tallies (NY, CT, SC), organizational grouping
across offices (NJ, now enjoined), and **a single mark casting a whole multi-seat slate
(Indiana, until 2016)**. What has never existed is **one jurisdiction holding the
components together with a seat-allocation rule attached.**

**Next check, and it is the important one: do any of the remaining five straight-ticket
states apply the straight-ticket mark to multi-seat races?** South Carolina has multi-seat
county councils and is also a line-based fusion state, which would put grouping and
multi-seat in one jurisdiction. Alabama, Kentucky, Michigan, Oklahoma all have multi-seat
local bodies. **If any one of them still counts a straight-ticket mark across an at-large
slate, there is a live US closed-list ballot in production right now.** Not yet verified.

### ANSWER: Connecticut. Multi-seat at-large local bodies, ballot lines, **and a party-based seat-allocation rule already in statute.**

**Conn. Gen. Stat. §9-167a, "Minority representation."** Caps the number of members of any
board, commission, legislative body, committee or similar body — **elected or appointed** —
who may belong to the same political party:

| Total membership | Max from one party |
|---:|---:|
| 3 | 2 |
| 4 | 2 |
| 5 | 3 |
| 6 | 4 |
| 7 | 5 |
| 8 | 5 |
| 9 | 6 |
| >9 | two-thirds |

It applies to "most governmental bodies of the state, its municipalities, and other
political subdivisions," and — decisively for this question — **exempts bodies "elected on
the basis of geographical division."** The exemption means the statute operates **precisely
on at-large multi-seat bodies**. Related: **§9-188**, selectmen, carries "Minority
representation; **restricted voting**" — i.e. limited voting, in statute, for an at-large
multi-seat office.

**Connecticut therefore holds all three components in one jurisdiction:**
1. **Line-based fusion** — separate ballot lines, each tallied separately before being
   summed (established in follow-up 1);
2. **Multi-seat at-large local bodies** — the bodies §9-167a was written for;
3. **A seat-allocation rule keyed to party** — the cap itself.

This is the demonstration case the model statute needed, and it reframes the drafting
problem. Connecticut does not merely permit party-based seat allocation in multi-seat
at-large elections; **it requires it, statewide, and has since the 1950s.** The move from
"no party may hold more than two-thirds" to "seats are allocated in proportion to the votes
cast on each line" is **a change of allocation formula inside an existing legal
architecture**, not the construction of a new one. The harder questions — may the state
condition local multi-seat elections on party composition at all, may a ballot group
candidates by organization, does a non-majority party get guaranteed seats — Connecticut
has already answered affirmatively, and the law has been tested (see CGA OLR, *Constitutionality
of Minority Representation Law*, 95-R-1368).

**Caveats, to resolve before relying on this.**
- The table and scope above are from **CGA Office of Legislative Research reports**
  (2017-R-0344; 95-R-1368) and Justia's 2011 codification, **not from a direct read of the
  current statute**. Pull the operative text from the current General Statutes before citing.
- §9-167a is a **cap, not a quota**. It guarantees a minority party *at most* a floor by
  limiting the majority; it does not allocate in proportion to votes. The distinction
  matters for how the model provision is framed.
- Whether the cap interacts with fusion lines in practice — e.g. how a cross-endorsed
  candidate's party is determined for cap purposes — is **unexamined** and is the obvious
  next question.
- **New York is the weaker parallel but worth noting**: village boards are typically a mayor
  plus four trustees **elected at-large**, in a line-based fusion state, but with no
  allocation rule attached. NY supplies the lines and the multi-seat contest; Connecticut
  supplies those *and* the allocation rule.

**Next:** read §9-167a and §9-188 as currently enacted; find how the cap is administered
when a candidate appears on more than one line; and identify a Connecticut town whose
at-large board election has produced a cap-binding result, which would be the worked
example for the paper.

### CORRECTION to follow-up 2 — straight-ticket is a block vote, not a closed list

Owner supplied prior research: **"At-Large Congressional Elections and Straight-Ticket
Voting, 1889–1967"**, ~3,100 words, filed at
`sources/us_history/at-large_straight-ticket_1889-1967.docx`. It answers the question this
session was circling and **corrects an overstatement I made above.**

**I wrote that Indiana's pre-2016 at-large straight-ticket vote was "a closed-list vote in
all but name." That is wrong.** The document is explicit:

> "Where a straight-ticket option existed, one mark cast **one vote for each candidate that
> party had listed** — transparently and with no party discretion: the mark mechanically
> attached the voter's vote to specific, named, publicly known candidates, and the party
> chose its slate beforehand through nomination, **never afterward through allocation**.
> This did not mean the party's candidates won or lost together… each seat or post was
> tallied as its own contest. A party's candidates therefore drew different totals and
> could diverge in outcome."

So straight-ticket in a multi-seat race is **block voting with a convenience mark**. Three
features distinguish it from a list, and all three are decisive:
1. votes attach to **named candidates**, never to the party;
2. **each seat is tallied as its own contest**;
3. a party's candidates **diverge in outcome** — demonstrated in Ohio's 1932 at-large
   election, where the major-party candidates drew distinct totals (Truax 1,206,631; Young
   1,200,946; Bender 1,109,562; Palmer 1,102,567).

**The document's central negative finding is cleaner and stronger than anything I found
today:** "In none of these states did a voter choose only a party and then have the party
allocate that vote to candidates of its own choosing. That mechanism — a closed party list
or group voting ticket — **has never been used for U.S. congressional elections.**"

It also records **New Mexico's designated-post system** — two at-large seats run as two
separate head-to-head contests (1966: Morris v. Cook; Walker v. Davidson) — as a third
pattern that is not a list either.

**Caveat the document states about itself:** the at-large data (years, seat counts) is
solid and well-sourced; the **straight-ticket column is looser**, since no single source
gives a clean year-by-year national roster across eight decades. Straight-ticket was the
norm — a majority of states into the 1960s — so the base rate of overlap is high, but any
individual state-year needs that state's election code for that year. **Hawaii cannot be
confirmed.**

**Part II of the document** takes up whether a state party-list ballot would be
unconstitutional, separating the Elections Clause "Manner" question from the statutory one,
and notes the threshold point that **2 U.S.C. §2c (Uniform Congressional District Act)
requires single-member districts**, so party-list for the U.S. House is statutorily
precluded regardless of the constitutional answer. This is the provision the Carnegie
packet's reform program already targets for amendment.

**How this bears on today's findings.** It sharpens rather than undercuts them. The
distinction the document draws — grouping and convenience versus **party-level pooling and
post-hoc allocation** — is the same line that separates every US mechanism found today from
an actual list. Connecticut §9-167a remains the strongest finding precisely because it is
the one place where **allocation by party happens at all**, even as a cap rather than a
quota.
