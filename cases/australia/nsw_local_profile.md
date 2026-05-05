# New South Wales — Local council elections

## 0. Case metadata

- **Country**: Australia (Commonwealth)
- **Sub-jurisdiction**: New South Wales (NSW)
- **Level of government**: Local — *Council* (general
  municipal-equivalent body); some councils divided into wards,
  others undivided.
- **Electoral system family**: **Optional preferential
  proportional representation (OPPR)** with **above-the-line
  group voting** for multi-seat wards and undivided councils.
  Mayoral elections separate.
- **Governing statute (primary)**: *Local Government Act 1993*
  (NSW), Part 4 of Chapter 10 ("Elections and other electoral
  matters"). Sections **308A** (grouping of candidates),
  **308B** (group voting — recording of votes), **308C** (group
  voting — marking of ballot-papers), and **308D** (group
  voting — regulations) are the architectural keystones. Vote
  counting and quota rules are in Schedule 4 of the Act.
- **Implementing regulation**: *Local Government (General)
  Regulation 2021* (NSW), Chapter 10 and forms.
- **Citation**: Local Government Act 1993 (NSW) No 30, in force
  as at 19 September 2025.
- **URLs**:
  - <https://legislation.nsw.gov.au/view/whole/html/inforce/current/act-1993-030>
  - AustLII alt: <https://www5.austlii.edu.au/au/legis/nsw/consol_act/lga1993182/>
- **Constitutional anchor**: New South Wales Constitution Act
  1902 (NSW); local government is a creature of state law per
  the Australian federal structure.
- **EMB**: *NSW Electoral Commission* (NSWEC) administers all
  NSW state and council elections.
- **Last regular election**: 14 September 2024 (next: 2028).
- **Analyst**: (this profile, 2026-05-05)
- **Source-retrieval note**: NSW legislation servers and AustLII
  are currently behind Cloudflare protection that blocks this
  analyst's automated retrieval. Substantive content below
  draws from the NSW Electoral Commission's official candidate
  handbook, the NSWEC's published "Distribution of Preferences"
  procedural reports, and section-level descriptions from
  authoritative secondary sources. Verbatim primary text for
  ss 308A–308D is identified as **outstanding** at the end of
  this profile and should be retrieved when access permits.

### Why this case is in the project

Three reasons make NSW local councils the project's **most
analytically central Australian case**:

1. **Above-the-line group voting** under § 308C LGA gives voters
   the choice between a single group mark and full candidate-
   level preferences — the exact design pattern the user has
   identified as the working baseline for the model statute.
2. **Optional preferences below the line** (under the LGA Part
   IV, Schedule 4 counting rules) mean that a voter who marks
   only above the line is treated differently from a voter who
   marks below the line — a drafting solution to the
   "what does a list mark mean?" problem.
3. **NSW retained the older above-the-line architecture** even
   after the 2016 federal Senate reform abolished group voting
   tickets at the Commonwealth level. NSW local thus preserves
   the simplest above-the-line interface in any current
   Australian jurisdiction — single mark, votes flow within
   the group only.

NSW local is also a useful **scale comparator**: with 128
councils across NSW and elections every four years, NSW runs
more above-the-line group-voted contests in a single cycle than
the Commonwealth Senate runs in a generation. The 14 September
2024 NSW local elections involved approximately 4,500
candidates across 128 councils.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Council size

Council size is set by each council's individual constitution
under the LGA — typically **5, 7, 9, 12, or 15 councillors**,
selected at the time of council establishment or amalgamation.
Larger metropolitan councils (e.g., Blacktown City Council)
have 15 councillors; smaller rural councils have 5. The
distribution across NSW is approximately:

- 5 councillors: small rural councils
- 7–9 councillors: mid-size councils
- 12–15 councillors: large metropolitan councils

A council may be **divided into wards** or **undivided**
(at-large). The choice affects district magnitude:

- **Undivided council**: M = total council size (5–15).
- **Ward-divided council**: M = total council size ÷ number of
  wards. Typically 3-seat wards in larger councils.

### Ward structure

Most large NSW metropolitan councils are ward-divided to
preserve geographic representation. A typical ward has **3
councillors elected proportionally**. This produces a Droop-
quota threshold of exclusion of:

- 3-seat ward: 1 / (3 + 1) = 25% of formal first-preference
  votes — relatively high.
- 5-seat ward (uncommon): 1 / 6 = 16.7%.
- Undivided 9-seat council: 1 / 10 = 10%.
- Undivided 15-seat council: 1 / 16 = 6.25%.

### Operationalized values

```
total_seats:                     5, 7, 9, 12, or 15 per council
codification_instrument:         Local Government Act 1993 (NSW)
                                 (council size set in council's
                                 constitution)
amendment_authority:             Local council (subject to
                                 regulatory oversight)
amendment_threshold:             ordinary council resolution

magnitude_uniform:               no — varies by ward design
magnitude_typical:               3 (ward-divided councils);
                                 5–15 (undivided councils)
magnitude_range:                 3–15
districts_count:                 1 (undivided); 2–6 (ward-divided)
districting_authority:           council itself, subject to NSW
                                 EC procedural rules and Boundaries
                                 Commission review
districting_frequency_years:     periodic review (typically every
                                 council term)
districting_criteria_in_statute: population equality across wards
                                 within a council; geographic
                                 community of interest

tiered:                          no
tier_count:                      1
tier_compensatory:               not applicable

threshold_of_exclusion_pct:      25% (M=3 ward) → 6.25% (M=15)
```

### Notes

The **mixed ward / undivided** structure is itself an
interesting drafting feature. NSW councils choose between
preserving geographic representation (ward-divided, M=3) and
maximizing proportionality (undivided, M up to 15). The
trade-off is explicit and council-by-council.

For US implementation: NSW's mixed ward / undivided pattern
maps cleanly onto US local charters. Many US cities are
already debating exactly this trade-off (see the LA reform
debate in the Guinier Project primer, p. 8). NSW shows a
working middle path — some councils are wards, others are
at-large, and the system functions as proportional under both
configurations.

The 25% threshold of exclusion for a 3-seat ward is **higher
than is typical** in continental European list-PR systems and
warrants attention. This is the structural cost of preserving
geographic representation through small wards.

---

## 2. Component 2 — Ballot Structure

### The above-the-line / below-the-line architecture

Where 2 or more councillors are to be elected (s 308A LGA), and
where a group of candidates has been formed and registered for
group voting (ss 308A–308C), the ballot paper has **two
sections**:

- **Above the line**: one square per registered group, with
  the group's name (or "Group A", "Group B", "Group C", etc.).
  A voter marks **one square** above the line to express a
  group preference.
- **Below the line**: one row of squares per candidate. A
  voter may number candidates in order of preference (1, 2, 3,
  …), with **optional preferences** — voters need not number
  every candidate.

### Section 308C LGA — Group voting marking of ballot-papers (substantive content)

The substantive rule (per the NSW Electoral Commission's
candidate handbook and the section description; verbatim text
to be added when primary-source access permits):

- A voter may **either** mark a single group square above the
  line **or** number individual candidates below the line —
  not both.
- A vote that marks above the line is treated as a vote **for
  the candidates of that group, in the group's listed order**.
  The above-the-line mark generates an automatic preference
  flow: vote 1 to candidate 1 of the group, vote 2 to
  candidate 2 of the group, and so on through the group's full
  list.
- A vote that marks below the line is interpreted at face
  value: the voter's numbered preferences govern.
- The above-the-line preference flow is **internal to the
  group only**. Unlike the pre-2016 federal Senate system,
  NSW local above-the-line votes do **not** flow to candidates
  of other groups via group voting tickets. A voter who wants
  to express preferences across groups must vote below the
  line.

### Section 308A LGA — Grouping of candidates

The substantive rule:

- Two or more candidates may **request to form a group** on
  the ballot paper, by joint nomination.
- A group is registered with the Returning Officer; the group
  must specify a **Group Voting Square** if eligible.
- Where eligible, the group's name appears as a column header
  above the line. Group order on the ballot is determined by
  draw conducted by the Returning Officer.
- Candidates may also stand individually (ungrouped); their
  names appear below the line on the right side, after all
  registered groups, with no above-the-line square.

### Operationalized values

```
ballot_type:                     stv_with_above_the_line_group_vote
                                 (out of project scope as
                                 vote-conversion rule, but
                                 architecturally relevant for the
                                 above-the-line interface)
preference_votes_per_voter:      1 group preference (above the line)
                                 OR multiple candidate preferences
                                 (below the line)
panachage_allowed:               below-the-line only (voter can
                                 number candidates across groups
                                 in order of preference)
cumulation_allowed:              no
above_the_line_option:           yes — single mark; preferences
                                 flow within the group only
below_the_line_option:           yes — voter numbers candidates
                                 individually; optional preferences

party_lists_allowed:             yes — registered political
                                 parties may form groups
voter_grouping_lists_allowed:    yes — any 2+ candidates may form
                                 a group jointly, regardless of
                                 party affiliation
voter_grouping_legal_term:       "group" (LGA s 308A)
citizen_committee_lists_allowed: yes — a group is fundamentally
                                 a candidate-level association,
                                 not an organizational form
independents_on_lists_allowed:   yes — independents may form a
                                 group jointly, or stand
                                 ungrouped without a group square

non_party_label_allowed:         yes — group may register a name
                                 (subject to non-deceptive rules
                                 and approval by the Returning
                                 Officer); otherwise allocated
                                 "Group A", "Group B", etc.
non_party_label_categories:      not statutorily restricted —
                                 groups may use civic, geographic,
                                 advocacy labels or remain
                                 alphabetic placeholders
non_party_label_restrictions:    no name confusable with a
                                 registered party
label_validation_authority:      Returning Officer / NSW Electoral
                                 Commission
```

### Notes — the above-the-line interface as a design pattern

Three features of NSW above-the-line voting bear directly
important for the user's preferred ballot architecture:

1. **Single mark above the line is the dominant voting mode**.
   In Australian Senate elections under the pre-2016 system,
   over 95% of voters used the above-the-line option;
   comparable proportions are reported for NSW local
   elections. The above-the-line option is not just a
   simplifier — it is the **default interface that the
   majority of voters actually use**, with below-the-line as
   the active-engagement option for those who want it.
2. **Within-group preference flow** is the post-2016
   architecture (and, importantly, the architecture NSW
   retained continuously since 1984). A single above-the-line
   mark gives the voter's vote to candidates of the marked
   group only, never to candidates of other groups. This is
   the cleaner drafting choice — it preserves voter intent
   and forecloses "preference-whisperer" gaming of group
   voting tickets.
3. **The group label is permissive but validated**. Groups
   may use any non-deceptive label, but the Returning Officer
   has authority to reject confusable labels. This is
   structurally similar to Bavaria's *Wahlausschuss* approval
   of *Wählergruppe Kennworte* — and gives the project a
   second working precedent for the labeling problem the
   primer flags (p. 12).

### Notes — what NSW local teaches that Bavaria does not

In addition to the differences with NRW (closed list, single-
mark default) and Bavaria (open list with cumulation/panachage),
NSW local offers a third distinctive ballot architecture: the
voter explicitly chooses between two voting modes. The choice
is **structurally embedded in the ballot**, not a side-feature.

This is the closest working comparator to the user's design:
one ballot, two voter modes, the choice itself displayed on the
ballot (above-the-line square vs. below-the-line preference
numbers).

---

## 3. Component 3 — Allocation Formula

### The Droop quota

Vote counting is governed by Schedule 4 of the LGA. The quota
formula is the standard **Droop quota**:

> Quota = ⌊ (total formal first-preference votes) / (number of
> seats to fill + 1) ⌋ + 1

For example, in an undivided 9-seat council with 100,000 formal
first-preference votes, the quota is:

> ⌊ 100,000 / 10 ⌋ + 1 = 10,001

A candidate elected reaching exactly the quota holds 10,001
votes; surplus votes (votes above the quota) are transferred to
remaining candidates per the surplus-transfer rule.

### Note on STV scope

STV-as-vote-conversion rule is **out of scope** for this
project (per the synthesis in `framework/synthesis.md`). NSW
local use is included for the architectural lessons of the
above-the-line interface (Component 2), not as a model for
vote conversion. The Droop quota and the surplus-transfer
mechanism are documented here for completeness; the eventual
US model statute is expected to use list-PR mechanics
(Sainte-Laguë / Webster) rather than STV.

### Surplus transfer rule

Per the NSW Electoral Commission's distribution-of-preferences
procedure:

- All ballot papers received by the elected candidate are
  **re-sorted** to their next preferred continuing candidate.
- Each ballot paper is re-valued at a **transfer value**
  calculated as: (surplus votes) ÷ (total ballot papers in
  the elected candidate's pile).
- The transfer-value-weighted next-preference votes are added
  to the receiving candidates' totals.

### Exclusion rule

If no candidate reaches the quota after first preferences are
counted (or after a surplus transfer), the candidate with the
**fewest votes** is excluded. All of that candidate's ballots
flow to their next preferences at the value at which they were
last counted.

### Operationalized values

```
allocation_formula:              droop_stv                # Schedule 4
                                 (out of project scope as
                                 vote-conversion rule)
formula_codified_as:             procedural — quota and transfer
                                 mechanics specified in Schedule
                                 4 LGA; implementing detail in
                                 Local Government (General)
                                 Regulation 2021
formula_statutory_citation:      LGA NSW Schedule 4
ties_rule:                       drawing of lots by Returning
                                 Officer (LGA Schedule 4)

legal_threshold_pct:             none statutorily; structural
                                 (Droop) only
threshold_level:                 ward / council
threshold_exemption_rules:       not applicable
threshold_backdoor:              not applicable

apparentement_allowed:           no — group declarations are
                                 made before the count, but
                                 cross-group preference flow
                                 occurs only via voter
                                 below-the-line preferences,
                                 not via post-vote pooling
intra_list_rule:                 above-the-line preferences
                                 flow in submitter-set group
                                 order; below-the-line preferences
                                 are voter-set
preference_threshold_pct:        not applicable (every preference
                                 counts)
intra_list_ties_rule:            lot
```

### Notes

Two features of the NSW counting regime are relevant for the
project even though STV-as-conversion is out of scope:

1. **The Droop quota is the procedural keystone** for any
   STV-derived system. Bavarian municipal allocation under
   Sainte-Laguë and NSW STV under Droop produce different
   distributional outcomes; comparing them empirically is
   instructive even if the US model adopts Sainte-Laguë.
2. **The optional-preference rule** under the LGA below-the-
   line interface means voters can stop numbering at any
   point. A voter who numbers only "1, 2, 3" in a 15-seat
   contest is treated as expressing only those three
   preferences; the ballot is **not** invalid for failure to
   number every candidate. This is a useful drafting model
   for any ballot architecture that gives voters granular
   control without imposing high cognitive cost.

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

NSW resident enrolment with the **Australian Electoral
Commission** (federal) is automatic for state and federal
elections; the same enrolment is used for NSW local elections.
NSW local-only voter classes:

- **Resident roll** (R-roll): adult Australian citizens
  resident in the council area.
- **Non-resident roll** (NR-roll): owners or occupiers of
  rateable land who do not reside in the council area.
- **Non-resident occupier roll** (CC-roll): occupiers of
  rateable land (e.g., business tenants) who do not reside in
  the council area.

Voting in council elections is **compulsory** for those on the
resident roll, consistent with the broader Australian
compulsory-voting tradition.

### B. Candidate / group registration — *full subsection*

Per the NSW Electoral Commission candidate handbook for the
2024 elections:

#### Candidate nomination

- All candidates must lodge an **individual nomination form**
  during the nomination period.
- Nomination deposit is required (amount set in regulation;
  forfeited if a candidate fails to reach a specified vote
  threshold, refunded otherwise).
- A nominator declaration is required from a specified number
  of registered voters in the relevant ward / council area
  (typical: 25 for council candidates).

#### Group formation

- Two or more candidates may request to **form a group on the
  ballot paper** at the same time as their nomination.
- A grouping form is lodged jointly. The group elects whether
  to request a **Group Voting Square** (above-the-line square).
- Eligibility for the group voting square: the group must be a
  bona fide group of two or more candidates (anti-fraud
  threshold).

#### Registration vs. nomination

- "Registration" with the NSW EC and "nomination" are distinct
  processes. From 15 August 2024, candidates and groups that
  nominate without prior registration are **deemed registered**
  on nomination — a significant 2024 reform. Deemed-registered
  participants take on record-keeping and disclosure
  obligations.

#### Ballot order

- The Returning Officer conducts a **public draw** to determine
  the order of groups and ungrouped candidates on the ballot.
- Within a group, candidate order is set by the group itself in
  the grouping form.

### Operationalized values

```
list_registration_authority:     NSW Electoral Commission /
                                 Returning Officer for the
                                 council
signatures_required_min:         ~25 nominator declarations
                                 (typical; verify exact number
                                 in current Local Government
                                 (General) Regulation 2021)
signature_scaling:               no scaling — same for all
                                 candidates regardless of council
                                 size
signature_geographic_distribution:
                                 nominators must be on the roll
                                 for the relevant ward / council
deposit_amount:                  set in regulation (typically
                                 hundreds of AUD per candidate)
deposit_currency:                AUD
deposit_refund_threshold:        4% of formal first-preference
                                 votes (typical for STV
                                 jurisdictions)
filing_deadline_days_before:     ~25 days before election
                                 (period set by NSW EC each cycle)
party_v_nonparty_equal_treatment:
                                 yes — registered parties and
                                 groups of independents follow
                                 the same nomination and grouping
                                 process
list_size_min:                   2 candidates (minimum to form
                                 a group)
list_size_max:                   not statutorily fixed (typical
                                 cap = number of seats × 2 in
                                 the regulation)
list_ordering_rule:              submitter — group sets candidate
                                 order on the grouping form
gender_quota:                    none in LGA; no statutory quota
residency_required:              candidate must be on the roll
                                 for the council / ward
multiple_candidacy_restrictions:
                                 candidate may stand in one
                                 council only; may stand in
                                 only one group within that
                                 council
```

### Notes — the labeling regime

Group names are subject to the Returning Officer's approval.
Names confusable with registered parties may be rejected. In
practice, NSW local groups use a wide range of label
categories:

- **Party-aligned**: e.g., "Liberal Party of Australia (NSW
  Division)", "Australian Labor Party (NSW Branch)", "The
  Greens NSW".
- **Independent / civic**: e.g., "Independents for [Council
  Name]", "Save Our Council Group".
- **Geographic**: e.g., neighborhood-named groups in
  ward-based elections.
- **Generic placeholders**: "Group A", "Group B", "Group C"
  where no distinctive name is registered.

This is structurally similar to the Bavarian *Wahlausschuss*
approval of *Kennworte*, but more permissive — NSW does not
exclude "ethnic affiliation" labels or limit categories
explicitly.

### C. Campaign finance

Governed by *Electoral Funding Act 2018* (NSW). Disclosure
thresholds and caps apply to candidates, groups, and parties.
**Group disclosure obligations apply to non-party groups as
well as party groups** — a useful drafting precedent.

### D. Election administration

NSW Electoral Commission (NSWEC), the same body administering
state elections, conducts council elections under the LGA. The
Commissioner is independent. Returning Officers are appointed
for each council. Polling staff are recruited and trained by
the NSWEC.

### E. Vote count, certification, dispute resolution

Counting is conducted at central counting centers (not at
polling stations) for proportional contests, owing to the
complexity of preference distribution. Preliminary results are
available election night for first preferences; full
distribution of preferences typically takes 1–3 weeks
depending on council size.

Election challenges may be brought to the **Court of Disputed
Returns** (the NSW Supreme Court sitting in this capacity).
Disputes may be brought by candidates or by qualified electors
within a specified time after the result.

### F. Media access

Governed by federal *Broadcasting Services Act 1992* and ACMA
regulations; NSW-level provisions in the *Electoral Funding
Act 2018* on advertising disclosure.

---

## 5. PROSeS performance diagnostic

The **14 September 2024 NSW local elections** are the empirical
anchor. There is no OSCE/ODIHR observation report at NSW local
level (Australia is not an OSCE participating State). Empirical
evidence comes from:

- **NSW Electoral Commission** post-election reports.
- **Australian Electoral Study** academic surveys.
- The *Australian Election Study* (federal, but tracking
  attitudes that affect local participation).
- *Local Government NSW* (peak body) reporting.

### Process Design

**Public participation.** The NSWEC conducts public consultation
on regulatory and administrative reforms. The 2024 cycle's
"deemed registration" reform was implemented after public
consultation.

**Probity and impartiality.** NSWEC is statutorily independent
and reports to Parliament. No significant integrity concerns
are routinely raised about the council-election administration.

**Accountability.** Election challenges run to the Court of
Disputed Returns; expedited deadlines apply.

### Resource Investment

Council elections are funded through a charge to the council
(councils pay the NSWEC for conducting their elections). This
is a notable difference from German practice (federal/Land
funding) — NSW councils carry the cost of their own elections.

### Service Output Quality

**Convenience.** Compulsory voting plus widespread postal,
pre-poll, and absent voting produces high participation (above
90% of registered voters). The above-the-line option
substantially reduces ballot-completion time for the majority
of voters who use it.

**Accuracy.** Above-the-line voting produces low informality
rates (single mark is unambiguous); below-the-line voting
historically has higher informality rates owing to the
complexity of numbering preferences. NSW EC publishes
informality-rate analyses after each cycle.

**Enforcement.** The Returning Officer's group-label approval
process is rule-bound and reviewable; group voting square
eligibility is checked at nomination.

### Service Outcomes

**Voter turnout** at NSW council elections is typically
**85–92%** of enrolled voters (compulsory voting effect).

**Equity / minority representation.** Indigenous Australian
representation on NSW councils has historically been
underrepresented relative to population share. Some councils
with significant Indigenous populations have implemented
specific outreach measures, but no statutory Indigenous-seat
provisions exist analogous to New Zealand's reserved Māori
seats. **This is a significant area for the project's
comparisons document on equality and minority
representation.**

Migrant-origin candidate representation has improved over
recent cycles in metropolitan Sydney councils, with several
councils now having majority migrant-origin council membership.

### Stakeholder Satisfaction

Generally high among administrators and observers; some
academic critique of the above-the-line interface as
delegating preference-formation to political parties even at
the local level.

---

## 6. Venice Commission compliance check

Australia is not a Venice Commission member, but the Venice
principles map onto Australian electoral law without
substantive friction:

```
universal_suffrage:    compliant   # Compulsory voting, broad
                                   # eligibility
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant   # 4-year cycle
fundamental_rights:    compliant
regulatory_stability:  high        # LGA in force since 1993,
                                   # incremental reforms
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| Above-the-line group voting interface (s 308C) | **Universal** | The single-mark group option with within-group preference flow is portable to any list-PR system; structurally simple and familiar to Australian voters. |
| Below-the-line optional preferences | **Hybrid** | Substantively universal (voter chooses level of detail); procedurally tied to STV vote conversion. Adapting to list PR requires careful drafting — the "optional" feature can be kept (voter need not number every preferred candidate) but the resulting preferences would feed an intra-list reordering rule rather than an STV count. |
| Group registration as candidate-association (not party-association) | **Universal** | The *group* under s 308A is fundamentally a candidate-level association, not a party. This is structurally similar to Bavarian *Wählergruppe* (GLKrWG Art. 24(1)) and is portable. |
| Returning Officer label-approval | **Universal** | Both NSW and Bavaria apply this pattern. |
| Compulsory voting | **Particular** | Distinctive Australian feature; not portable to US contexts where compulsory voting is constitutionally and politically untenable. |
| Council-funded elections | **Particular** | Reflects Australian fiscal federalism; US local-election funding patterns vary by state. |
| Indigenous representation gap (no reserved seats) | — | A negative finding rather than a portable feature — illustrates that high-quality PR design alone does not solve representation gaps for historically marginalized groups. |
| Group voting at the M=3 ward level | **Hybrid** | The architectural pattern is portable; the high (25%) threshold of exclusion at M=3 may make the design unattractive for US contexts where the goal is to lower thresholds. |

### Top three takeaways for US state/local implementation

1. **Above-the-line group voting is one implementation
   of one-mark-or-detailed-preferences voter choice.** The
   ballot makes the choice structurally explicit by using two
   sections (above and below the line). The single-mark option
   is the dominant voting mode in practice (>95% of voters in
   Senate elections; comparable in NSW local). For the user's
   preferred ballot design, this is the directly importable
   architectural pattern.

2. **Within-group preference flow only.** NSW local
   above-the-line votes flow within the marked group and
   nowhere else. This forecloses "preference-whisperer"
   gaming and ensures voter-intent preservation. The 2016
   federal Senate reform reached the same conclusion at the
   national level. For US drafting, this is the right default
   — never let an above-the-line mark flow to candidates of
   another group without the voter's express direction.

3. **Decouple the registration and nomination processes.**
   NSW's 2024 "deemed registration" reform recognizes that
   participants who nominate without prior registration take
   on the same record-keeping and disclosure obligations.
   This is a useful drafting move: it lowers the entry
   barrier (one process, not two) while preserving regulatory
   protections.

---

## 8. Sources

### Primary

- *Local Government Act 1993* (NSW) No 30, in force as at 19
  September 2025. Sections 308A, 308B, 308C, 308D and
  Schedule 4 are the architectural keystones.
  <https://legislation.nsw.gov.au/view/whole/html/inforce/current/act-1993-030>
- *Local Government (General) Regulation 2021* (NSW), Chapter
  10 (Elections).
- AustLII alternative reference:
  <https://www5.austlii.edu.au/au/legis/nsw/consol_act/lga1993182/>
- *Commonwealth Electoral Act 1918* (Cth) — federal Senate
  provisions (reference, not the substantive NSW local
  authority).
- *Electoral Funding Act 2018* (NSW) — campaign finance.

### Secondary (NSW Electoral Commission official materials)

- NSW Electoral Commission, *Candidate handbook: NSW Local
  Government elections* (2024 edition). Authoritative on
  registration, nomination, group formation, and ballot
  layout.
- NSW Electoral Commission, *Distribution of Preferences (DoP)
  in a Local Government election* (procedural report; PDF on
  NSWEC website).
- NSW Electoral Commission, post-election bulletins for the 14
  September 2024 cycle.
- *Local Government NSW* peak-body materials.

### Outstanding gaps

The following remain to be retrieved (NSW legislation servers
and AustLII are currently behind Cloudflare protection that
blocks automated retrieval):

- Verbatim text of LGA NSW ss 308A, 308B, 308C, 308D.
- Verbatim text of LGA NSW Schedule 4 (counting of votes,
  including the Droop quota and surplus-transfer rules).
- Verbatim text of the *Local Government (General) Regulation
  2021* provisions on nomination forms, group registration,
  and ballot layout.
- 2024 NSW local election outcome data: invalid-vote rates by
  council size and ward configuration; share of seats won by
  non-party groups vs registered parties; demographic
  representation analysis.
- Indigenous Australian representation data on NSW councils
  (for the planned equality-and-minority-representation
  comparisons document).
- Comparative data on above-the-line vs below-the-line voting
  rates.

### 2016 federal Senate reform — reference notes

For the eventual comparison with the user's preferred ballot
design, the **2016 federal Senate reform** is the most
important precedent in any common-law democracy:

- **Pre-2016**: above-the-line vote interpreted via registered
  group voting tickets (GVTs). Single mark "1" above the line
  → vote allocated according to the party's pre-registered
  preference flow, often reaching candidates of other
  parties via GVT chains. Approximately 95% of voters used
  above-the-line voting under this regime.
- **2016 reform** (*Commonwealth Electoral Amendment Act
  2016*): GVTs abolished. Above-the-line voting now requires
  numbering at least 6 boxes; preferences flow only to
  candidates of the marked groups, in voter-determined order.
  Below-the-line minimum numbering reduced from "every
  candidate" to "at least 12 boxes."
- **Why this matters for the project**: the federal reform
  effectively converted above-the-line voting from a
  party-controlled preference proxy into a voter-controlled
  multi-group ranking. NSW local has *not* followed this
  reform — NSW local retains the simpler within-group-only
  flow that the user's preferred design also adopts. The NSW
  position is therefore the more directly portable model.

### Resolved in iterations to date

**2026-05-05** (initial profile):
- LGA ss 308A–308D substantive content captured (verbatim
  text outstanding).
- LGA Schedule 4 counting procedure described from official
  handbook.
- Group registration and labeling regime documented.
- 2016 federal Senate reform context noted for comparison.
- Equity / Indigenous representation flagged for the
  comparisons document.
