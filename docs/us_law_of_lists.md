# The US law of list systems

*Started 2026-10-06. Working synthesis, not a finished argument. Feeds the model
statute: it establishes which components of a list ballot already exist in US law
and which have to be drafted. Sources and session-by-session findings are in
`docs/sources_log.md`; the historical research is at
`sources/us_history/at-large_straight-ticket_1889-1967.docx`.*

---

## The question

Does any US jurisdiction have, or has any ever had, the legal machinery for a
**list** — a ballot on which votes attach to a group of candidates, are pooled at
the group level, and are then converted into seats by an allocation rule?

## The distinction everything turns on

The literature and the statutes repeatedly blur two things that must stay separate:

| | What it is | Example |
|---|---|---|
| **Grouping / convenience** | Candidates appear together, or one mark reaches several of them, but each vote remains attached to a **named candidate** and each seat is **tallied as its own contest** | straight-ticket voting; NJ's county line |
| **Pooling / allocation** | Votes attach to the **group**, are summed at group level, and seats are then **distributed among its candidates** by rule | list PR; group voting tickets |

Every US mechanism found so far is on the left. The one partial exception is
Connecticut, below, and even that allocates by **cap** rather than by vote share.

**The decisive negative, from the historical research:** "In none of these states
did a voter choose only a party and then have the party allocate that vote to
candidates of its own choosing. That mechanism — a closed party list or group
voting ticket — **has never been used for U.S. congressional elections.**"

---

## Five mechanisms, none complete

### 1. The three-word designation — a shared label
**CO · MA · RI.** Several unaffiliated candidates may appear under a common name.

- **Colorado, C.R.S. §1-4-802** — petition may "designate in not more than three
  words the political or other name selected by the signers to identify an
  unaffiliated candidate," but "**each petition must contain only the name of one
  candidate for one office**" (excepting Pres/VP and Gov/Lt-Gov). Colorado also
  defines a **"political organization"** as a group of electors who place nominees
  on the ballot by §1-4-802 petition — a container with no list consequence.
- **Massachusetts political designation** — up to three words beside the name,
  created when 50 registered voters file with the Secretary; voters may register
  under it. A label with a membership.
- **Rhode Island §17-19-9.1** — independents listed in a vertical column below
  party candidates, with a three-word descriptor or "independent" by default.

**Missing:** everything downstream. The label does not nominate, group, or pool.

### 2. The fusion ballot line — a real multi-candidate grouping
**NY · CT · SC** (line-based). Distinguish from **OR · VT** (dual-labeling: one
line, several party names printed beside the name, no line-level tally).

A cross-endorsed candidate's name appears on each endorsing party's line, and the
**votes on each line are tallied separately** before being summed for the
candidate. New York's §6-138 "independent body" is a non-party line of this kind,
with a name exclusive per office.

**Why this matters more than it first appears:** summing across lines *requires*
counting each line separately. **The ballot design, the canvass, and the reporting
already support a line-level vote total**, in production, in New York and
Connecticut.

**Missing:** the allocation step. A line's votes are summed *into one candidate*
rather than apportioned *among the candidates the line carries*.

### 3. Organizational grouping across offices — enjoined
**NJ, the "county line."** The primary ballot grouped county-party-endorsed
candidates into a single row or column **regardless of office**, with unbracketed
candidates relegated elsewhere. The strongest *visual* list analog in US practice.

Held a severe First Amendment burden: **Kim v. Hanlon**, D.N.J., aff'd 3d Cir.
No. 24-1594 (Apr. 17, 2024).

**The caution to carry:** ballot grouping by organization can be held
unconstitutional **where it confers advantage without a vote-aggregation
rationale**. A list statute supplies that rationale; the county line did not.

### 4. The straight-ticket mark — block voting with a shortcut
**AL · IN · KY · MI · OK · SC** retain it (NCSL, updated 2025-12-09).

**This is not a list, and the point is easy to get wrong.** One mark cast one vote
for *each* named candidate the party had listed. Each seat was tallied as its own
contest, and a party's candidates diverged in outcome — Ohio's 1932 at-large
election returned four different major-party totals (Truax 1,206,631; Young
1,200,946; Bender 1,109,562; Palmer 1,102,567).

**Indiana abolished the straight-ticket vote for at-large elections in 2016**, on
**voter-error grounds**: voters marked straight-ticket *and then also* marked
individual at-large candidates, creating overvote ambiguity. A bipartisan effort to
restore it is live.

**The lesson for the model statute is about ballot design, not representation.**
The US withdrew its most list-adjacent multi-seat ballot because of an interaction
between a group mark and candidate marks on the same sheet. Any list ballot that
coexists with single-seat contests will face that interaction. See the March 2026
voter-error review in `sources/literature/`.

### 5. Party-keyed seat allocation — Connecticut, and only Connecticut
**Conn. Gen. Stat. §9-167a, "Minority representation."** Caps how many members of
any board, commission, or legislative body — **elected or appointed** — may belong
to one party: 2 of 3, 2 of 4, 3 of 5, 4 of 6, 5 of 7, 5 of 8, 6 of 9, two-thirds
above 9. It **exempts bodies "elected on the basis of geographical division,"** so
it operates **precisely on at-large multi-seat bodies**. **§9-188** adds
"Minority representation; **restricted voting**" for selectmen — limited voting in
statute.

**Missing:** proportionality. It is a **cap on the majority**, not an allocation by
vote share.

---

## Connecticut holds three of the five

| Component | CT | NY | Elsewhere |
|---|:--:|:--:|---|
| Multi-candidate ballot line, separately tallied | ✓ | ✓ | SC |
| Multi-seat at-large local bodies | ✓ | ✓ | most states |
| Seat allocation keyed to party | ✓ | — | — |

New York supplies the lines and the multi-seat contests; Connecticut supplies those
**and** an allocation rule.

**This reframes the drafting problem.** Connecticut does not merely permit
party-based seat allocation in at-large multi-seat elections — **it requires it,
statewide, and has since the 1950s.** The move from *"no party may hold more than
two-thirds"* to *"seats are allocated in proportion to the votes cast on each
line"* is **a change of allocation formula inside an existing legal architecture.**
The threshold constitutional questions — may a state condition local multi-seat
elections on party composition, may a non-majority party be guaranteed seats — are
already answered affirmatively and already litigated.

## What a model statute therefore has to add

1. **An allocation rule** attached to an existing line-level tally. Not a
   nomination vehicle, not a ballot format, not a canvass procedure — those exist.
2. **Relief from one-candidate-per-petition** where it is stated expressly
   (Colorado) or implied.
3. **A ballot-design answer to the Indiana failure mode**: how a group mark and
   candidate marks coexist without generating overvotes.
4. **An aggregation rationale on the record**, to distinguish the scheme from the
   county line struck down in *Kim v. Hanlon*.
5. For congressional application only: **amendment of 2 U.S.C. §2c** (Uniform
   Congressional District Act), which requires single-member districts and
   forecloses House list PR by statute regardless of the constitutional answer.

## Verification status

| Claim | Status |
|---|---|
| C.R.S. §1-4-802 one-candidate rule and three-word designation | **statute text read** |
| NY §6-138 independent-body naming and exclusivity | **statute text read** |
| NY is fusion; line is the organizing unit | owner, 2026-10-06 |
| Straight-ticket is block voting, not a list | **owner's research**, Ohio 1932 totals |
| Six straight-ticket states; Indiana 2016 at-large repeal | NCSL 2025-12-09; IN press |
| Fusion-state list incl. Oregon; line vs dual-labeling split | Brennan Center; Ballotpedia |
| **Conn. §9-167a table, scope, geographic exemption** | **CGA OLR 2017-R-0344 and Justia 2011 — statute NOT yet read directly** |
| RI §17-19-9.1 "ticket column" language | **searched for, NOT found — treat as unverified** |
| VT: 41 two-member House districts, block voting, dual-labeling | Ballotpedia/NCSL |

## Next reads

- **Conn. Gen. Stat. §9-167a and §9-188 as currently enacted** — the one load-bearing
  citation still resting on secondary sources.
- How the §9-167a cap is administered when a candidate appears on **more than one
  fusion line** — party attribution for cap purposes is unexamined.
- A Connecticut town whose at-large board election produced a **cap-binding
  result** — the worked example this needs.
- **NY Election Law §6-140**, the petition-form section, for whether one petition
  may carry a multi-office slate.
- Whether the remaining five straight-ticket states apply the mark to **multi-seat**
  races. South Carolina is the one to check first: line-based fusion *and*
  multi-seat county councils.
- Territories (PR, GU) — ballot structures differ from the states' and were not
  searched.
