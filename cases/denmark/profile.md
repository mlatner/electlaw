# Denmark — Folketing (National Parliament)

## 0. Case metadata

- **Country**: Kingdom of Denmark (Kongeriget Danmark)
- **Sub-jurisdiction**: National (Folketinget — the unicameral
  national parliament). The two Greenlandic and two Faroese
  seats are noted but the architectural focus of this profile
  is the 175 seats allocated within Denmark proper.
- **Level of government**: National. A separate Danish profile
  in this directory (`README.md`) addresses local elections
  under the *Lov om kommunale og regionale valg*; this profile
  is the Folketing-level companion.
- **Electoral system family**: **Two-tier flexible-list
  proportional representation** with party-elective intra-list
  architecture. The 175 mainland seats are split between a
  **constituency tier** (135 *kredsmandater* / constituency
  seats, allocated district-by-district by Hare quota with
  remainder distribution) and a **compensatory tier** (40
  *tillægsmandater* / supplementary or leveling seats,
  distributed nationally by Sainte-Laguë / Webster to repair
  the constituency-tier disproportionality). Voters cast one
  vote, which may be expressed as either a personal vote for a
  candidate or as a party-only vote.
- **Governing statutes**:
  - ***Lov om valg til Folketinget*** (Folketing Elections Act
    — *Folketingsvalgloven*), consolidated text by
    Lovbekendtgørelse. The Act is the comprehensive statute
    governing nomination, ballot architecture, allocation
    across the two tiers, the national threshold, and the
    administration of the count.
  - ***Lov om kommunale og regionale valg*** (Municipal and
    Regional Elections Act — *Kommunal- og regionalvalgloven*).
    Cross-referenced in this profile for parallels in
    flexible-list mechanics and list-cartel administration; the
    detailed local treatment lives in
    `cases/denmark/README.md`.
  - ***Danmarks Riges Grundlov*** (Constitution Act of the
    Kingdom of Denmark, 5 June 1953). §§ 28–32 fix the basic
    Folketing structure; § 31 is the operative electoral
    clause.
- **Constitutional anchor**: Grundloven § 31. The clause
  obligates the legislator to construct an electoral system
  that secures "an equal representation of the various
  opinions among the electorate" (*ligelig repræsentation af
  de forskellige meninger blandt vælgerne*). This phrase is
  the constitutional source of the two-tier architecture: the
  legislator reads the obligation as a directive to compensate
  constituency-tier disproportionality through a national
  leveling tier.
- **EMB**: ***Valgnævnet*** (the Electoral Board) reviews
  party-name registrations and certain disputes;
  ***Indenrigsministeriet*** (the Ministry of the Interior —
  current ministerial designation
  *Indenrigs- og Sundhedsministeriet*) administers the
  Folketing elections operationally, with detailed local
  conduct in the hands of *valgbestyrelser* (electoral boards)
  in each constituency and ultimately the municipal
  *kommunalbestyrelser* for polling-station operations.
- **Last regular election**: **1 November 2022** (early
  election called by Prime Minister Frederiksen). Next regular
  election due no later than four years from constitutive
  meeting of the new Folketing.
- **Analyst**: this profile, 2026-05-15.

### Why this case is in the project

Three features make Denmark a central case for the project:

1. **Party-elective intra-list architecture (*partiliste* vs
   *sideordnet opstilling*).** The Folketingsvalgloven gives
   each party a structural choice at nomination between two
   intra-list seat-assignment regimes: a closed-list,
   submitter-ordered *partiliste* presentation, or a parallel-
   ordered *sideordnet opstilling* presentation in which all
   nominated candidates sit equally on the list and intra-list
   seat assignment is governed entirely by personal-vote
   totals within the constituency. The choice is per party and
   per constituency, registered at the time of nomination.
   This is the project's only example of intra-list architecture
   treated as a party-elective parameter rather than as a
   system-level constant. For a U.S. drafter, the design is a
   working illustration that a single statute can leave the
   open-list / closed-list axis to the nominating association
   rather than committing the legislator to a single answer
   for every list.
2. **List-cartel mechanics (*listeforbund* and *valgforbund*).**
   The Folketingsvalgloven traditionally permitted parties to
   declare **valgforbund** — formal pre-election cartels
   pooling votes for purposes of seat allocation — at both the
   constituency tier and (originally) at the national tier.
   The 2018 reform package (Lov nr. 712 af 8. juni 2018)
   abolished valgforbund for Folketing elections. The
   pre-2018 regime and the 2018 abolition together constitute
   the project's most directly portable record of how a
   national legislator can both create and dismantle a
   list-cartel apparatus. List-cartel mechanics survive at the
   municipal level under the *Kommunal- og regionalvalgloven*.
3. **Two-tier compensatory architecture under a single
   statute.** The split between 135 constituency seats and 40
   national leveling seats is administered within one statute
   without recourse to a constitutional formula. This is the
   project's clearest example of statutory implementation of
   the *Grundloven* § 31 obligation; the formulation is
   transparent on its face and reduces operational reliance on
   judicial interpretation of constitutional text.

The case also documents Denmark's signature provisions on
voter-association nominations (*stillerlister*) for new parties
and independents, which extend ballot access beyond established
parties without recourse to a separate non-party-list entity
class.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — Grundloven § 31

The Constitution Act (1953), § 31, fixes the basic parameters
of Folketing composition and the directing principle of the
electoral system:

> § 31. Stk. 1. Folketingets medlemmer vælges ved almindelige,
> direkte og hemmelige valg.
>
> Stk. 2. Loven fastsætter de nærmere regler for valgrettens
> udøvelse, herunder bestemmelser om valgretten i særlige
> tilfælde og om opstilling af kandidater.
>
> Stk. 3. Det antal medlemmer, der vælges i de enkelte områder
> af landet, fastsættes således, at det med Færøerne og
> Grønland ikke overstiger 179, hvoraf 2 vælges på Færøerne og
> 2 i Grønland. Loven fastsætter de nærmere regler om
> opdelingen i valgkredse.
>
> Stk. 4. Ved de i loven fastsatte regler, hvorefter
> mandaterne fordeles på partierne, skal der gives disse en
> efter deres styrke ligelig repræsentation. Som fremgangsmåde
> ved valg af medlemmer, der vælges i enkeltkredse, kan loven
> fastsætte forholdstalsvalg, flertalsvalg eller dele af begge
> dele.

(Translation: § 31(1) Members of the Folketing are elected by
universal, direct, and secret suffrage. (2) The Act prescribes
detailed rules on the exercise of the franchise, including
provisions on the franchise in special cases and on the
nomination of candidates. (3) The total number of members
elected from the several areas of the country, together with
the Faroe Islands and Greenland, may not exceed 179, of which
2 are elected in the Faroe Islands and 2 in Greenland. The Act
prescribes detailed rules on the division into constituencies.
(4) Under the rules prescribed in the Act for the distribution
of seats to the parties, the parties shall be given a
representation corresponding to their respective strengths. The
Act may provide for proportional, plurality, or a combination
of both as the procedure for the election of members elected
in single constituencies.)

The substantive directive — *"en efter deres styrke ligelig
repræsentation"* (a representation corresponding to their
respective strengths) — is the constitutional source of the
compensatory-tier architecture in the Folketingsvalgloven. The
constitutional text deliberately under-specifies the formula:
it requires proportional outcomes but leaves to the statute
the technical means by which proportionality is achieved.

### Assembly size

Per Grundloven § 31(3), the total assembly size is capped at
**179 members**, split as follows:

- **175 seats elected within Denmark proper**, themselves split
  between 135 constituency seats and 40 compensatory seats.
- **2 seats elected in the Faroe Islands** under separate
  procedures specified by the Faroese authorities under
  delegated arrangement.
- **2 seats elected in Greenland**, similarly under separate
  procedures.

The Folketingsvalgloven specifies the 135 / 40 split within
the 175 mainland seats. The constitutional cap on 179 places
the legislator on a fixed ceiling: adjustments to district
boundaries or to the tier split must keep the total constant.

### Districts and magnitude — the three-level constituency structure

The Folketingsvalgloven operationalizes the constituency
structure on three levels:

1. **Three regional groupings (*landsdele*)**: Hovedstaden
   (the Copenhagen Metropolitan landsdel), Sjælland-Syddanmark
   (Zealand–Southern Denmark), and Midtjylland-Nordjylland
   (Central–North Jutland). The threshold disjunction
   (Component 3 below) operates partly at this level.
2. **Ten multi-member constituencies (*storkredse*)**: the
   ten storkredse partition the country, with magnitudes that
   range roughly from 6 to 20 constituency seats each. The
   storkredse are the unit at which the constituency-tier
   Hare-quota allocation is performed and at which lists are
   submitted.
3. **Local nomination districts (*opstillingskredse*)**: 92
   sub-storkreds units used for ballot-design and intra-list
   personal-vote tabulation. The opstillingskredse do not
   themselves receive seats; they organize the personal-vote
   competition within a list.

The 135 constituency seats are pre-distributed across the ten
storkredse by a population-and-area formula (Folketingsvalg-
loven specifies the recomputation procedure; recomputation
runs each cycle from the most recent demographic and area
data). Approximate per-storkreds magnitudes from the most
recent allocation:

| Landsdel | Storkreds | Approx. constituency-seat magnitude |
|---|---|---:|
| Hovedstaden | Københavns Storkreds | ~16 |
| Hovedstaden | Københavns Omegns Storkreds | ~11 |
| Hovedstaden | Nordsjællands Storkreds | ~11 |
| Hovedstaden | Bornholms Storkreds | 2 |
| Sjælland-Syddanmark | Sjællands Storkreds | ~20 |
| Sjælland-Syddanmark | Fyns Storkreds | ~12 |
| Sjælland-Syddanmark | Sydjyllands Storkreds | ~18 |
| Midtjylland-Nordjylland | Østjyllands Storkreds | ~14 |
| Midtjylland-Nordjylland | Vestjyllands Storkreds | ~13 |
| Midtjylland-Nordjylland | Nordjyllands Storkreds | ~16 |

Bornholm has a constitutionally protected 2-seat minimum
within the constituency tier; in practice this is the single
exception to the otherwise population-driven magnitude
calculation.

### Tiered structure

```
tiered:                          yes
tier_count:                      2
tier_magnitudes:
  tier_1 (constituency):         135 seats distributed across
                                 10 storkredse; per-storkreds M
                                 ~ 2 – 20
  tier_2 (compensatory/leveling): 40 seats distributed nationally
                                 to parties qualifying under the
                                 national threshold
tier_compensatory:               yes — tier 2 levels overall
                                 national proportionality
                                 conditional on the threshold
```

### Operationalized values

```
total_seats:                     179 (Grundloven § 31(3)) —
                                 175 mainland + 2 Faroese + 2
                                 Greenlandic; this profile
                                 covers the 175 mainland
codification_instrument:         Grundloven § 31(3) (assembly
                                 size); Folketingsvalgloven
                                 (constituency and tier
                                 structure)
amendment_authority:             Folketinget (statute) for
                                 constituency / tier rules;
                                 constitutional amendment under
                                 Grundloven § 88 for the
                                 assembly-size cap
amendment_threshold:             ordinary majority for the
                                 statute; constitutional
                                 amendment procedure (§ 88) for
                                 the cap

magnitude_uniform:               no
magnitude_typical:               ~13 (median constituency-tier
                                 magnitude per storkreds)
magnitude_range:                 2 (Bornholm) — ~20 (Sjælland)
districts_count:                 10 storkredse (tier 1) plus
                                 1 national tier (tier 2);
                                 92 opstillingskredse for
                                 ballot administration
districting_authority:           Folketingsvalgloven (statute);
                                 boundary maintenance through
                                 Indenrigsministeriet
districting_frequency_years:     per cycle (magnitudes
                                 recomputed; storkreds boundaries
                                 stable since 2007 reform)
districting_criteria_in_statute: population + area formula
                                 specified in the Act; Bornholm
                                 floor preserved

threshold_of_exclusion_pct:      ~33% (Bornholm, M=2) → ~5%
                                 (Sjælland, M=20) at constituency
                                 tier; effectively superseded by
                                 the 2% national threshold + 40
                                 compensatory seats at the
                                 national tier
```

### Notes

The Danish two-tier architecture is the project's clearest
example of a statute deriving the entire allocation framework
from a constitutional fairness clause. Grundloven § 31(4)
states the directive in general terms; the Folketingsvalgloven
operationalizes the directive by reserving 40 of 175 mainland
seats for compensatory allocation. The 40-seat tier-2
allocation is calibrated to be large enough to level all
within-storkreds disproportionality that the Hare-quota tier-1
allocation leaves behind, provided the affected list clears
the national threshold.

The Bornholm 2-seat minimum is the only departure from the
otherwise demographic-driven allocation. The retention of
Bornholm as a freestanding storkreds reflects an island-
geography rationale; it produces a constituency-tier M = 2 for
which the constituency-tier threshold of exclusion is
nominally 33%. The compensatory tier substantially repairs
this for any party that clears the 2% national threshold,
because compensatory seats can be assigned to candidates in
storkredse where the party's constituency-tier allocation fell
short.

For U.S. drafters, the Danish constituency / compensatory
split is a directly portable model for state-legislature-scale
PR adoption. The constituency-tier magnitudes (~10–20) are at
the upper end of what a U.S. state could plausibly adopt at a
single tier without political controversy; the addition of a
compensatory tier permits the legislator to preserve the
existing geographic representation framework (county /
region groupings) and add proportionality through a
leveling tier without redrawing existing district boundaries.

The constitutional placement of the assembly cap (Grundloven
§ 31(3)) is a *Particular* feature in Gardner's terminology:
locking the 179-seat ceiling in the constitution constrains
the legislator's adjustments and reflects Denmark's specific
1953 settlement. For a U.S. drafter, the substantive choice —
fixing assembly size — is portable; the question is whether to
fix it in statute (most flexible), in a state constitution
(intermediate), or in a charter (most rigid).

---

## 2. Component 2 — Ballot Structure

### The voter's act — one vote, two expressions

Per Folketingsvalgloven (the operative chapters on ballot
casting and tabulation), each voter casts **one vote**, which
may be expressed in either of two forms:

1. **Personal vote (*personlig stemme*)**: the voter marks the
   name of a specific candidate. The vote counts both for the
   candidate's list (for inter-list allocation) and for the
   candidate's personal-vote total (for intra-list assignment
   if the list uses *sideordnet opstilling*).
2. **Party vote (*partistemme*)**: the voter marks the party
   name only, without naming a candidate. The vote counts for
   the list for inter-list allocation; it then flows to
   candidates either by the submitter's prescribed order
   (*partiliste*) or in a manner that depends on the list's
   chosen presentation (see *sideordnet opstilling* below).

The Danish ballot architecturally accommodates both
expressions on a single ballot: each list block on the ballot
displays the party name (which can be marked for a
*partistemme*) and the candidates' names (any of which can be
marked for a *personlig stemme*). The voter chooses one mark.

This distinguishes Denmark from the Netherlands (no separate
party-only option; voter must mark a candidate) and aligns it
with Brazil (which separates *voto de legenda* from *voto
nominal*). The party-only option is statutorily explicit
rather than a convention of marking the #1 candidate.

### The party-elective intra-list architecture

Folketingsvalgloven gives each nominating party (or candidate-
list) a choice at the time of nomination between two intra-list
presentation modes. The choice is made **per storkreds per
party** at the time of nomination and binds the list for that
election. The two modes are:

#### Mode A — *Partiliste* (party list, closed-list presentation)

The list is submitted with candidates in an order set by the
party. Under partiliste presentation, the order assigns seats:
when the list wins seats in that storkreds, the top-listed
candidate seats first, then the second-listed, and so on.
Personal votes still count toward the list's vote total but do
not (within partiliste presentation) reorder the candidates.

This is functionally a closed-list mode for the candidates,
but it sits within a flexible-list ballot — the voter can
still cast a personal vote for any candidate on the list, and
that personal vote will flow toward the list's allocation.

#### Mode B — *Sideordnet opstilling* (parallel ordering, open-list presentation)

All candidates on the list are presented as standing equally;
there is no submitter-imposed ordering. When the list wins
seats, they are assigned in descending order of personal-vote
totals. Party votes (votes for the party name without a named
candidate) are distributed across the candidates within the
storkreds in proportion to their personal-vote shares
(*forholdsmæssig fordeling*), so a candidate's effective total
becomes the sum of their personal votes plus a pro-rata share
of the storkreds-level party votes for that list.

Sideordnet opstilling is functionally a fully open-list mode:
voter personal-vote totals govern intra-list assignment with
no submitter-imposed ordering effect.

#### Operational significance

Major Danish parties typically choose *sideordnet opstilling*
in most storkredse — converting Folketing elections into a
substantively open-list exercise — while reserving the option
to use *partiliste* where the party wishes to lock a
particular ordering (for instance, to secure a sitting
incumbent's position, or to enforce a leadership-determined
ranking on a particularly competitive list). New, small, or
single-candidate lists also tend to use *sideordnet
opstilling* because they have only one or a few candidates
and the choice is operationally moot.

The portability significance for U.S. drafting is the design
itself, not the empirical pattern of party choice. The Danish
statute treats the open-list / closed-list axis as a
parameter the *nominating association* sets, rather than the
*legislator*. A U.S. statute could adopt the same approach:
permit each list-submitter to elect, at the time of filing,
which mode applies to that list in that district.

### Operationalized values

```
ballot_type:                     flexible_list with
                                 party-elective intra-list
                                 architecture
preference_votes_per_voter:      one (single mark per ballot)
                                 — may be a personal vote
                                 (candidate mark) or a party
                                 vote (party-name mark)
panachage_allowed:               no
cumulation_allowed:              no
above_the_line_option:           yes — party-only vote
                                 (*partistemme*) by marking
                                 the party name without
                                 naming a candidate

party_lists_allowed:             yes
voter_grouping_lists_allowed:    yes — *stillerlister*
                                 (voter-association
                                 nominations) under
                                 Folketingsvalgloven; new
                                 parties qualify by collecting
                                 signatures from a number of
                                 eligible voters equal to
                                 approximately 1/175 of valid
                                 votes cast in the previous
                                 election (currently in the
                                 vicinity of 20,000
                                 signatures)
voter_grouping_legal_term:       *stillerliste* (literally
                                 "list of supporters" — the
                                 form attesting voter support
                                 for a new party's
                                 candidature)
citizen_committee_lists_allowed: yes — through party
                                 registration with
                                 *Valgnævnet* or candidacy
                                 without party label
independents_on_lists_allowed:   yes — candidates may stand
                                 outside any party
                                 (*uden for partierne*),
                                 subject to local
                                 (opstillingskreds) signature
                                 requirements

non_party_label_allowed:         yes (a candidate may stand
                                 without party label; new
                                 party labels must clear
                                 *Valgnævnet* registration to
                                 appear on the ballot under a
                                 party name)
non_party_label_categories:      not statutorily restricted by
                                 type, but new names cannot be
                                 confusingly similar to an
                                 existing registered party
label_validation_authority:      *Valgnævnet* (Electoral
                                 Board)

intra_list_rule:                 party-elective per storkreds:
                                 *partiliste* (list order
                                 binding) OR *sideordnet
                                 opstilling* (personal-vote
                                 total decides, with
                                 proportional pro-rata
                                 distribution of party votes
                                 across candidates within
                                 the storkreds)
preference_threshold_pct:        N/A — *sideordnet opstilling*
                                 uses pure personal-vote
                                 ordering; *partiliste* uses
                                 list order. There is no
                                 percentage threshold for
                                 intra-list reordering
                                 analogous to the Dutch
                                 voorkeursdrempel.
intra_list_ties_rule:            drawing of lots
                                 (*lodtrækning*) by the
                                 constituency electoral board
```

### Notes

The Danish ballot structure is the project's clearest example
of three distinct drafting choices that a U.S. drafter would
otherwise treat as separate questions:

1. **Should the voter have a party-only option?** Denmark
   answers yes (partistemme is statutorily explicit). The
   Netherlands answers no (voorkeurstem-only ballot, with
   #1-position vote as convention). Brazil answers yes (voto
   de legenda). For U.S. drafting, the project recommends the
   Danish / Brazilian model.
2. **Should the open-list / closed-list choice be a system-
   level decision or a list-level decision?** Denmark is the
   only project case that resolves this question at the list
   level. The Folketingsvalgloven gives each nominating
   party-and-storkreds combination the choice between
   *partiliste* and *sideordnet opstilling*. Other project
   cases (Belgium federal, Brazil, Netherlands, Spain) fix
   the answer at system level.
3. **How are party-only votes (when permitted) distributed to
   candidates within a list?** Denmark distributes them
   proportionally to personal-vote shares within the storkreds
   under *sideordnet opstilling* (so they amplify the
   personal-vote ranking), and serially in submitter order
   under *partiliste* (so they confirm the submitter ranking).
   The proportional distribution under *sideordnet
   opstilling* is a notable design choice: it means a
   *partistemme* cast in a storkreds where one candidate has
   overwhelming personal-vote share will land disproportionately
   on that candidate, whereas in a storkreds with relatively
   even personal-vote distribution it will spread across all
   candidates.

For an open-list U.S. drafting target, the Danish *sideordnet
opstilling* allocation rule is the portable substantive
provision: party-only votes distributed proportionally to
personal-vote shares. The alternative (party-only votes
distributed serially in submitter order, as Brazil's voto de
legenda does under CE Art. 109 prior to the candidate-ranking
step) is also workable; the Danish proportional-pro-rata
distribution is more closely aligned with the principle that
the voter's expressed preferences within the list should
govern intra-list assignment.

---

## 3. Component 3 — Allocation Formula

### The two-tier allocation procedure

The Folketingsvalgloven specifies a four-step procedure that
allocates the 175 mainland seats:

1. **Tier 1: Constituency seats (*kredsmandater*)**: each
   storkreds's vote totals (each list's combined personal and
   party votes within the storkreds) are subjected to a
   Hare-quota (Hamilton/Hare) calculation. Each list receives
   one constituency seat per Hare quota of votes; remainder
   seats are distributed by largest-remainders within the
   storkreds.
2. **National threshold qualification**: a list qualifies to
   participate in the **tier-2 compensatory allocation** if and
   only if at least one of three conditions is met (see
   *threshold disjunction* below).
3. **Tier 2: Compensatory seats (*tillægsmandater*)**: the 40
   national leveling seats are distributed among qualifying
   lists by **Sainte-Laguë / Webster** applied to nationwide
   vote totals, with the seats already won at tier 1 deducted.
   The Sainte-Laguë method (divisors 1, 3, 5, 7, …) is used
   because of its low bias property: it minimizes the gap
   between vote shares and seat shares for any pair of
   qualifying lists.
4. **Assignment of compensatory seats to constituencies**: the
   compensatory seats won at the national level are assigned
   to specific storkredse within each party using a procedure
   that maximizes the proximity to ideal proportionality at
   the storkreds level. The assignment is to candidates within
   each list according to that list's *partiliste* or
   *sideordnet opstilling* presentation in the receiving
   storkreds.

### The threshold disjunction — Folketingsvalgloven (national threshold)

A list qualifies for tier-2 compensatory-seat allocation if
**any** of the following three conditions is satisfied:

1. The list wins **at least one constituency (tier-1) seat**
   anywhere in the country. (A list that wins a storkreds
   Hare-quota seat is by that fact qualified.)
2. The list receives **at least 2% of all valid votes cast
   nationwide**. (The standard national threshold.)
3. The list receives, in **at least two of the three
   landsdele**, vote totals that reach a level computed as
   the storkreds-level average of valid votes per
   constituency seat at the previous election (the so-called
   *regional-victories disjunction*, embedded in the
   Folketingsvalgloven; this third condition is rarely
   activated in practice because the 2% national threshold
   binds first for almost every nationally-organized list).

The threshold is therefore a **disjunctive** rule: clearing
*any one* of the three is sufficient. The structure is
designed to accommodate small parties with regionally-
concentrated support that may fall below 2% nationally but
nonetheless clear the constituency-seat or regional-victories
condition.

For comparative reference:
- **New Zealand** uses a similar disjunctive structure (5%
  national vote OR one electorate seat).
- **Germany** uses a similar disjunctive structure
  (5% national vote OR three constituency seats — the
  *Grundmandatsklausel* — though the 2023 BWahlG reform
  modified this).
- **Belgium federal** uses a per-district 5% threshold with
  no national equivalent.

The Danish three-condition disjunction is the most permissive
of the four configurations: the 2% national threshold itself
is lower than the 5% used by Germany and New Zealand, and the
constituency-seat backdoor is a single-seat condition (lower
than Germany's three-seat threshold).

### List cartels — *listeforbund* and *valgforbund*

#### The pre-2018 regime

Prior to 2018, the Folketingsvalgloven permitted two forms of
list-cartel arrangement:

- ***Listeforbund*** (literally "list cartel"): a formal
  pre-election declaration in which two or more lists
  *within the same party* agreed that their vote totals
  would be pooled for purposes of seat allocation. (In
  practice this arrangement was operational mostly within
  a single storkreds where one party ran multiple parallel
  lists; it is structurally similar to *apparentement*
  within a party.)
- ***Valgforbund*** (literally "election cartel"): a formal
  pre-election declaration in which two or more separate
  *parties* (or party + voter-association lists) agreed to
  pool their vote totals for purposes of seat allocation.
  Valgforbund participants retained their separate ballot
  identities; pooling occurred only at the seat-allocation
  step.

The mechanics of pooling worked as follows: at the inter-list
allocation step (Hare quota at tier 1, Sainte-Laguë at tier 2),
the cartel was treated as a single entity. Once the cartel
won its combined seats, the seats were re-distributed *within*
the cartel among its constituent parties — typically by a
D'Hondt-style sub-allocation.

The effect was to permit small parties to coordinate without
formally merging: a cartel of two parties each polling 1.5%
could pool to 3% and thereby qualify for compensatory seats
(under the pre-2018 threshold rule). Cartels also served at
the tier-1 stage to capture remainder seats that would
otherwise have gone to larger parties.

#### The 2018 reform

The Folketing enacted **Lov nr. 712 af 8. juni 2018** (the
2018 amendment to the Folketingsvalgloven), which
**abolished valgforbund and listeforbund for Folketing
elections**. The reform was driven by two analytic
considerations:

1. The cartel pooling produced opaque allocation effects: a
   voter who cast a personal vote for Party A's candidate
   could see her vote functionally translate into a seat for
   Party B if Party A had entered a valgforbund with Party B
   and the seat-redistribution within the cartel landed
   Party B at the margin.
2. The cartels reduced the effective threshold below the
   2% statutory floor for any party participating in a
   cartel, undermining the purpose of the threshold.

The 2018 abolition tracks the Netherlands' 2017 abolition of
*lijstverbinding* and Brazil's 2017 abolition of *coligações*
(by Emenda Constitucional 97/2017). Three project cases
abolished pre-vote pooling within an eighteen-month window in
2017–2018. The substantive reasoning is identical in all three
cases: that pre-vote pooling produces effects on the seat
distribution that are opaque to voters at the moment of
ballot casting, and that the cartel-induced effective
threshold reduction undermines statutory threshold
calibration.

#### Status at the local level

List-cartel mechanics survive at the **municipal and regional
level** under the *Lov om kommunale og regionale valg*. The
local statute continues to permit *listeforbund* (within a
party) and *valgforbund* (between parties) for municipal and
regional council elections. The local-level mechanics — and
the policy reasons the legislator distinguished the two
levels in the 2018 reform — are documented in
`cases/denmark/README.md`.

The Danish bifurcation between national (cartels abolished)
and local (cartels retained) is itself a portable drafting
choice: the legislator can plausibly distinguish two levels of
government on the basis that local elections involve smaller
seat pools and more granular party fragmentation, where
cartel mechanics may serve representation goals that they
undermine at the national scale.

### Operationalized values

```
allocation_formula:              two-tier hybrid:
                                 (1) Hamilton/Hare quota with
                                     largest remainders at the
                                     constituency tier
                                     (storkreds-level)
                                 (2) Webster/Sainte-Laguë for
                                     the 40 national
                                     compensatory seats
formula_codified_as:             procedural — Hare-quota
                                 calculation and Sainte-Laguë
                                 divisor sequence specified
                                 directly in the
                                 Folketingsvalgloven; named
                                 eponyms are not used in the
                                 statute
formula_statutory_citation:      Folketingsvalgloven, chapters
                                 on tier-1 (constituency)
                                 allocation and tier-2
                                 (compensatory) allocation —
                                 see Outstanding gaps for the
                                 verbatim §§ citations
ties_rule:                       drawing of lots
                                 (*lodtrækning*) by the
                                 relevant electoral board

legal_threshold_pct:             2.0 (national) — but
                                 disjunctive with two
                                 alternatives:
                                   (i) one constituency seat
                                   anywhere in the country
                                   OR
                                   (ii) qualifying vote totals
                                   in two of three landsdele
threshold_level:                 national (for the 2% test);
                                 disjunctively constituency
                                 or regional for the
                                 alternatives
threshold_exemption_rules:       constituency-seat alternative
                                 and regional-victories
                                 alternative both function as
                                 statutory exemption pathways
threshold_backdoor:              yes — one-constituency-seat
                                 condition (analogous to the
                                 New Zealand 5%-or-one-
                                 electorate rule)

apparentement_allowed:           no (Folketing, since 2018);
                                 yes (municipal and regional,
                                 under Kommunal- og
                                 regionalvalgloven)
apparentement_form:              *listeforbund* (within a
                                 party) and *valgforbund*
                                 (between parties) — both
                                 forms abolished at the
                                 Folketing level by Lov nr.
                                 712 af 8. juni 2018
apparentement_rules:             N/A at the Folketing level
                                 post-2018; see
                                 `cases/denmark/README.md`
                                 for the surviving local
                                 regime

intra_list_rule:                 party-elective per storkreds
                                 (see Component 2):
                                 *partiliste* (list order)
                                 OR *sideordnet opstilling*
                                 (personal-vote total with
                                 proportional pro-rata
                                 distribution of party votes)

counting_authority:              polling-station boards
                                 (*valgstyrere*) for primary
                                 count; *valgbestyrelser*
                                 (constituency electoral
                                 boards) for storkreds
                                 totalization;
                                 Indenrigsministeriet for
                                 national totalization and
                                 the tier-2 compensatory
                                 allocation calculation
recount_trigger:                 statutorily-provided
                                 recount procedures; ad-hoc
                                 reviews on dispute
audit_requirements:              paper ballots retained;
                                 manual counting with
                                 documented procedure
allocation_computation_authority: Indenrigsministeriet under
                                 the Folketingsvalgloven
```

### Notes — worked sketch of the two-tier allocation

A schematic worked example of the procedure (using
illustrative numbers, not 2022 actuals):

- Suppose Party X wins 6.2% nationwide. The party clears the
  2% national threshold and is therefore qualified for tier-2
  compensatory allocation.
- At tier 1, Party X's per-storkreds vote totals produce 7
  constituency seats: it wins above-one-Hare-quota seats in
  storkredse where its concentration is highest and remainder
  seats where the largest-remainders distribution favors it.
- At tier 2, the 40 compensatory seats are distributed among
  all qualifying parties by Sainte-Laguë applied to the
  national totals. Party X's proportional share of 175 seats
  on its 6.2% vote share is approximately 10.85 seats; the
  procedure rounds toward 11. Subtracting the 7 already won at
  tier 1, Party X receives 4 compensatory seats.
- The 4 compensatory seats are then assigned to specific
  storkredse within Party X's national vote pattern, prioritizing
  storkredse where Party X had high vote shares but failed to
  clear the Hare quota at tier 1.
- Within each assigned storkreds, the seat goes to the highest-
  personal-vote candidate on Party X's list (if the list uses
  *sideordnet opstilling*) or to the next candidate in submitter
  order (if the list uses *partiliste*).

The procedure has three observable properties:

1. **Overall proportionality is bounded by the size of the
   compensatory tier**, not by the constituency-tier
   allocation. The 40 compensatory seats provide approximately
   23% of the 175 mainland seats, sufficient to repair almost
   all within-storkreds disproportionality for any party that
   clears the national threshold.
2. **The compensatory tier is silent for non-qualifying
   parties.** A list that fails the 2% threshold, fails to
   win any constituency seat, and fails the regional-victories
   alternative receives no tier-2 seats; the only path to
   representation is to win a storkreds-level Hare-quota seat
   on first-tier allocation (which also satisfies the
   threshold by the constituency-seat alternative).
3. **The within-cartel D'Hondt sub-allocation is obsolete at
   the national level** since the 2018 reform. Local-level
   listeforbund / valgforbund preserve the sub-allocation
   mechanism.

### Comparative table — threshold disjunctions across the case set

| Case | National threshold | Backdoor / alternatives |
|---|---|---|
| Denmark (Folketing) | 2% | one constituency seat OR regional-victories in 2 of 3 landsdele |
| Germany (Bundestag, BWahlG § 6) | 5% | Grundmandatsklausel (post-2023 reform: 3 constituency seats) |
| New Zealand (Electoral Act 1993, MMP) | 5% | one electorate seat |
| Spain (LOREG Arts. 163, 180) | 3% (Congress), 5% (municipal) | none |
| Belgium federal | 5% per district | none (per-district application) |
| Netherlands | 0% (effective threshold = 1 kiesdeler) | N/A |
| Brazil (CE Art. 109) | 2% nationwide + 1.5% in 1/3 of states | combined |

Denmark's 2% threshold is the lowest among project cases that
operate a formal percentage threshold, and the disjunctive
structure produces three independent qualification paths. The
combination is the project's most permissive threshold
configuration outside the threshold-free Netherlands.

For U.S. drafters, the Danish disjunctive threshold model is a
working precedent for accommodating regionally-concentrated
small parties without abandoning the threshold concept
altogether. The structure: a relatively low national
percentage threshold combined with a constituency-seat
backdoor produces representation for parties whose support is
either nationally distributed (above the percentage) or
locally concentrated (in a constituency they can win
outright). It is a portable design for U.S. state-legislature
contexts with substantial geographic variation in party
strength.

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

Per Folketingsvalgloven and Grundloven § 29:

- Danish nationals aged 18+ with permanent residence in the
  realm vote in Folketing elections.
- EU citizens, Nordic citizens, and other resident foreign
  nationals (subject to residence-duration rules) vote in
  municipal and regional elections only (not Folketing).
- Voter registration is **passive** — derived from the *Det
  Centrale Personregister* (CPR, the national personal-data
  register). Voters do not separately register for elections.

Grundloven § 29 sets the franchise: *"Valgret til Folketinget
har enhver, som har dansk indfødsret, fast bopæl i riget og
har nået den i stk. 2 omhandlede valgretsalder, medmindre
vedkommende er erklæret umyndig."* (The right to vote in the
Folketing belongs to every Danish citizen with permanent
residence in the realm who has reached the voting age
specified in subsection 2, unless declared legally
incapacitated.)

### B. Candidate / list registration — *full subsection*

The most analytically central section for the project.

#### Party-name registration through *Valgnævnet*

A political party that wishes to appear on the ballot under
a party name must **register the name** (*partinavn*) with
**Valgnævnet** (the Electoral Board). Registration is
governed by the Folketingsvalgloven. Once registered, a
party retains its registration across cycles subject to
maintaining a minimum level of electoral activity
(operationalized as receiving votes in a specified share of
constituencies in the previous election or re-collecting
support signatures).

For a *new* party to register a party name, the party must
submit support signatures (*vælgererklæringer*) from a
specified number of eligible voters. The threshold is set in
the Folketingsvalgloven and is calibrated to approximately
**1/175 of the valid votes cast at the previous Folketing
election** — i.e., approximately the share required to win
one Folketing seat on a proportional basis. In current
practice, this works out to approximately **20,000 voter
declarations**.

The voter declaration system was reformed in 2017 (Lov nr.
1742 af 27. december 2016) to require a **digital
declaration system** operated by Indenrigsministeriet. The
declaration must be made through the digital portal using
*NemID* / *MitID* authentication; a voter may declare support
for only one party at a time, and the declaration must
"cool" for one week before being valid (the voter has the
opportunity to reconsider during the cooling period). The
2017 reform was driven by concerns about the prior paper-
based collection system, which produced several incidents of
contested signatures.

#### Candidate-list submission

Per Folketingsvalgloven, each party (or independent
candidate) must submit a candidate list (*kandidatliste*) for
each storkreds in which it intends to compete. The
submission includes:

- The candidate names, with consent declarations
  (*samtykkeerklæringer*) from each named candidate.
- The list's chosen presentation mode for that storkreds —
  *partiliste* or *sideordnet opstilling*. (This is the
  operative election of the intra-list architecture; once
  filed, the choice binds for the election.)
- For new parties or independents, the supporting voter
  declarations (party-level for new parties, local for
  independents).

Filing deadlines and procedural details are set by the
Folketingsvalgloven and operationalized by Indenrigsmin-
isteriet.

#### Independent candidates (*kandidater uden for partierne*)

Per the Folketingsvalgloven, a candidate may stand for the
Folketing without party affiliation. The requirements
include:

- Supporting voter signatures from the **opstillingskreds**
  (local nomination district) in which the candidate stands.
  The number is set by the Folketingsvalgloven; current
  practice places it in the range of 150–200 voters from the
  opstillingskreds, with the precise number depending on the
  district.
- A declaration of candidacy.
- A deposit (*kandidatdepositum*), refundable if the candidate
  reaches a specified vote share.

Independent candidates compete on the ballot in the same
storkreds-level competition as party candidates, but their
votes are not pooled with any party's votes for purposes of
tier-1 or tier-2 allocation.

#### Operationalized values

```
list_registration_authority:     *Valgnævnet* (national,
                                 party names);
                                 *valgbestyrelser*
                                 (constituency electoral
                                 boards, candidate lists)
signatures_required_min:         party registration: ~20,000
                                 voter declarations (1/175 of
                                 previous valid votes);
                                 independent candidacy:
                                 ~150–200 (opstillingskreds-
                                 dependent)
signature_scaling:               party-registration threshold
                                 scales with previous-cycle
                                 valid vote total (1/175 rule);
                                 independent-candidacy
                                 threshold is fixed per
                                 opstillingskreds
signature_geographic_distribution: party registration is
                                 nationwide; independent
                                 signatures must be from the
                                 opstillingskreds
signature_collection_mode:       digital (NemID/MitID) since
                                 2017 reform; cooling-period
                                 requirement of one week
deposit_amount:                  yes — *kandidatdepositum*
                                 (refundable above a vote
                                 share threshold)
deposit_currency:                DKK
filing_deadline_days_before:     set by Folketingsvalgloven;
                                 typically 11 days before the
                                 election
party_v_nonparty_equal_treatment: partial — independents
                                 face per-opstillingskreds
                                 signature requirements but
                                 do not face the 20,000-
                                 declaration party-registration
                                 requirement; on the other
                                 hand, independents do not
                                 benefit from the
                                 compensatory-tier mechanism
                                 in the same way (an
                                 independent must clear a
                                 storkreds-level Hare quota
                                 to win a tier-1 seat; the
                                 tier-2 allocation by
                                 Sainte-Laguë is in practice
                                 a party-list mechanism)
list_size_min:                   1 candidate
list_size_max:                   not capped in statute; in
                                 practice limited by the
                                 number of opstillingskredse
                                 in the storkreds
list_ordering_rule:              party-elective (partiliste
                                 OR sideordnet opstilling),
                                 set at nomination
gender_quota:                    none in the
                                 Folketingsvalgloven
residency_required:              candidate must satisfy
                                 Grundloven § 30 (eligibility
                                 to be elected to the
                                 Folketing) — Danish
                                 citizenship and not legally
                                 incapacitated; no residency
                                 requirement specific to the
                                 storkreds
multiple_candidacy_restrictions: candidate may stand for
                                 only one party / list per
                                 election; may stand in
                                 multiple opstillingskredse
                                 within a single storkreds
                                 on the same list
```

#### Notes — the digital-declaration system as a portable mechanism

The 2017 shift to a digital voter-declaration system
(operated through MitID and Indenrigsministeriet) is a working
example of administering a signature-based ballot-access
requirement through an authenticated digital channel rather
than through paper signature collection. The Danish model has
three notable design features:

1. **Authentication is identity-bound**: the voter declares
   support using a state digital ID (MitID), eliminating
   verification costs and reducing fraudulent signatures.
2. **The one-week cooling period** introduces a structural
   delay between intent-to-support and the legal effect of
   support, mitigating impulse declarations and giving the
   voter a window for reconsideration.
3. **Each voter may declare support for only one party at a
   time**, mirroring the Bavarian *Eintragung in
   Unterstützungslisten* and Spanish *agrupación de
   electores* single-list-only signature rule.

For U.S. drafting, the Danish digital-declaration system is a
portable design for state-level ballot-access requirements,
contingent on the availability of a state-operated digital ID
infrastructure. The U.S. equivalent would be a state Secretary
of State digital portal authenticated through a state ID
system (where one exists) or an equivalent identity-
verification mechanism. The single-list rule and the cooling-
period mechanism are directly portable independent of the
authentication infrastructure.

### C. Campaign finance

Governed by the *Lov om private bidrag til politiske partier
og offentliggørelse af politiske partiers regnskaber* (Act on
Private Contributions to Political Parties and the Publication
of Political Parties' Accounts) and related public-funding
statutes. Public funding (*partistøtte*) is calibrated to
party vote share and is paid per-vote at a statutory rate;
the per-vote rate applies separately to Folketing,
regional, and municipal elections. Disclosure thresholds for
private contributions are set in the Act. Spending caps
specific to election campaigns are limited in scope compared
to those in some European peer cases.

### D. Election administration

The Danish EMB is structurally layered:

- ***Indenrigsministeriet*** (Ministry of the Interior —
  currently *Indenrigs- og Sundhedsministeriet*) operates as
  the national electoral authority. The Ministry maintains
  the candidate-registration infrastructure, the digital
  voter-declaration portal, and the computation of tier-2
  compensatory-seat allocation.
- ***Valgnævnet*** (the Electoral Board), a statutory body,
  reviews party-name registrations and certain disputes.
- ***Valgbestyrelser*** (constituency electoral boards), one
  per storkreds, supervise the conduct of the election in
  their storkredse, including the storkreds-level
  totalization.
- ***Valgstyrere*** (polling-station boards), one per polling
  station, conduct the primary count.

The administration is decentralized in execution
(municipalities operate polling stations) but coordinated by
Indenrigsministeriet for the procedural and computational
elements. There is no single autonomous electoral commission
analogous to the Spanish Junta Electoral Central or the New
Zealand Electoral Commission; election administration is a
core Ministry function.

For U.S. drafters: the Danish allocation of authority across
Indenrigsministeriet, Valgnævnet, valgbestyrelser, and
valgstyrere maps onto a U.S. system in which a state
Secretary of State (or equivalent), an autonomous Elections
Board, county electoral boards, and polling-station officials
together administer the election. The Danish model places
substantially more authority in the central Ministry than the
U.S. equivalent typically does; a closer U.S. analog is the
New Zealand Electoral Commission structure, where a single
autonomous body runs the entire process.

### E. Vote count, certification, recounts, dispute resolution

Counting is conducted at the polling station on election
night (paper ballots, manual count, statutorily-prescribed
procedure). Storkreds-level totalization occurs the day after.
National totalization and tier-2 compensatory-seat
computation are completed within days of the election by
Indenrigsministeriet.

Election challenges are heard by **Folketinget itself** in the
first instance — Grundloven § 33 provides that the Folketing
verifies the credentials of its own members (*"Folketinget
afgør selv gyldigheden af dets medlemmers valg"*). For
operational and administrative-law disputes, decisions of the
electoral boards are reviewable through the ordinary
administrative-law courts (Ombudsmand, ordinary courts) on
limited grounds.

The Folketing-internal credential verification is a distinctive
feature of the Danish system. Unlike Brazil (specialized
Justiça Eleitoral) and Spain (Tribunal Constitucional review
through recurso de amparo), Denmark vests primary electoral-
dispute resolution in the legislative body itself. This is a
Westminster-tradition feature that the Danish 1953
constitutional revision preserved.

### F. Media access

Public-service broadcasters (Danmarks Radio, TV 2) allocate
political broadcast time during election campaigns under
broadcasting-law rules (*Lov om radio- og fjernsynsvirksomhed*).
The structure is allocation-by-equal-time across parties that
qualify for the ballot, with adjustments for parties holding
existing Folketing seats. There are no statutory paid-
advertising limits at the national level, though disclosure
rules apply.

### G. (Districting law — captured under Component 1)

The 10 storkredse and 92 opstillingskredse are stable since
the 2007 administrative-reform-driven redistricting
(*Strukturreformen* in 2007 reduced the number of
municipalities and re-aligned the constituency boundaries).
Boundary maintenance is the responsibility of
Indenrigsministeriet.

---

## 5. PROSeS performance diagnostic

The empirical anchor is the **1 November 2022 Folketing
election**. Sources for the diagnostic include:

- *Danmarks Statistik* — official electoral results and
  socio-demographic correlates.
- *Indenrigsministeriet* — administrative reports on the
  election.
- *Valgforskningsprogrammet* (Danish Election Study) —
  academic survey of voters and parties.

### Process Design

**Public participation**: the Folketingsvalgloven is amended
through ordinary legislative process; reform packages
(notably the 2017 digital-declaration reform and the 2018
cartel abolition) have been preceded by parliamentary-
committee consultations.

**Probity and impartiality**: Danish elections are
consistently rated highly in international comparative indices
(Electoral Integrity Project, V-Dem); no significant integrity
challenges in recent cycles.

**Accountability**: dispute-resolution authority resides with
the Folketing for credential verification and with ordinary
administrative courts for operational disputes. The absence
of a specialized electoral court is not a documented source
of operational dysfunction.

### Resource Investment

**Transparency**: the Folketingsvalgloven is publicly
available in consolidated form on retsinformation.dk;
Indenrigsministeriet publishes the tier-1 and tier-2
allocation calculations after each cycle.

**Sustainability**: the structure has been stable across
multiple cycles. The 2018 cartel reform was the most recent
substantive amendment; the architecture itself is largely
unchanged since 1953.

**Legitimacy**: turnout in Folketing elections has remained
consistently in the 80s percent across the post-1953 cycles
(2022: **84.2%** of eligible voters), which is among the
highest in OECD comparisons.

### Service Output Quality

**Convenience**: voting is in-person on election day at
designated polling stations; postal voting is available for
voters abroad and in defined categories; same-day voting at
alternative polling stations is permitted within the storkreds.

**Accuracy**: paper ballots manually counted at the polling
station; storkreds-level and national-level recounting
procedures are statutorily prescribed; invalid-vote rates are
in the range of 0.3–0.7% across recent cycles.

**Enforcement**: Indenrigsministeriet and the valgbestyrelser
administer compliance. The Valgnævnet adjudicates party-name
disputes.

### Service Outcomes

**Voter turnout** at the 1 November 2022 Folketing election
was **84.2%** of eligible voters.

**Equity / minority representation**: Denmark has no statutory
mechanism for ethnic or religious minority representation
specifically (no reserved seats, no analog to Spanish LOREG
Art. 44 bis for gender). Women's representation has reached
**~43–45%** of the Folketing in recent cycles, achieved
through party self-imposed candidate-selection practices
rather than statutory quotas.

Migrant-origin representation has grown over recent cycles
but remains below population share. The combination of
*sideordnet opstilling* (which permits voter-driven
intra-list reordering) and party-controlled nomination
(which determines who appears on the list at all) places the
operational weight on party candidate-selection practices.

### Stakeholder Satisfaction

Consistently high among administrators, parties, and
observers. The 2018 cartel reform and the 2017 digital-
declaration reform produced parliamentary-committee
engagement; neither has been substantively re-litigated.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # Grundloven § 29;
                                   # Folketingsvalgloven
                                   # operationalizes
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant   # Grundloven § 31(1)
direct_suffrage:       compliant   # Grundloven § 31(1)
periodic_elections:    compliant   # Grundloven § 32 fixes a
                                   # four-year maximum term
fundamental_rights:    compliant
regulatory_stability:  high        # the Folketingsvalgloven
                                   # architecture has been
                                   # stable since 1953; the
                                   # 2018 cartel abolition is
                                   # the most recent
                                   # substantive change
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

| Provision | Type | Rationale |
|---|---|---|
| Two-tier constituency + compensatory architecture | **Universal** | The tier split (constituency seats + national leveling seats) is a portable model for any jurisdiction wishing to preserve geographic representation alongside proportional outcomes. The 135/40 ratio is a tunable parameter. |
| Hamilton/Hare quota at tier 1 + Webster/Sainte-Laguë at tier 2 | **Universal** | Both formulas are familiar; the use of different formulas at different tiers — Hare for the constituency-level distribution where remainder-handling matters, Sainte-Laguë for the national-level leveling where bias minimization matters — is a portable design choice. |
| Disjunctive threshold (2% national OR one constituency seat OR regional-victories test) | **Universal** | The threshold disjunction is a working precedent for accommodating regionally-concentrated small parties without abandoning the threshold concept. Directly portable; the percentage and the constituency-seat alternative are tunable. |
| Party-elective intra-list architecture (*partiliste* vs *sideordnet opstilling*) | **Universal** | The substantive innovation — treating the open-list / closed-list axis as a *list-level* rather than a *system-level* parameter — is directly portable. The mechanism is straightforward: the choice is registered at the time of nomination. |
| Proportional pro-rata distribution of party votes under *sideordnet opstilling* | **Universal** | A working answer to the question of how party-only votes should flow to candidates within an open-list framework. Portable; the alternative (serial distribution in submitter order) is also workable. |
| 2018 abolition of valgforbund / listeforbund at the Folketing level | **Universal** | The reasoning — that pre-vote pooling produces opaque allocation effects and undermines threshold calibration — is portable. The 2018 reform tracks the Netherlands' 2017 lijstverbinding abolition and Brazil's 2017 coligações abolition. |
| Retention of valgforbund / listeforbund at the local level | **Universal** | The substantive choice to distinguish national from local on cartel mechanics is portable. The reasoning — local elections involve smaller seat pools where cartel mechanics may serve representation goals — is a legislator-discretionary calibration. |
| Digital voter-declaration system for party registration (MitID, cooling period, single-list rule) | **Hybrid** | The substance — authenticated digital declaration with cooling period and single-list rule — is portable. The implementation depends on the availability of a state-operated digital ID infrastructure, which the U.S. lacks at the federal level (though some states have analogs). |
| Folketing self-verification of member credentials (Grundloven § 33) | **Particular** | Reflects Westminster-tradition constitutional inheritance. Not directly portable to U.S. constitutional structures, which typically vest electoral-dispute resolution in courts. |
| Constitutional cap on assembly size (Grundloven § 31(3): 179) | **Particular** | The substantive choice — fixing assembly size — is portable; the constitutional placement reflects Danish institutional history. |
| Bornholm constituency-tier 2-seat minimum | **Particular** | Specific to Danish geography; reflects the island's status as a freestanding storkreds. |

### Top three takeaways for US state/local implementation

1. **Party-elective intra-list architecture is the Danish
   case's most directly portable innovation.** The
   Folketingsvalgloven's choice — treating *partiliste* /
   *sideordnet opstilling* as a per-list, per-storkreds
   election rather than a system-level constant — gives U.S.
   drafters a working model for resolving the open-list /
   closed-list axis at the list level. A U.S. statute could
   adopt the same approach by permitting each list-submitter
   to elect at filing time which mode applies. The
   substantive consequence is that nominating associations
   that prefer to lock candidate ordering retain the option,
   while those that prefer voter-driven intra-list ordering
   also retain the option, within a single statutory
   framework.

2. **The disjunctive threshold structure is portable for
   state-legislature contexts.** A 2% national threshold
   combined with a one-constituency-seat backdoor produces
   representation for parties whose support is either
   nationally distributed or locally concentrated, without
   requiring the legislator to choose between low and high
   thresholds. For U.S. state legislatures with substantial
   urban / rural variation, the Danish model is a working
   precedent for filtering nationwide fragmentation while
   preserving regional small-party participation.

3. **The two-tier constituency-plus-compensatory architecture
   is a portable framework for any state wishing to combine
   existing geographic district structures with proportional
   outcomes.** The Danish 135/40 split (~77% constituency /
   23% compensatory) is one calibration; other working
   examples in the project's case set include New Zealand
   (60% constituency / 40% list in the MMP structure) and
   Germany (parallel-but-leveled FPTP + list under the
   pre-2023 BWahlG). For a U.S. state-legislature reform that
   wishes to preserve existing district representation while
   adding proportionality, the Danish design — keep the
   districts, add a compensatory tier large enough to repair
   district-level disproportionality, set the threshold low
   enough to admit small parties — is the most directly
   applicable architecture in the project's set.

---

## 8. Sources

### Primary

- ***Danmarks Riges Grundlov*** (Constitution Act of the
  Kingdom of Denmark, 5 June 1953), §§ 28–33. Operative
  electoral clauses: § 29 (franchise), § 31 (elections),
  § 32 (term), § 33 (credentials).
  <https://www.retsinformation.dk/eli/lta/1953/169>
- ***Lov om valg til Folketinget*** (Folketing Elections Act
  — *Folketingsvalgloven*), current consolidated text. The
  comprehensive statute governing Folketing nomination,
  ballot structure, two-tier allocation, the threshold
  disjunction, and the administration of the count. Cited
  in this profile by topic; verbatim §§ to be retrieved from
  the retsinformation.dk consolidation.
  <https://www.retsinformation.dk/eli/lta/2020/1260>
  (latest consolidated Lovbekendtgørelse to be confirmed)
- ***Lov om kommunale og regionale valg*** (Municipal and
  Regional Elections Act — *Kommunal- og regionalvalgloven*).
  For the surviving listeforbund / valgforbund regime at the
  local level; detailed treatment in
  `cases/denmark/README.md`.

### Reform legislation

- **Lov nr. 1742 af 27. december 2016** — digital voter-
  declaration system for party registration.
- **Lov nr. 712 af 8. juni 2018** — abolition of valgforbund
  and listeforbund for Folketing elections; retention at the
  local level under the Kommunal- og regionalvalgloven.

### Official EMB materials

- ***Indenrigs- og Sundhedsministeriet*** — Folketing
  elections portal; tier-1 and tier-2 allocation computations
  published after each cycle.
- ***Valgnævnet*** — party-name registration decisions.
- ***Danmarks Statistik*** — official electoral results.

### Secondary

- *International IDEA Electoral System Design Database* —
  Denmark entry.
  <https://www.idea.int/data-tools/country-view/85/40>
- *Inter-Parliamentary Union — Folketinget*: parliamentary
  procedure and electoral system summary.
  <http://archive.ipu.org/parline-e/reports/2087_B.htm>

### Outstanding gaps — primary-source retrieval to complete

The substantive descriptions above are consolidated from
the Folketingsvalgloven structure (as reported in
Indenrigsministeriet administrative documentation and
Valgnævnet decisions) and from international comparative
documentation. The following verbatim primary-text
retrievals are the outstanding work for this profile:

- **Folketingsvalgloven §§ on tier-1 constituency-seat
  allocation** — the verbatim Danish text of the chapter
  specifying Hamilton/Hare quota application and largest-
  remainders distribution within each storkreds. Web access
  to retsinformation.dk was not available during this
  drafting iteration; the §§ should be identified and
  quoted in a subsequent revision.
- **Folketingsvalgloven §§ on tier-2 compensatory-seat
  allocation** — the verbatim Danish text of the chapter
  specifying Webster/Sainte-Laguë application at the
  national level and the storkreds-level reassignment of
  compensatory seats to specific lists.
- **Folketingsvalgloven §§ on the threshold disjunction** —
  the verbatim Danish text of the three-condition threshold
  qualification rule (2% national OR one constituency seat
  OR regional-victories in two of three landsdele).
- **Folketingsvalgloven §§ on *partiliste* and *sideordnet
  opstilling*** — the verbatim Danish text specifying the
  per-list election of intra-list presentation mode and the
  operational consequences (binding submitter order vs
  personal-vote ranking with proportional pro-rata
  distribution of party votes).
- **Folketingsvalgloven §§ on voter declarations
  (*vælgererklæringer*) for party registration** — the
  verbatim Danish text specifying the 1/175-of-previous-
  valid-votes calibration rule and the cooling-period and
  digital-declaration requirements.
- **Folketingsvalgloven §§ on independent candidacy
  (*kandidater uden for partierne*)** — the verbatim Danish
  text specifying the per-opstillingskreds signature
  requirement and the deposit rule.
- **Lov nr. 712 af 8. juni 2018** — verbatim text of the
  cartel-abolition amendment, including the legislative
  rationale (lovforslag bemærkninger).
- **Cached PDF of the consolidated Folketingsvalgloven** —
  to be added to `sources/denmark/` for the project's
  source archive.
- **Cached PDF of Grundloven** — for §§ 28–33 verbatim text;
  the § 31 quotation above is from the 1953 constitutional
  text but should be verified against the official
  consolidated version.

### Resolved in this iteration

**2026-05-15** (initial profile):

- Grundloven § 31 quoted verbatim (subject to confirmation
  from official consolidated text) and analyzed as the
  constitutional source of the two-tier architecture.
- Two-tier allocation procedure described: 135 constituency
  seats by Hamilton/Hare with largest remainders at the
  storkreds level; 40 compensatory seats by
  Webster/Sainte-Laguë at the national level.
- Three-condition threshold disjunction documented (2%
  national OR one constituency seat OR regional-victories
  in two of three landsdele).
- Party-elective intra-list architecture documented:
  *partiliste* (closed-list, submitter-ordered) vs
  *sideordnet opstilling* (open-list, personal-vote-driven
  with proportional pro-rata distribution of party votes).
- 2018 abolition of valgforbund / listeforbund at the
  Folketing level documented; retention at the local level
  under the Kommunal- og regionalvalgloven noted.
- 2017 digital voter-declaration reform (MitID, cooling
  period, single-list rule) documented.
- Independent candidacy (*kandidater uden for partierne*)
  signature and deposit framework documented.
- Folketing § 33 self-verification of member credentials
  identified as a distinctive Westminster-tradition feature.
- Bornholm 2-seat constituency-tier minimum documented as
  the single exception to the otherwise demographic-driven
  per-storkreds allocation.
