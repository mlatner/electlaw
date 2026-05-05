# Flanders — Local elections (Gemeenteraadsverkiezingen)

## 0. Case metadata

- **Country**: Kingdom of Belgium
- **Sub-jurisdiction**: Flemish Region (*Vlaams Gewest*) — 300
  municipalities in Flanders.
- **Level of government**: Local — *Gemeenteraad* (municipal
  council). Mayor (*burgemeester*) is appointed by the Flemish
  government on the council's recommendation.
- **Electoral system family**: **Open-list PR** with **Imperiali
  allocation**. Single vote, cast as either a list vote
  (*lijststem* / *kopstem*) or one or more candidate
  preference votes within a single list. Each municipality is
  a single electoral district; M = total council size.
- **Governing statute**: ***Lokaal en Provinciaal Kiesdecreet***
  van 8 juli 2011 (BS 25 juli 2011), as amended through 2023
  (most relevant: the 2021 amendment ending compulsory voting
  at municipal level, and the 2023 amendment to the *lijststem*
  effect on intra-list ordering).
- **Implementing regulation**: *Uitvoeringsbesluit* of the
  Flemish Government.
- **Constitutional anchor**: Belgian Constitution Art. 41
  (municipal autonomy); Art. 162 (regional competence over
  municipal organization since the 2014 *Zesde Staatshervorming*
  / Sixth State Reform).
- **Last regular election**: **13 October 2024** — the first
  election held under the post-2023 *Lokaal en Provinciaal
  Kiesdecreet* amendments, including the abolition of the
  *lijststem* effect on intra-list ordering and the abolition
  of compulsory voting.
- **Analyst**: this profile, 2026-05-05.

### Why this case is in the project

Three features make Flanders the project's analytical center
for the **Imperiali formula** and for **list-vote-meaning
reform**:

1. **Imperiali allocation** — the Flemish *Lokaal en Provinciaal
   Kiesdecreet* uses the Imperiali divisor sequence (1, 1.5, 2,
   2.5, 3, 3.5, …) for inter-list seat distribution. Imperiali
   produces stronger large-party bias than D'Hondt and is the
   project's only working Imperiali jurisdiction.
2. **2023 reform of the *lijststem* effect**: the *pot-system*
   — under which list votes flowed to candidates in submitter-
   set order until each had reached an *éligibilité* quota —
   was abolished for the 2024 cycle. The list vote remains as
   an inter-list count, but no longer affects intra-list
   ordering. Intra-list seats now go strictly to candidates by
   personal vote totals.
3. **2021 abolition of compulsory voting** at municipal level
   only (compulsory voting remains at federal and regional
   levels). The 2024 cycle was the first under voluntary
   municipal voting.

The Flemish 2023 reform produces a system close to the Bavarian
GLKrWG Art. 36(1) "pure preference" intra-list rule — but with
Imperiali rather than Sainte-Laguë inter-list allocation, and
with the list vote still serving its inter-list-counting
function. This combination is unique in the project's set.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

Council size in Flanders is set in the *Lokaal en Provinciaal
Kiesdecreet* (or the *Decreet over het Lokaal Bestuur*; verify
exact location) on a population-tiered table. The structure is
broadly similar to Bavarian GO Art. 31 and Dutch Gemeentewet
Art. 8:

- **Smallest municipalities** (~1,000 inhabitants): ~7 seats.
- **Mid-size municipalities** (10,000–20,000 inhabitants):
  17–25 seats.
- **Antwerpen** (~530,000 inhabitants — the largest Flemish
  city): 55 seats.

Each municipality is a single electoral district. M = total
council size for the municipality.

### Operationalized values

```
total_seats:                     ~7 (smallest) — 55 (Antwerpen)
codification_instrument:         Decreet over het Lokaal Bestuur
                                 (governance act); council-size
                                 schedule cross-referenced in the
                                 Lokaal en Provinciaal
                                 Kiesdecreet
amendment_authority:             Vlaams Parlement
amendment_threshold:             ordinary regional legislation

magnitude_uniform:               yes within each municipality
magnitude_typical:               population-determined
districts_count:                 1 per municipality
districting_authority:           N/A — district = municipality
districting_frequency_years:     N/A
districting_criteria_in_statute: N/A

tiered:                          no
threshold_of_exclusion_pct:      structural (1/(M+1)); operative
                                 threshold dominated by Imperiali
                                 large-party bias
```

### Notes

The Flemish council-size schedule is set in regional legislation
since the 2014 *Zesde Staatshervorming* transferred competence
over municipal organization from the federal to the regional
level. Wallonia and the Brussels-Capital Region maintain
parallel but separately legislated schedules.

For U.S. drafters: the Flemish placement of the schedule in
regional rather than federal law mirrors the U.S. federalist
allocation of municipal organization to states. The amendment
threshold is ordinary regional legislation — politically
tractable.

---

## 2. Component 2 — Ballot Structure

### The single vote: lijststem or candidate preferences

Per the *Lokaal en Provinciaal Kiesdecreet*, each voter casts
one vote, expressed in one of two ways:

- **Lijststem (kopstem / list vote)**: the voter marks the head
  box (*kopvak*) of a single list. Counts toward the list's
  total for inter-list allocation under Imperiali. Since the
  2023 reform, **the lijststem no longer flows to candidates in
  submitter-set order**.
- **Candidate preference vote(s)**: the voter marks one or more
  candidates within a single list. Each preference mark counts
  for the candidate (intra-list ordering) and for the list
  (inter-list allocation under Imperiali).

Cross-list voting (panachage) is **not** permitted at municipal
level, paralleling the federal rule.

### The 2023 reform — abolition of the *pot-system*

Pre-2023 (and in Wallonia, Brussels, and at federal level),
the Flemish system used a *pot-system* (sometimes called
*devolutie*) under which:

1. List votes were "pot" votes flowing to candidates in
   submitter-set order;
2. Each pot vote brought the next candidate in order closer to
   the *éligibilité* quota;
3. Candidates who reached the quota through some combination of
   personal preference votes and pot votes took seats in the
   list's seat allocation.

The 2023 amendment to the *Lokaal en Provinciaal Kiesdecreet*
**abolished the pot-system effect on intra-list ordering**.
Under the post-2023 rule:

- The lijststem still counts toward the list's total for
  inter-list allocation.
- But list votes do **not** flow to candidates in submitter-set
  order to reach the éligibilité quota.
- Candidates within a winning list are seated **strictly in
  descending order of their personal preference votes**.

The reform is the closest the project has documented to a clean
pivot from a flexible-list architecture (Belgium federal,
pre-2023 Flemish local) to a pure-preference architecture
(Bavaria GLKrWG Art. 36(1)).

### Operationalized values

```
ballot_type:                     open_list_with_lijststem_for_
                                 inter_list_count_only
preference_votes_per_voter:      one lijststem OR multiple
                                 preference votes within a single
                                 list
panachage_allowed:               no
cumulation_allowed:              no — each preference mark counts
                                 once

party_lists_allowed:             yes
voter_grouping_lists_allowed:    yes — non-party lists permitted
                                 under signature requirements
voter_grouping_legal_term:       lokale lijst (local list)
citizen_committee_lists_allowed: yes
independents_on_lists_allowed:   yes (single-name lists)

intra_list_rule:                 pure_preference (post-2023
                                 reform)
preference_threshold_pct:        not applicable — every
                                 preference vote counts
intra_list_ties_rule:            lot

compulsory_voting:               no (2021 reform abolished at
                                 municipal level only)
```

### Notes

The 2023 reform produced an architecturally consequential
asymmetry: **the lijststem still exists as a count-bearing
voter mark, but no longer carries any intra-list ordering
weight**. The lijststem retains a pure inter-list role.

For the user's preferred ballot architecture (single-vote
candidate-or-party): the post-2023 Flemish system is the
working operational case for the design choice that says "the
party vote should count for the party total but should not
override what voters say about intra-list order." This is a
distinct drafting position from:

- Brazilian *voto de legenda* (party vote counts for inter-list
  allocation, no intra-list effect, no list flow);
- Dutch single-vote lijsttrekker convention (no formal party
  vote at all);
- Bavarian *Listenkreuz* (list mark causes votes to flow in
  submitter order — the pot system Flanders just abolished).

The Flemish 2023 reform reaches the same intra-list outcome as
Brazil (pure preference within the list) by a different route —
abolition of the pot-system rather than design without one.

---

## 3. Component 3 — Allocation Formula

### Imperiali allocation

Per the *Lokaal en Provinciaal Kiesdecreet*, inter-list seat
allocation at the municipal level uses the **Imperiali
highest-averages method**. The divisor sequence used in Flemish
municipal practice is:

> **1, 1.5, 2, 2.5, 3, 3.5, 4, 4.5, 5, …**

(This is the form documented in Flemish electoral commentary;
the standard mathematical equivalent of dividing by (seats+2)
that appears in other Imperiali implementations is computable
but not the sequence used in the practical computation.)

A list's vote total (lijststem + candidate preference votes) is
divided successively by 1, 1.5, 2, 2.5, … . The seats are
awarded by descending order of the resulting quotients.

### Comparison to D'Hondt

D'Hondt's divisor sequence is 1, 2, 3, 4, … — integer steps.
Imperiali at half-integer steps means each subsequent seat
"costs" the list a smaller increment of votes than under
D'Hondt. **Imperiali therefore produces stronger large-party
bias than D'Hondt at any given magnitude**.

For a numerical illustration: with 100 voters and 5 seats, a
list with 60 votes vs a list with 40 votes:

- Under D'Hondt: 60/1=60, 60/2=30, 60/3=20, 60/4=15, 60/5=12;
  40/1=40, 40/2=20, 40/3=13.3, 40/4=10. Highest five: 60,
  40, 30, 20, 20 — ties handled by the rule. List 1 gets 3
  seats; list 2 gets 2 seats.
- Under Imperiali (Flemish form): 60/1=60, 60/1.5=40,
  60/2=30, 60/2.5=24, 60/3=20; 40/1=40, 40/1.5=26.7,
  40/2=20, 40/2.5=16. Highest five: 60, 40, 40, 30, 26.7. List
  1 gets 3 seats; list 2 gets 2 seats.

At this magnitude and vote split the methods produce the same
result. Imperiali's distinct effect emerges in tighter contests
or at smaller magnitudes; the principal effect is to discourage
small-list survival over multiple cycles.

### No statutory threshold

Flemish municipal allocation has **no statutory percentage
threshold** beyond the structural Imperiali threshold from
magnitude alone. A list that receives any votes can in principle
win seats if its quotient ranks high enough, but in practice
Imperiali's bias means lists below approximately one
Imperiali-quota of votes are excluded.

### Operationalized values

```
allocation_formula:              imperiali_half_integer
formula_codified_as:             procedural — divisor sequence
                                 1, 1.5, 2, 2.5, … specified
formula_statutory_citation:      Lokaal en Provinciaal
                                 Kiesdecreet (relevant articles
                                 to be quoted from the
                                 consolidated text)
ties_rule:                       lot

legal_threshold_pct:             0
threshold_level:                 N/A
threshold_exemption_rules:       N/A

apparentement_allowed:           no (Flanders municipal level;
                                 historically permitted at
                                 provincial level, abolished)
intra_list_rule:                 pure_preference (post-2023
                                 reform)
```

### Notes — why Imperiali at municipal level

Imperiali was historically chosen for Belgian municipal
elections in part because the formula is more favorable to the
formation of stable governing majorities at the local level.
Bel­gian municipalities form executive coalitions
(*schepencolleges*) by negotiation among parties; Imperiali's
bias toward larger parties simplifies coalition arithmetic by
reducing the number of viable coalition partners.

For U.S. drafters: Imperiali is the project's working example
of a deliberately large-party-favoring allocation method. The
trade-off is explicit: Imperiali sacrifices small-party survival
for governance stability. U.S. PR adoption that prioritizes
governance stability (e.g., for executive-formation purposes)
over small-party survival has Imperiali as a precedent. Most
U.S. PR-reform proposals work in the opposite direction —
toward greater proportionality and small-party survival — and
would more naturally adopt Sainte-Laguë (Germany) or a hybrid
quota+highest-averages (Brazil, Netherlands) than Imperiali.

The 2025 NRW VerfGH ruling on the "Rock-Verfahren"
(`cases/germany/nrw_profile.md`) — which struck down a
percentage-remainder method that systematically advantaged
larger parties — raises the question whether Imperiali itself
could survive analogous constitutional scrutiny under U.S.
state-constitutional equal-protection doctrine. The German
holding turned on the **predictability** of the bias; Imperiali
is more predictable in its bias than the Rock-Verfahren was.
A U.S. PR statute adopting Imperiali should anticipate
constitutional challenge under analogous doctrine.

---

## 4. Connected areas (brief)

### A. Voter eligibility

Belgian citizens aged 18+ resident in the municipality, plus
EU citizens for municipal elections (Maastricht Treaty
obligation), plus non-EU foreign nationals after 5 years of
legal residence. Voting is **voluntary** at municipal level
since the 2021 reform; remains compulsory at federal and
regional levels.

### B. Candidate / list registration

Lists are submitted by registered political parties or by
non-party voter groupings. Signature requirements scale with
council size:

- Smaller councils (M < 25): signatures from a small number of
  voters (typically ~50–100).
- Larger councils (M ≥ 25): higher thresholds.

Lokale lijsten (local lists) — non-party local groupings — are
common in Flemish municipal elections. Local-list prominence
varies by region: stronger in West-Flanders, less so in
Antwerp.

### C. Campaign finance

Governed by Flemish regional legislation post-Sixth State
Reform. Public funding for parties does not extend to
non-party local lists at the municipal level — a parallel to
the Dutch lokale-partijen funding asymmetry.

### D. Election administration and local governance

The Flemish Region administers municipal elections through the
*Agentschap Binnenlands Bestuur* (Agency for Domestic
Governance). Each municipality has its own *gemeentelijk
hoofdbureau* (municipal central electoral bureau).

**Mayor selection (post-2024 reform)**: under the 2024 *Lokaal
en Provinciaal Kiesdecreet* amendments, the candidate with the
most preference votes within the largest faction of the
governing coalition automatically becomes mayor — replacing
the prior negotiation-based mayor designation. This is a
notable structural reform tying the mayor's mandate directly
to voter preference rather than to coalition negotiation.

### E. Vote count, certification, dispute resolution

Counting at the polling-station level; aggregated through the
gemeentelijk hoofdbureau. Election challenges to the *Raad voor
Verkiezingsbetwistingen* (Council for Electoral Disputes) — a
specialized administrative body — with appeal to the Council
of State on administrative-law grounds.

### F. Media access

Governed by the Flemish *Mediadecreet*. Public broadcasters
allocate political broadcast time by formula; lokale lijsten
generally receive less time than national-party local
branches (the funding-asymmetry pattern recurring).

### G. (Districting law — captured under Component 1)

---

## 5. PROSeS performance diagnostic

The 13 October 2024 elections were the first under the
post-2023 *Lokaal en Provinciaal Kiesdecreet* reforms (no
lijststem flow + voluntary voting + automatic mayor designation).

### Service Outcomes

**Voter turnout** at the 13 October 2024 Flemish municipal
elections was **~65%** of registered voters — substantially
lower than the ~90% pre-reform compulsory-voting era.

**Equity / minority representation**: Imperiali bias produces
underrepresentation of smaller parties and minority-supported
lists at small magnitudes. The 2023 reform's pure-preference
intra-list rule has been welcomed for giving voters more direct
say within lists, but has not addressed the inter-list bias.

### Stakeholder Satisfaction

The 2024 elections produced significant academic and
political-commentary discussion of:
- The lijststem reform (most observers welcomed it);
- The compulsory-voting abolition (turnout decline raised
  representation-quality concerns);
- The automatic-mayor rule (criticized for reducing coalition
  flexibility but praised for democratic clarity).

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # citizens, EU citizens, and
                                   # 5-year residents
equal_suffrage:        compliant   # subject to Imperiali bias
                                   # critique
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant
fundamental_rights:    compliant
regulatory_stability:  medium      # 2021 (compulsory voting) and
                                   # 2023 (lijststem, mayor)
                                   # reforms produced significant
                                   # mid-cycle change
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

| Provision | Type | Rationale |
|---|---|---|
| Imperiali allocation formula | **Particular** | Reflects Belgian deliberate choice for governance stability; less suitable for U.S. PR reform priorities. |
| Lijststem-counts-for-inter-list-only (post-2023) | **Universal** | Drafting model for the design choice "party vote without intra-list ordering effect." |
| Pure preference intra-list rule | **Universal** | Same drafting move as Bavaria GLKrWG Art. 36(1); portable. |
| Automatic mayor designation by preference vote | **Hybrid** | Substantively portable; depends on the Flemish council-elects-mayor architecture. U.S. analogue would tie mayor selection to popular vote within council elections — politically consequential and constitutionally distinct. |
| Voluntary municipal voting in compulsory-federal context | **Particular** | Belgian-particular; the U.S. has no compulsory-voting baseline to deviate from. |

### Top three takeaways for US state/local implementation

1. **Lijststem-for-count-only is a clean drafting position.**
   The post-2023 Flemish architecture lets the party vote count
   for the inter-list allocation while having zero effect on
   intra-list ordering. This is an analytically useful midpoint
   between Brazil's voto-de-legenda (where the legenda vote
   has no intra-list role at all but the Brazilian system also
   has the voto-nominal as the ONLY intra-list mechanism) and
   pure-preference systems.

2. **Imperiali is the cautionary case** for U.S. PR adoption.
   The Flemish experience documents that strong large-party
   bias is workable in a multi-party governance system with
   stable coalition norms — but the same bias would face
   constitutional challenge under U.S. state-constitutional
   equal-protection doctrine, especially after the 2025 NRW
   VerfGH precedent. Drafters should choose Sainte-Laguë or
   D'Hondt, not Imperiali.

3. **Automatic mayor designation by preference vote** is a
   distinctive 2023 reform worth flagging. The mechanism ties
   the mayoral mandate to the most-preferred candidate within
   the largest coalition faction — combining proportional
   council selection with a preference-vote-derived executive.
   For U.S. council-manager cities considering hybrid
   structures, this is a working precedent.

---

## 8. Sources

### Primary

- ***Lokaal en Provinciaal Kiesdecreet*** van 8 juli 2011, as
  amended through 2023 (BS 25 juli 2011 met latere
  wijzigingen). Codex Vlaanderen URL:
  <https://codex.vlaanderen.be/Portals/Codex/documenten/1020561.html>
- ***Decreet over het Lokaal Bestuur*** (Flemish governance
  act).
- *Belgische Grondwet*, Articles 41 and 162 (municipal
  autonomy and regional competence).

### Reform legislation

- 2021 amendment ending compulsory voting at municipal level.
- 2023 amendment abolishing the pot-system effect on
  intra-list ordering and introducing automatic mayor
  designation.

### Secondary

- *Vlaanderenkiest.be — Hoe verloopt de zetelverdeling?*:
  <https://vlaanderenkiest.be/faq/zetelverdeling>
- VVSG (Flemish Association of Municipalities) — gemeenteraads-
  verkiezingen materials.

### Outstanding gaps

- Verbatim text of the *Lokaal en Provinciaal Kiesdecreet*
  articles on Imperiali allocation and the post-2023
  intra-list rule.
- Verbatim text of the council-size schedule (in the *Decreet
  over het Lokaal Bestuur* or cross-referenced).
- 2024 Flemish election outcome data: turnout by municipality;
  invalid-vote rates; share of seats won by lokale lijsten;
  comparative analysis of intra-list ordering pre- and
  post-2023 reform.
- Cached PDF of the consolidated *Lokaal en Provinciaal
  Kiesdecreet*.
- Comparative analysis of Imperiali vs. D'Hondt outcomes at
  matched magnitudes.
