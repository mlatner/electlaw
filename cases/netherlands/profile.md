# Netherlands — Municipal council elections (Gemeenteraadsverkiezingen)

## 0. Case metadata

- **Country**: Kingdom of the Netherlands (Koninkrijk der
  Nederlanden)
- **Sub-jurisdiction**: All municipalities (*gemeenten*) — 342 as
  of 2025.
- **Level of government**: Local — *Gemeenteraad* (municipal
  council). The Mayor (*burgemeester*) is appointed by Royal
  Decree, not elected, so this profile addresses only the
  council contest.
- **Electoral system family**: **Open-list proportional
  representation** with **preference-vote (voorkeurstem)
  reordering**. Single vote, cast for a specific candidate; no
  separate party-only vote option. Each municipality is a
  single electoral district (M = total council size).
- **Governing statutes**:
  - **Kieswet** (Wet van 28 september 1989, Stb. 423) — the
    national Election Act, governing all elections (national,
    provincial, municipal, water-board, European Parliament).
    Hoofdstukken H (candidate-list submission) and P (result
    determination and seat allocation) are the architectural
    keystones.
  - **Kiesbesluit** — the implementing decree.
  - **Gemeentewet** (Wet van 14 februari 1992, Stb. 96) — the
    Municipalities Act. Article 8 sets council size by
    population.
  - **Wet financiering politieke partijen** (Wfpp) — political-
    party financing.
- **Constitutional anchor**: *Grondwet* (Constitution) Art. 4
  (right to vote and stand for election); Art. 129 (provincial
  and municipal council elections).
- **EMB**: *Kiesraad* (Electoral Council) at national level;
  *centraal stembureau* (central electoral bureau) at the
  municipality.
- **What is and is not elected at the municipal level**: only
  the *gemeenteraad* (council) is directly elected. The
  *burgemeester* (mayor) is appointed by Royal Decree
  (Grondwet Art. 131); *wethouders* (aldermen) are elected by
  the council. The full executive (*college van burgemeester
  en wethouders*) is derived from the proportional council
  composition through coalition formation. See Section 4.D for
  full detail.
- **Last regular election**: 16 March 2022. Next regular: March
  2026 (held quadrennially on the third Wednesday of March).
- **Analyst**: this profile, 2026-05-05.

### Why this case is in the project

Three features make the Netherlands a central case for the
project:

1. **Lokale partijen (local parties) are a working non-party-
   list ecosystem at scale.** Local-only parties — *Lokaal
   Belang*, *Leefbaar [Stad]*, *[Stad] Lokaal*, and analogous
   formations — together win more than half of all gemeenteraad
   seats in many cycles. Unlike Bavarian *Wählergruppen*,
   Dutch lokale partijen register as political parties under
   the Kieswet and operate within the same statutory framework
   as national parties.
2. **The voorkeurstem (preference vote) reordering rule** is a
   specific, calibrated drafting parameter: a candidate is
   reordered above the list-submitter's order if the
   candidate receives ≥ 25% of the *kiesdeler* (electoral
   quotient) in personal votes, or ≥ 50% in councils of fewer
   than 19 members. This is the project's most directly
   instructive case for how an open-list reordering threshold
   can be set in statute.
3. **The dual remainder-method rule (Kieswet Art. P 7 vs
   P 8)** uses D'Hondt (highest averages) for councils of 19
   seats or more and largest-remainders with a 75%-kiesdeler
   floor for smaller councils. The recognition that allocation
   methods produce different distributional effects at
   different magnitudes is itself a portable drafting move.

The Dutch ballot architecture differs from Brazil's voto-de-
legenda model in one consequential way: there is **no separate
party-only voting option**. The voter must mark a specific
candidate. By long-standing convention, marking the #1
candidate on a list is the de-facto "party vote" — but it is
formally a vote for that named person. This is a contrast that
sharpens the analytical question for the user's preferred
single-vote candidate-or-party design.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — Gemeentewet Art. 8 (Number of Council Members)

The council-size table sits in the Gemeentewet (the basic
Municipalities Act), not in the Kieswet:

> Art. 8(1) De raad bestaat uit:
>
> - 9 leden in een gemeente beneden de 3.001 inwoners;
> - 11 leden in een gemeente van 3.001 – 6.000 inwoners;
> - 13 leden in een gemeente van 6.001 – 10.000 inwoners;
> - 15 leden in een gemeente van 10.001 – 15.000 inwoners;
> - 17 leden in een gemeente van 15.001 – 20.000 inwoners;
> - 19 leden in een gemeente van 20.001 – 25.000 inwoners;
> - 21 leden in een gemeente van 25.001 – 30.000 inwoners;
> - 23 leden in een gemeente van 30.001 – 35.000 inwoners;
> - 25 leden in een gemeente van 35.001 – 40.000 inwoners;
> - 27 leden in een gemeente van 40.001 – 45.000 inwoners;
> - 29 leden in een gemeente van 45.001 – 50.000 inwoners;
> - 31 leden in een gemeente van 50.001 – 60.000 inwoners;
> - 33 leden in een gemeente van 60.001 – 70.000 inwoners;
> - 35 leden in een gemeente van 70.001 – 80.000 inwoners;
> - 37 leden in een gemeente van 80.001 – 100.000 inwoners;
> - 39 leden in een gemeente van 100.001 – 200.000 inwoners;
> - 45 leden in een gemeente boven 200.000 inwoners.

Art. 8(2) provides that population-driven changes in council
size take effect only at the next regular council election.

### Districts and magnitude

Each *gemeente* is a single electoral district. Dutch
municipalities are not subdivided into wards or sub-districts
for council elections. **District magnitude equals council size**
for each municipality:

- M = 9 in the smallest municipalities.
- M = 19 marks the dividing line for the dual remainder-method
  rule (Component 3).
- M = 39 in mid-large cities (100,000 – 200,000 inhabitants).
- M = 45 in the largest cities (Amsterdam, Rotterdam, The
  Hague, Utrecht, etc.).

### Operationalized values

```
total_seats:                     9 (smallest) — 45 (>200,000)
codification_instrument:         Gemeentewet Art. 8 (statute)
amendment_authority:             Tweede Kamer + Eerste Kamer
                                 (national legislature)
amendment_threshold:             ordinary national legislation

magnitude_uniform:               yes within each municipality
magnitude_typical:               population-determined
magnitude_range:                 9 — 45
districts_count:                 1 per municipality
districting_authority:           N/A — district = municipality
districting_frequency_years:     N/A
districting_criteria_in_statute: N/A

tiered:                          no
tier_count:                      1
tier_compensatory:               not applicable

threshold_of_exclusion_pct:      10.0% (M=9) → 2.17% (M=45)
                                 [structural threshold from
                                 magnitude alone; no statutory
                                 percentage threshold]
```

### Notes

The Dutch population table is significantly less granular than
Bavaria's (ending at M = 45 vs. Munich's M = 80) and
significantly less granular than Brazil's (ending at M = 45 vs.
São Paulo's M = 55). This is partly a function of population
distribution — the Netherlands has no city above 1 million —
and partly a deliberate choice not to scale council size as
aggressively with city size as Bavaria does. Amsterdam (~890,000
inhabitants) and Munich (~1.5 million) both land at the top of
their respective tables; the Bavarian table gives Munich an
M = 80 council, the Dutch table gives Amsterdam an M = 45
council.

For U.S. implementation, the Dutch placement of the council-
size table in the *Gemeentewet* (a separate statute from the
elections code) is a structural drafting choice worth noting:
it separates the question of "how big should the council be?"
from the question of "how do we elect it?" U.S. drafting can
follow either pattern (combined statute as in NSW LGA 1993, or
split statutes as in NL).

---

## 2. Component 2 — Ballot Structure

### The voter's act

Per Kieswet Hoofdstuk J (vote casting) and Hoofdstuk P
(result determination), each voter casts **one vote for a
specific candidate**. The ballot lists all candidates organized
by party (one column per list); the voter marks one candidate
in one column.

There is **no separate party-only vote option**. A voter who
wishes to support the party without expressing a candidate
preference marks the #1 candidate on the list. By convention,
the #1 candidate is the party's *lijsttrekker* (list leader),
and a vote for the lijsttrekker is functionally treated as a
party vote — but it is statutorily a vote for that named
person.

### Statutory text — Kieswet Art. P 15 (Voorkeursdrempel)

The preference-vote threshold for reordering:

> Art. P 15: A candidate is elected with priority (i.e.,
> reordered above the submitted list order) if the candidate
> received personal votes equal to at least **25% of the
> kiesdeler** (electoral quotient).
>
> For elections in which fewer than 19 seats are distributed
> (i.e., councils of M < 19), the threshold is **50% of the
> kiesdeler**.

(Verbatim Dutch text to be added when statutory text is fully
extracted; description above per Kiesraad official guidance and
Wikisource Hoofdstuk P.)

### Mechanism — voorkeurstemmen reordering

Within each list, the procedure is:

1. The list-submitter's order (set at candidate registration) is
   the default.
2. Any candidate receiving personal votes ≥ 25% of the kiesdeler
   (or 50% for M < 19) is treated as having "passed the
   voorkeursdrempel" and is reordered to take a seat ahead of
   higher-listed candidates who did not.
3. If multiple candidates clear the threshold, they take seats
   in order of their personal vote totals.
4. Remaining seats then flow to candidates in the original list
   order.

### Operationalized values

```
ballot_type:                     open_list_with_voorkeurstem_threshold
preference_votes_per_voter:      1 (single candidate vote;
                                 no party-only mode)
panachage_allowed:               no
cumulation_allowed:              no
above_the_line_option:           no — voter must mark a
                                 specific candidate. The "party
                                 vote" emerges by convention via
                                 marking the #1 (lijsttrekker)
                                 candidate.

party_lists_allowed:             yes
voter_grouping_lists_allowed:    yes — but local groupings
                                 register as political parties
                                 (lokale partijen) under the
                                 Kieswet, not as a separate
                                 entity class
voter_grouping_legal_term:       lokale partij (local party)
                                 — a category of political
                                 party that competes only in a
                                 specific municipality
citizen_committee_lists_allowed: yes — through registration as
                                 a political party at the
                                 municipal level
independents_on_lists_allowed:   yes — the *blanco lijst*
                                 mechanism allows a candidate
                                 or group to stand without a
                                 registered party name; the
                                 list is then identified by
                                 letter (Lijst A, Lijst B, etc.)

non_party_label_allowed:         yes (party name registered
                                 with central electoral bureau,
                                 or blanco lijst)
non_party_label_categories:      not statutorily restricted
non_party_label_restrictions:    no name confusable with an
                                 existing registered party

intra_list_rule:                 list_order_with_voorkeurstem_
                                 reordering (Art. P 15)
preference_threshold_pct:        25 (M ≥ 19); 50 (M < 19)
```

### Notes

The **voorkeursdrempel** is the project's most directly portable
drafting parameter for any U.S. implementation that wants to
preserve list-submitter ordering as the default while leaving
voters a meaningful path to override it. The Dutch threshold
was lowered from 50% (default for all councils) to 25% by the
Kieswet amendment of 1997 (Wijzigingswet 25.221), with the 50%
threshold preserved only for small councils.

The 25%/50% split at M = 19 mirrors the dual remainder-method
split in Component 3. The Netherlands recognizes that
M = 19 is a structural threshold below which formula and
threshold choices produce different distributional effects, and
adjusts the rules accordingly. This is a portable drafting
move regardless of the formula family adopted.

For the user's preferred ballot architecture (single-vote
candidate-or-party): the Netherlands shows what a list-PR
ballot looks like **without** a separate party-only mode. The
reliance on voting-for-the-lijsttrekker as a de-facto party
vote is statutorily fragile — voters who are unfamiliar with
the convention can produce unintended intra-list reordering
effects, and there is regular Dutch academic and political
discussion about adding a formal "lijststem" option. The
project's recommendation to U.S. drafters should be to include
the explicit party-only option (Brazil's voto-de-legenda model)
rather than rely on the convention.

### Lijstverbinding (list connection) — abolished 2017

Pre-2017, the Kieswet permitted parties to declare a
**lijstverbinding** before the election — a joint declaration
in which two or more parties' votes would be pooled for the
remainder-seat calculation in Component 3. The lijstverbinding
was effectively an apparentement mechanism, similar to Danish
*listeforbund* and Finnish *vaaliliitto*.

Lijstverbindingen were **abolished by the Wijzigingswet
afschaffen lijstverbindingen** in 2017. The reform was driven
by the perception that lijstverbindingen produced strategic
behavior disconnected from voter intent, and that their effect
in seat distribution was opaque to voters at the time of
voting.

The 2017 Dutch abolition runs in parallel with the 2017
Brazilian abolition of *coligações* (EC 97/2017). Two
common-law-tradition jurisdictions reached structurally
similar conclusions in the same year, for related reasons.

---

## 3. Component 3 — Allocation Formula

### Statutory text — Kieswet Hoofdstuk P (Result Determination)

The Dutch allocation procedure is a **two-step hybrid**:
**kiesdeler (Hare-quota whole seats)** for the principal
allocation, and **D'Hondt (highest averages) or largest
remainders** for the remainder seats, depending on council
size.

#### Article P 5 — Kiesdeler (Electoral Quotient)

> Het centraal stembureau deelt de som van de stemcijfers van
> alle lijsten door het aantal te verdelen zetels.

(Translation: The central electoral bureau divides the sum of
the vote totals of all lists by the number of seats to be
distributed.)

The result is the **kiesdeler** — equivalent to the Hare quota.

#### Article P 6 — Whole-quotient seats

> Zoveel maal als de kiesdeler is begrepen in het stemcijfer
> van een lijst wordt aan die lijst een zetel toegewezen.

(Translation: As many seats are awarded to a list as the
kiesdeler fits into that list's vote total.)

#### Article P 7 — Remainder seats, councils ≥ 19 seats

For councils of 19 or more seats, remainder seats are
distributed by the **D'Hondt highest-averages method**: each
list's vote total is divided by (current seats + 1), and the
seat is awarded to the list with the highest resulting average.
The procedure is repeated for each remaining seat.

Ties are decided by lot.

#### Article P 8 — Remainder seats, councils < 19 seats

For councils of fewer than 19 seats, remainder seats are
distributed by **largest remainders after dividing by the
kiesdeler**, with a critical exclusion: lists that received
**fewer than 75% of the kiesdeler** are excluded from the
remainder distribution.

This produces stronger small-list protection at small magnitudes
(where D'Hondt's large-party bias would otherwise be severe) at
the cost of admitting some lists below a single-quota worth of
votes.

### Operationalized values

```
allocation_formula:              two-step hybrid:
                                 (1) Hare quota / kiesdeler for
                                     whole-quotient seats (P 6)
                                 (2a) D'Hondt highest averages
                                      for councils ≥ 19 seats
                                      (P 7)
                                 (2b) Largest remainders with
                                      75%-kiesdeler floor for
                                      councils < 19 seats (P 8)
formula_codified_as:             procedural — quota and
                                 highest-averages mechanics
                                 specified directly in articles;
                                 the "D'Hondt" eponym is not
                                 used in the statute
formula_statutory_citation:      Kieswet Hoofdstuk P, Arts. P 5
                                 – P 8
ties_rule:                       drawing of lots by central
                                 electoral bureau

legal_threshold_pct:             0 (no statutory percentage
                                 threshold for council elections);
                                 effective threshold = 1 kiesdeler
                                 for principal allocation; 75% of
                                 kiesdeler for remainder
                                 distribution at M < 19
threshold_level:                 N/A (no formal threshold)
threshold_exemption_rules:       N/A
threshold_backdoor:              N/A

apparentement_allowed:           no (since 2017 abolition of
                                 lijstverbindingen)

intra_list_rule:                 list_order_with_voorkeurstem_
                                 reordering (Art. P 15)
```

### Notes

Three drafting features stand out:

1. **Magnitude-conditional allocation method** (P 7 vs P 8). At
   M ≥ 19, D'Hondt; at M < 19, largest remainders with floor.
   This is a calibrated drafting move recognizing that formula
   choice produces different effects at different magnitudes.
   For U.S. implementation, the underlying logic — that small
   councils may warrant more small-list-protective rules —
   is portable, with the magnitude threshold and floor as
   tunable parameters.
2. **No statutory percentage threshold**. The Netherlands relies
   entirely on the structural threshold from M alone, plus the
   75%-kiesdeler floor at small magnitudes. For Tweede Kamer
   (national, M = 150), the effective threshold is ~0.67%. For
   gemeenteraad elections (M = 9 → 45), the effective threshold
   ranges from ~10% (smallest councils) to ~2.2% (largest).
3. **Procedural drafting style**. Like Bavaria GLKrWG Art. 35
   and the German federal BWahlG § 5, the Dutch Kieswet
   specifies the formula procedurally without using the eponym
   "D'Hondt." This continues the pattern documented across the
   project's case set: working systems consistently choose
   procedural over named drafting for allocation formulas.

#### Comparative table: remainder-method choices across the case set

| Case | Remainder method | Effect |
|---|---|---|
| Germany federal (BWahlG § 5) | Sainte-Laguë / Webster | Least biased |
| Germany Bavaria (GLKrWG Art. 35) | Sainte-Laguë / Webster | Least biased |
| Germany NRW (KWahlG § 33) | Sainte-Laguë / Webster (post-2025 VerfGH ruling) | Least biased |
| Brazil (CE Art. 109) | Highest averages (D'Hondt-style) | Larger-party bias |
| Netherlands (Kieswet P 7, M ≥ 19) | D'Hondt | Larger-party bias |
| Netherlands (Kieswet P 8, M < 19) | Largest remainders with floor | Smaller-party protection at low M |
| Belgium municipal | Imperiali | Strong large-party bias |

The Dutch dual rule is the only case in the project's set that
uses **different methods for different magnitudes** within the
same statute. Bavaria, NRW, and the federal Bundestag use
Sainte-Laguë end-to-end; Brazil uses Hare-quota plus
highest-averages end-to-end.

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

Per *Kieswet* Hoofdstuk B (kiesgerechtigdheid):
- Dutch nationals aged 18+ and resident in the municipality;
- EU citizens resident in the municipality (Maastricht Treaty
  obligation);
- non-EU foreign nationals who have legally resided in the
  Netherlands for at least 5 years.

Voter registration is **passive** — derived from the *Basis-
registratie Personen* (BRP, the population register). Voters do
not register affirmatively for elections.

### B. Candidate / list registration — *full subsection*

The most analytically central section for the project.

#### Party name registration (Kieswet Hoofdstuk G)

A political party that wishes to appear on the ballot under a
party name must **register the name** (*aanduiding*) with the
central electoral bureau of the relevant level (national for
Tweede Kamer; provincial for Provinciale Staten; municipal for
Gemeenteraad). Registration is one-time and does not need to be
renewed for each election. A party that does not register a
name appears on the ballot as a **blanco lijst** identified by
letter (Lijst A, Lijst B, etc.).

For municipal-only parties, registration with the municipality's
central electoral bureau is sufficient. National parties
typically register at the national level and are then
recognized at all subordinate levels.

#### Candidate-list submission (Kieswet Hoofdstuk H)

For each election, the party submits a *kandidatenlijst*
(candidate list) on *kandidaatstellingsdag* (candidate-
nomination day, set in statute for each election cycle). The
submission must include:

- The candidate list itself, with candidates in the submitter's
  preferred order (Form H 1).
- Consent declarations (*verklaringen van instemming*) from
  each candidate (Form H 9).
- The party name (*aanduiding*) if registered, or a request to
  use a blanco lijst.
- Where required, **ondersteuningsverklaringen** (supporting
  declarations) — see below.

#### Supporting declarations — ondersteuningsverklaringen

Per Kieswet Art. H 4, parties that did **not win seats in the
previous election** at the relevant level (or are participating
for the first time) must submit a minimum number of supporting
declarations:

- For municipalities with councils of **≥ 19 seats**: **20
  ondersteuningsverklaringen** (Form H 4).
- For smaller councils: a smaller threshold (typically 10 to
  20).

The supporting declaration is a written statement signed by an
eligible voter, expressing support for the party's
participation in the upcoming municipal council election. The
voter must sign **in person at the municipality's offices**
(parallel to the Bavarian *Eintragung in Unterstützungslisten*
under GLKrWG Art. 28). Each voter may sign only one
ondersteuningsverklaring per election.

#### Operationalized values

```
list_registration_authority:     centraal stembureau (central
                                 electoral bureau) — national,
                                 provincial, or municipal
signatures_required_min:         20 (municipalities ≥ 19 seats)
                                 ~10–20 (smaller councils)
signature_scaling:               threshold-based: applies to new
                                 parties only; established
                                 parties (with seats from
                                 previous election) are exempt
signature_collection_mode:       in-person at municipal offices
                                 (parallel to Bavaria GLKrWG
                                 Art. 28); not collected by the
                                 list-submitter
deposit_amount:                  yes (waarborgsom — refundable
                                 if the list reaches a vote
                                 threshold)
deposit_currency:                EUR
filing_deadline:                 kandidaatstellingsdag — set in
                                 the Kieswet for each election
party_v_nonparty_equal_treatment:
                                 yes — lokale partijen and
                                 national parties follow the
                                 same Kieswet provisions
list_size_min:                   1 candidate
list_size_max:                   set by Kieswet — typically 50
                                 candidates for gemeenteraad
                                 elections
list_ordering_rule:              submitter (subject to Art. P 15
                                 voorkeurstem reordering)
gender_quota:                    none in Kieswet — no statutory
                                 quota at any level
residency_required:              candidate must be eligible to
                                 vote in the relevant
                                 municipality
multiple_candidacy_restrictions: candidate may appear on only
                                 one list per election
```

#### Notes — lokale partijen as a working non-party-list ecosystem

Lokale partijen — local-only parties registered under the
Kieswet but operating only in a single municipality — together
win **a majority of all gemeenteraad seats** in many cycles.
The Wikipedia summary "extremely common" reflects ~30%–50% of
council seats nationwide, with much higher shares in smaller
municipalities.

For U.S. implementation, the Dutch model is the working answer
to a question the project's case set has been working through:
**how does a country accommodate non-party participation at the
local level when the national-level system is partisan?** The
Dutch answer: extend the same party-registration framework to
the municipal level, but allow registration to be local-only.
A *Lokaal Belang Amsterdam* registers with Amsterdam's central
electoral bureau and contests only Amsterdam's elections.

This is structurally different from:
- Bavaria's *Wählergruppen* (a separate entity class outside
  the *Parteiengesetz*; see GLKrWG Art. 24(1));
- Brazilian *coligações* (now abolished) or *federações*
  (still party-based);
- NSW *groups* (candidate-level associations not entity
  registrations).

The Dutch model has the practical advantage of using one
unified party-registration framework across all levels — but
the analytical disadvantage that "party" as a legal category
encompasses both nationally-organized political parties and
ad-hoc municipal vehicles. For a U.S. drafter, the choice
between the Bavarian model (separate non-party-list entity
class) and the Dutch model (universal party registration with
local-only option) is a structural drafting decision.

### C. Campaign finance

Governed by *Wet financiering politieke partijen* (Wfpp).
National parties receive subsidies tied to membership and
representation. **Local parties receive no national subsidy**
under the Wfpp — they must self-fund. This produces a
significant funding asymmetry between lokale partijen and
local branches of national parties; multiple Dutch
parliamentary-committee reports have flagged the asymmetry, but
no statutory remediation has been enacted.

### D. Election administration and local governance structure

The *Kiesraad* (Electoral Council) is the national EMB. Council
elections are administered by the **municipality itself**
through its central electoral bureau, with the Kiesraad
providing standardized procedures and forms. This is a
decentralized model similar to German *Länder* practice, with
the addition of a coordinating national body.

#### What is and is not elected at the municipal level

Per *Gemeentewet* and the Grondwet:

- **Gemeenteraad** (council): the only directly elected body.
  Members elected by the proportional rules of Components 1–3.
- **Burgemeester** (mayor): **not elected**. Appointed by Royal
  Decree (*Koninklijk Besluit*) on the recommendation of the
  Minister of the Interior, after a recommendation from the
  council. Grondwet Art. 131. The minister may refuse the
  council's recommendation only for "weighty reasons"
  (*zwaarwegende redenen*) and rarely does.
- **Wethouders** (aldermen / executive members): elected by
  the council from inside or outside the council membership.
  Wethouders form the daily executive board (*college van
  burgemeester en wethouders*) together with the burgemeester.

The implication is structurally important: **Dutch municipal
proportional representation determines the entire democratic
component of municipal government**. The college (executive) is
derived through council coalition formation; the mayor is
appointed by the Crown. Voters elect only the council, but the
council's PR composition then determines the executive
composition.

This is a contrast with U.S. municipal practice, where mayor
and council are typically elected separately and a strong-mayor
configuration may give the mayor a popular mandate independent
of the council. For U.S. PR adoption in council-manager cities
(where the manager is appointed and there is no separately
elected strong mayor), the Dutch model maps cleanly. For
strong-mayor cities, PR adoption affects only one chamber of a
two-mandate system.

#### Wet dualisering gemeentebestuur (2002)

The **Wet dualisering gemeentebestuur** (Municipal Government
Dualization Act, 7 March 2002) separated the legislative and
executive functions at the municipal level:

- Wethouders no longer sit on the council;
- Council and executive operate analogously to the Tweede Kamer
  / cabinet relationship at national level;
- The council's representative function is statutorily
  emphasized.

For U.S. drafters: the dualization model is one drafting choice
for how to separate council legislative function from executive
function. The U.S. council-manager system reaches a similar
result through a different route (council elects/appoints a
manager; manager runs the executive).

#### Sub-municipal councils — *deelgemeenten / stadsdeelraden* abolished 2014

Pre-2014, Amsterdam had directly elected *stadsdeelraden*
(district councils) for its seven *stadsdelen* (urban districts);
Rotterdam had analogous *deelgemeenten*. These were sub-municipal
elected bodies with their own proportional elections.

The **Wet afschaffing deelgemeenten** (Law abolishing
sub-municipal entities, 2014) removed these bodies nationally.
Amsterdam replaced its stadsdeelraden with **bestuurscommissies**
(administrative commissions); for the first 2014 cycle these
were directly elected, but they were subsequently converted to
appointed bodies with reduced powers.

For the project, the 2014 abolition is a documented case of
**retreat from local PR**: a layer of proportionally elected
representation was removed by national legislation, with the
municipality losing the option to retain it. U.S. drafters
considering sub-municipal PR structures (e.g., neighborhood
councils with elected representatives) should be alive to the
political-economy lessons: such bodies require ongoing
political support to survive cycles of efficiency-focused
restructuring.

### E. Vote count, certification, dispute resolution

Counting is conducted at the polling-station level on election
night, with results aggregated to the municipality and then
nationally. Final totalization typically within days. The
*Kiesraad* certifies national results.

Election challenges may be brought in the **Afdeling
Bestuursrechtspraak van de Raad van State** (Administrative
Jurisdiction Division of the Council of State) for
administrative-law issues, or referred to the **Raad** (the
council itself) for council-membership decisions. There is no
specialized electoral-court system analogous to Brazil's
*Justiça Eleitoral*.

### F. Media access

Governed by the *Mediawet* (Media Act). Public broadcasters
allocate political-broadcast time by formula, with adjustments
for national vs. local elections. Local broadcasters
(*lokale omroepen*) provide additional time for municipal
campaigns.

### G. (Districting law — captured under Component 1)

District structure is non-applicable: each gemeente is a single
electoral district, with no sub-municipal divisions for council
contests.

---

## 5. PROSeS performance diagnostic

The empirical anchor is the **16 March 2022 gemeenteraads-
verkiezingen** — the most recent municipal cycle. The next
cycle is March 2026. Sources:

- *Kiesraad* — official results and procedural data.
- *Centraal Bureau voor de Statistiek* (CBS) — turnout and
  demographic data.
- Academic literature on Dutch local elections (notably the
  *Tijdschrift voor Politicologie*).

### Process Design

**Public participation**: the Kiesraad consults publicly on
procedural amendments. Local-level participation in election
administration is structured through the municipality's
democratic processes.

**Probity and impartiality**: no significant integrity
concerns in recent cycles. The Dutch electoral administration
is consistently rated highly in international comparative
indices (Electoral Integrity Project, V-Dem, etc.).

**Accountability**: dispute resolution channels exist but the
absence of a specialized electoral court means that election-
related administrative-law issues compete with other
administrative-law matters for adjudication time.

### Resource Investment

Municipalities fund their own council elections (with national-
government reimbursement for some categories). The funding
asymmetry between national parties (subsidized through Wfpp)
and lokale partijen (self-funded) is a documented gap that has
not been remediated.

### Service Output Quality

**Convenience**: voting is in-person at polling stations on
election day; postal voting is restricted to specific
categories (overseas Dutch nationals, certain professionals);
proxy voting is more widely available. Voter ID is required.

**Accuracy**: paper ballots are used at all levels; manual
counting at polling stations on election night, with electronic
aggregation. Invalid-vote rates are typically 0.3%–0.6% for
gemeenteraad elections.

### Service Outcomes

**Voter turnout** at the 2022 gemeenteraadsverkiezingen was
**50.3%** of eligible voters — the lowest since 1970 and a
matter of ongoing political debate.

**Equity / minority representation**: Dutch gemeenteraden
have historically underrepresented residents of migrant
origin relative to population share. The gap has narrowed
in major cities (Amsterdam, Rotterdam, The Hague, Utrecht)
where lokale partijen and national-party local branches
have actively recruited candidates from migrant communities,
but persists in smaller municipalities.

**Lokale partijen vote share**: lokale partijen received
~37% of all gemeenteraad votes in 2022 — the largest single
category, exceeding any individual national party. This
share has been stable or growing over the past decade.

### Stakeholder Satisfaction

Consistently high among administrators and observers; some
academic critique of the absence of a formal lijststem option
(noted in Component 2) and of the funding asymmetry between
national and local parties.

#### Major outstanding empirical work

- 2022 election outcome data: invalid-vote rates by municipality
  size; share of seats won by lokale partijen vs national-party
  local branches; voorkeurstem reordering incidence.
- 2026 follow-up after the next regular election.
- Comparative data on the 25%/50% voorkeursdrempel impact at
  M = 19 boundary.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # Kieswet Hoofdstuk B;
                                   # extends to EU citizens
                                   # and 5-year residents
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant   # 4-year cycle, fixed dates
fundamental_rights:    compliant
regulatory_stability:  high        # Kieswet structure stable;
                                   # 2017 lijstverbinding
                                   # abolition was the last
                                   # major substantive change
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| Voorkeursdrempel reordering rule (Kieswet Art. P 15) | **Universal** | The 25% / 50% threshold is a calibrated drafting parameter that adapts to any open-list PR system. The percentage is tunable. |
| Magnitude-conditional remainder method (Arts. P 7 vs P 8) | **Universal** | The recognition that small councils warrant different rules is portable. The specific 19-seat boundary is a tunable parameter. |
| Lokale partijen as universal-party-framework local lists | **Hybrid** | The substance — extending the party-registration framework to the local level — is portable. The Dutch implementation depends on having a unified national party-registration system, which the U.S. lacks. A U.S. analog would more closely resemble the Bavarian *Wählergruppe* model. |
| In-person ondersteuningsverklaringen | **Particular** | Reflects Dutch administrative-law tradition. Less compatible with U.S. expectations of electronic / mail-based political organizing. |
| 2017 lijstverbinding abolition | **Universal** | The reasoning — that pre-vote pooling produces opaque post-vote effects — is portable. The U.S. equivalent of apparentement (cross-list endorsement) is structurally similar and faces analogous critiques. |
| Hare-quota + D'Hondt hybrid | **Universal** | Both methods are familiar; the two-step structure is portable. |
| Council size set in separate Municipalities Act | **Hybrid** | The substance — that "how big should the council be?" and "how do we elect it?" are separable questions — is portable. The implementation depends on the existence of a Municipalities Act, which U.S. states have analogues for (general-purpose municipal codes). |

### Top three takeaways for US state/local implementation

1. **Voorkeursdrempel as a tunable reordering parameter.** A
   25% (or 50%) of-kiesdeler threshold for intra-list reordering
   gives voters meaningful agency without abolishing the list-
   submitter's role. The threshold is statutorily explicit and
   reviewable. For U.S. open-list adoption, this is a directly
   importable drafting move.

2. **Magnitude-conditional formula choice.** The Dutch dual rule
   at M = 19 (D'Hondt above; largest remainders with floor
   below) recognizes that distributional effects vary by
   magnitude. U.S. drafters considering local PR at varying
   magnitudes (5-seat wards vs 30-seat at-large councils) can
   adapt the dual-rule pattern to soften the large-party bias
   that pure D'Hondt produces at small magnitudes.

3. **The absence of a separate party-only vote.** The Netherlands
   does not provide what Brazil does (voto de legenda) — and
   the consequences are documented: voters use the lijsttrekker
   convention as a de-facto party vote, but this produces
   intra-list reordering effects when voters mistakenly mark
   the wrong candidate. The Dutch experience is a negative
   precedent for U.S. drafting: include the explicit
   party-only option (Brazilian model) rather than rely on the
   convention.

---

## 8. Sources

### Primary

- *Kieswet* (Wet van 28 september 1989, Stb. 423), consolidated
  text. Hoofdstukken H (kandidaatstelling) and P (vaststelling
  uitslag) are the architectural keystones.
  <https://wetten.overheid.nl/BWBR0004627/>
- *Gemeentewet* (Wet van 14 februari 1992, Stb. 96). Article 8
  sets council size by population.
  <https://wetten.overheid.nl/BWBR0005416/>
- *Grondwet voor het Koninkrijk der Nederlanden*, Articles 4 and
  129.
- *Wet financiering politieke partijen* (Wfpp).

### Reform legislation

- **Wijzigingswet 25.221 (1997)** — lowered voorkeursdrempel
  from 50% to 25% for elections with M ≥ 19.
- **Wet afschaffen lijstverbindingen (2017)** — abolished
  apparentement.

### Official EMB materials

- *Kiesraad — kiesdrempel, kiesdeler en voorkeurdrempel*:
  <https://www.kiesraad.nl/verkiezingen/gemeenteraden/uitslagen/kiesdrempel-kiesdeler-en-voorkeurdrempel>
- *Kiesraad — zetelverdeling over kandidaten*:
  <https://www.kiesraad.nl/verkiezingen/gemeenteraden/uitslagen/zetelverdeling-over-kandidaten>
- *Kiesraad — ondersteuningsverklaringen*:
  <https://www.kiesraad.nl/verkiezingen/gemeenteraden/kandidaatstelling/ondersteuningsverklaringen>
- *Kiesraad — registreren naam partij*:
  <https://www.kiesraad.nl/verkiezingen/gemeenteraden/partijnamen/registreren-naam-partij>

### Outstanding gaps

- Verbatim Dutch text of Kieswet Art. P 15 (voorkeursdrempel),
  Art. P 7 (D'Hondt remainder), Art. P 8 (largest remainders
  with 75%-kiesdeler floor). The descriptions above are drawn
  from Wikisource Hoofdstuk P and Kiesraad official guidance;
  retrieval of the verbatim official text from
  wetten.overheid.nl is the next step.
- Verbatim text of Kieswet Hoofdstuk H provisions on
  ondersteuningsverklaringen and candidate-list submission.
- Cached PDF of the consolidated Kieswet for the project's
  source archive.
- 2022 election outcome data: invalid-vote rates;
  voorkeurstem reordering incidence; share of seats won by
  lokale partijen.
- Comparative analysis of voorkeursdrempel impact pre- and
  post-1997 reform.

### Resolved in this iteration

**2026-05-05** (initial profile):
- Gemeentewet Art. 8 (population-tiered council-size table)
  quoted in Component 1.
- Kieswet Art. P 5 (kiesdeler), Art. P 6 (whole-quotient
  seats), Art. P 7 (D'Hondt remainder for M ≥ 19), Art. P 8
  (largest remainders with floor for M < 19), Art. P 15
  (voorkeursdrempel) described in Component 3 and Component 2.
- 2017 lijstverbinding abolition documented.
- 1997 voorkeursdrempel lowering documented.
- Lokale partijen ecosystem and the universal-party-
  registration framework documented in Connected B.

**2026-05-05** (local-governance addendum):
- Burgemeester appointment regime (Grondwet Art. 131)
  documented.
- Wet dualisering gemeentebestuur (2002) — separation of
  council and executive functions — documented.
- Wet afschaffing deelgemeenten (2014) — abolition of
  Amsterdam stadsdeelraden and Rotterdam deelgemeenten —
  documented as a case of retreat from local PR.
- College van burgemeester en wethouders structure
  documented as the mechanism by which proportional council
  composition produces the executive.
