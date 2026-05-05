# Belgium — Federal level (Chamber of Representatives)

## 0. Case metadata

- **Country**: Kingdom of Belgium (Royaume de Belgique /
  Koninkrijk België)
- **Sub-jurisdiction**: Federal level
- **Level of government**: National (Chamber of Representatives,
  the lower chamber of the Federal Parliament)
- **Electoral system family**: **List PR** in 11 multi-member
  districts. **D'Hondt** allocation. **5% threshold per
  district**.
- **Governing statutes**:
  - **Code Électoral / Kieswetboek** (Loi du 12 avril 1894 —
    Algemene Kieswet, consolidated text). The federal electoral
    code, governing parliamentary elections.
  - **Constitution belge / Belgische Grondwet**, Articles 61–63
    (Chamber of Representatives composition and franchise).
- **Constitutional anchor**: Constitution Art. 63 fixes the
  Chamber size at 150 members.
- **Last regular election**: **9 June 2024** (held jointly with
  European Parliament and Regional elections; first under post-
  2012 BHV reform's mature operation).
- **Compulsory voting**: yes — at federal level, since 1893
  (Constitution Art. 62); fines imposed for non-voting (rarely
  enforced in practice).
- **Analyst**: this profile, 2026-05-05.

### Why this case is in the project

Belgium federal is a working comparator for U.S. drafters
considering state-legislature-level PR adoption with district-
based allocation. Three features:

1. **D'Hondt + 5% per-district threshold** is the canonical
   continental-European federal-PR architecture. Belgium has
   operated this combination through eight federal cycles since
   the 2002 threshold introduction.
2. **11 multi-member districts** with magnitudes ranging from 4
   (German-speaking enclave) to 24 (Antwerp) demonstrate how
   PR functions across substantial within-country magnitude
   variation.
3. The post-2012 BHV (Brussels-Halle-Vilvoorde) reform produced
   the current district map and is a working example of
   resolving a constitutional crisis through a redistricting
   reform.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — Constitution Art. 63

> Art. 63 § 1: La Chambre des représentants compte 150 membres.
> *(Dutch: De Kamer van Volksvertegenwoordigers telt 150 leden.)*

(Translation: The Chamber of Representatives has 150 members.)

### Districts and magnitudes

The 11 federal districts after the 2012 reform:

| District | Province / Region | Approximate magnitude |
|---|---|---:|
| Antwerpen | Antwerp province (Flanders) | ~24 |
| Brabant flamand / Vlaams Brabant | Flemish Brabant | ~15 |
| Hainaut | Hainaut (Wallonia) | ~18 |
| Liège | Liège (Wallonia) | ~15 |
| Limburg | Limburg (Flanders) | ~12 |
| Luxembourg | Luxembourg (Wallonia) | ~4 |
| Namur | Namur (Wallonia) | ~6 |
| Brabant wallon | Walloon Brabant | ~5 |
| Oost-Vlaanderen | East Flanders | ~20 |
| West-Vlaanderen | West Flanders | ~16 |
| Bruxelles-Capitale / Brussel-Hoofdstad | Brussels-Capital Region | ~15 |

(Magnitudes are recomputed per cycle from population data;
figures above are approximate from the 2024 cycle.)

The 150 seats split between two language groups:
- **Dutch-language group**: 88 seats (5 Flemish provincial
  districts + Flemish portion of Brussels-Capital).
- **French-language group**: 62 seats (5 Walloon provincial
  districts + French portion of Brussels-Capital).

The German-speaking community has no separate federal district
but elects through the Liège district.

### Operationalized values

```
total_seats:                     150 (Constitution Art. 63 § 1)
codification_instrument:         Constitution (national)
amendment_authority:             constitutional revision (special
                                 majority procedure)
amendment_threshold:             constitutional amendment

magnitude_uniform:               no
magnitude_typical:               varies by district population
magnitude_range:                 ~4 (Luxembourg) — ~24 (Antwerpen)
districts_count:                 11
districting_authority:           statutory list (Code Électoral
                                 annexes); recomputed by formula
                                 each cycle from federal census
districting_frequency_years:     each federal cycle (4-year max)
districting_criteria_in_statute: provincial boundaries respected
                                 (each province = 1 district);
                                 Brussels-Capital separate;
                                 magnitudes redistributed by
                                 population

tiered:                          no
tier_count:                      1
tier_compensatory:               not applicable

threshold_of_exclusion_pct:      ~25% (Luxembourg, M=4) → ~4%
                                 (Antwerpen, M=24)
                                 [structural, plus the 5% legal
                                 threshold per district]
```

### Notes

The Belgian federal magnitude range — 4 to 24 — produces
substantial within-country variation in how proportional the
system is in practice. In Luxembourg (M=4), the structural
threshold of exclusion (~25%) effectively eliminates small
parties. In Antwerpen (M=24), the structural threshold is well
below the legal 5% threshold, so the legal threshold is the
binding constraint.

For U.S. drafters: the Belgian district map demonstrates that
PR allocation can operate alongside provincial / state-tier
geographic boundaries that vary substantially in population.
The constraint is constitutional (Const. Art. 63 § 1 fixes 150
seats), not statutory; the provincial boundaries are a
political-historical given.

---

## 2. Component 2 — Ballot Structure

### Single vote, list vote OR candidate vote

The Belgian federal ballot is structured analogously to the
Brazilian voto-de-legenda model: voters cast a single mark
that may be expressed either as a list vote (*kopstem* /
*vote en tête de liste*) or as a candidate vote (one or more
preference marks within a list).

Per the Code Électoral:
- The voter may mark **the head box of one list** (kopstem):
  the vote counts for the list and is treated as a vote
  conferred on the candidates in submitted order.
- Alternatively, the voter may mark **one or more preference
  marks for individual candidates** within the same list.
  Multiple preference votes are valid (within a single list).
- The voter may **not** combine a kopstem with preference votes
  on the same list (would invalidate the kopstem).
- Cross-list voting (panachage) is **not** permitted at federal
  level.

This is a flexible-list system. The kopstem flows to candidates
in submitter-set order; preference votes accumulate to specific
candidates and can reorder the list above the threshold.

### Operationalized values

```
ballot_type:                     flexible_list_with_kopstem
preference_votes_per_voter:      one kopstem OR multiple
                                 preference votes within a
                                 single list
panachage_allowed:               no (federal)
cumulation_allowed:              no — each preference mark counts
                                 once
above_the_line_option:           kopstem (list vote) is
                                 functionally equivalent

party_lists_allowed:             yes
voter_grouping_lists_allowed:    no (no Wählergruppen-equivalent
                                 at federal level)
citizen_committee_lists_allowed: no
independents_on_lists_allowed:   yes (single-name lists permitted
                                 but rare)

intra_list_rule:                 hybrid_threshold (kopstem flows
                                 in submitter order; preference
                                 votes can override above the
                                 *eligibility threshold*, which
                                 in Belgium is computed from the
                                 list's seat allocation and
                                 valid votes; the precise
                                 mechanic is described in
                                 Component 3 below)
```

---

## 3. Component 3 — Allocation Formula

### Inter-list allocation: D'Hondt + 5% per-district threshold

Per the Code Électoral, federal-level seat allocation in each
district follows two steps:

1. **5% per-district threshold (introduced 2002)**: lists
   receiving fewer than **5% of valid votes** in a district are
   excluded from the allocation. This is a per-district threshold
   — a list that wins 5% in any one district participates in that
   district's allocation, regardless of its national share.
2. **D'Hondt highest-averages method**: the remaining lists'
   vote totals (kopstem + preference votes within each list)
   are divided successively by 1, 2, 3, 4, … and seats are
   assigned by descending order of the resulting quotients.

### Intra-list allocation: kopstem + preference votes

Per the Code Électoral (post-2002 reforms), intra-list seat
assignment within each list operates through an *éligibilité*
(eligibility) calculation:

1. The list's whole seats are computed from the inter-list
   allocation.
2. Half of the list's kopstem votes are added (a 2002 reform
   reduced this from full kopstem allocation; the so-called
   "2002 *devolutie* halving").
3. The kopstem votes are then distributed to candidates in
   submitter-set order, candidate by candidate, until each has
   accumulated enough votes to reach an *éligibilité* quota
   computed from the list's seat allocation.
4. Candidates who reach the éligibilité quota through a
   combination of preference votes and kopstem distribution
   are seated in the list's order of seat assignment.
5. Candidates who do not reach the quota take seats in the
   submitter-set order from the remaining seats.

### Operationalized values

```
allocation_formula:              d_hondt                        # federal
formula_codified_as:             procedural (divisor sequence
                                 1, 2, 3, 4, … specified)
formula_statutory_citation:      Code Électoral (federal)
ties_rule:                       drawing of lots; oldest
                                 candidate fallback in some
                                 historical applications

legal_threshold_pct:             5 (per district)
threshold_level:                 district
threshold_exemption_rules:       none
threshold_backdoor:              none

apparentement_allowed:           no at federal level (formerly
                                 permitted at provincial level
                                 prior to 2002; no longer in
                                 force)
intra_list_rule:                 hybrid: kopstem allocated to
                                 candidates in submitter order
                                 to reach éligibilité quota;
                                 preference votes can override
                                 above the quota
preference_threshold_pct:        computed per list per cycle
                                 (the éligibilité quota); not a
                                 fixed percentage
intra_list_ties_rule:            lot
```

### Notes

**The éligibilité mechanism is a flexible-list architecture.**
The kopstem votes count first toward the candidates in submitter
order; preference votes can lift candidates ahead of the order
if they cross the quota. Post-2002 reforms halved the weight of
kopstem in the éligibilité calculation, intentionally
strengthening the role of preference votes. This is a working
flexible-list parameter that U.S. drafters can adapt: the
"weight of the list-mark" in intra-list ordering is a
statutorily tunable choice between 0% (pure preference, as in
Bavaria GLKrWG Art. 36(1)) and 100% (binding submitter order,
as in NRW KWahlG § 33(6)). Belgium federal sits at 50%.

**The 5% per-district threshold is a notable contrast** with
the German federal 5% nationwide threshold. Belgium's
per-district application means a regional party can win seats
in its home province even with a national vote share well below
5%. The German model (BWahlG § 4(2) #2) excludes such parties
unless they meet the *Grundmandatsklausel* exception; the
Belgian model embeds the regional accommodation directly in
the allocation rule.

For U.S. drafting in a state-legislature context with
geographically distinct constituencies (e.g., urban / rural
divides), the Belgian per-district threshold model is the more
portable variant.

---

## 4. Connected areas (brief)

### A. Voter eligibility

Belgian citizens aged 18+, or EU citizens for the EU-Parliament
and municipal levels (federal level is citizens-only). Voting
is **compulsory** at federal level; non-voters face a fine
under the Code Électoral.

### B. Candidate / list registration

Per Code Électoral provisions on *présentation des candidats*
(candidate presentation):

- Lists are submitted by registered political parties, or by a
  group of voters submitting a non-party list.
- Signature requirements:
  - Existing parties (with at least one seat in the previous
    Parliament): exempt.
  - New parties or non-party lists: typically 200–500 voter
    signatures per district, with regional variation.
- Lists submitted through a *bureau électoral* (electoral
  bureau) at the district level.

### C. Campaign finance

Governed by the Loi du 4 juillet 1989 and subsequent reforms.
Public funding for parties (per-vote and per-seat formula);
spending caps per candidate and per party per district;
disclosure to the *Commission de contrôle des dépenses
électorales*.

### D. Election administration

Decentralized — administered by *bureaux électoraux* at three
levels (district, canton, polling station). Federal coordination
through the Federal Public Service Interior (FPS Interior /
*SPF Intérieur* / *FOD Binnenlandse Zaken*).

### E. Vote count, certification, dispute resolution

Counting at the polling station; results aggregated through
canton and district to the federal level. Election challenges
under Constitution Art. 48: each chamber verifies its own
elections in the first instance. Appeals to the Council of State
(*Conseil d'État* / *Raad van State*) on administrative-law
grounds.

### F. Media access

Public broadcasters allocate political broadcast time by formula
under regional media legislation (Flanders, Wallonia, German-
speaking Community each have their own regimes).

### G. (Districting law — captured under Component 1)

---

## 5. PROSeS performance diagnostic

The empirical anchor is the **9 June 2024 federal election** —
held simultaneously with European and regional elections,
producing the largest joint Belgian electoral exercise in
recent memory.

### Process Design and Resource Investment

Belgian federal elections are professionally administered with
high integrity ratings in international comparative indices.
The decentralized count produces preliminary results election
night.

### Service Output Quality

Compulsory voting plus electronic voting in some districts
produces high turnout (~89% in 2024). Invalid-vote rates
typically under 5% (relatively high for European comparisons,
reflecting compulsory voting effects).

### Service Outcomes

**Voter turnout** at the 9 June 2024 federal election was
**88.4%** of registered voters.

**Equity / minority representation**: the language-group split
(88 Dutch / 62 French) is structurally guaranteed and produces
substantively different political competitions on the two
sides of the language frontier. Migrant-origin representation
varies substantially by district.

### Stakeholder Satisfaction

Generally high; the 2012 BHV reform was a major political
achievement (resolving a long-running constitutional dispute)
and has not been substantively re-litigated.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # citizens 18+
equal_suffrage:        compliant
free_suffrage:         partial     # compulsory voting raises
                                   # the standard question
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant
fundamental_rights:    compliant
regulatory_stability:  high        # post-2012 BHV reform stable
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

| Provision | Type | Rationale |
|---|---|---|
| D'Hondt + 5% per-district threshold | **Universal** | Standard continental-European federal-PR architecture; portable to U.S. state-legislature contexts. |
| Kopstem (list vote) with éligibilité-quota intra-list reordering | **Universal** | Tunable flexible-list parameter — list-mark weight in intra-list ordering can be set anywhere between 0% and 100%. |
| Per-district 5% threshold (rather than nationwide) | **Universal** | More portable to U.S. state-legislature contexts than nationwide threshold; permits regional variation in party support. |
| Compulsory voting | **Particular** | Politically and constitutionally untenable in U.S. contexts. |
| Constitutional fixing of Chamber size | **Hybrid** | Substantive choice portable; constitutional placement reflects Belgian institutional history. |
| Language-group seat split | **Particular** | Brussels / Wallonia / Flanders dynamic with no U.S. analog. |

### Top three takeaways for US state/local implementation

1. **Per-district threshold is the more portable threshold
   model.** A 5% threshold applied within each district,
   rather than nationwide, preserves regional small-party
   participation while still filtering nationwide
   fragmentation. For U.S. state legislatures with substantial
   urban / rural variation, the Belgian model produces fewer
   constitutional concerns than a nationwide threshold.

2. **The éligibilité-quota intra-list reordering rule is a
   tunable flexible-list parameter.** The 2002 halving of
   kopstem weight in the éligibilité calculation demonstrates
   that the "weight of the list-mark" is statutorily
   adjustable. U.S. drafters can set this parameter at any
   point between 0% (pure preference, as Bavaria) and 100%
   (binding list order, as NRW).

3. **D'Hondt is the project's best-documented working federal
   formula despite its larger-party bias.** Belgium has
   operated D'Hondt at federal level continuously since 1899;
   the Belgian experience demonstrates that the larger-party
   bias is politically tolerable in a multi-party system with
   strong regional parties. U.S. drafters comparing
   Sainte-Laguë (Germany) and D'Hondt (Belgium) at state-
   legislature scale should see Belgium as the working
   D'Hondt example.

---

## 8. Sources

### Primary

- **Constitution belge / Belgische Grondwet**, Articles 61–63
  (Chamber of Representatives).
  <https://www.dekamer.be/kvvcr/pdf_sections/publications/constitution/grondwetEN.pdf>
- **Code Électoral / Algemeen Kieswetboek** (Loi du 12 avril
  1894 / Wet van 12 april 1894).
- **Loi du 4 juillet 1989** — campaign finance.

### Secondary

- *Inter-Parliamentary Union — Belgium (Chambre des
  Représentants), Electoral system*:
  <http://archive.ipu.org/parline-e/reports/2029_B.htm>
- Wikipedia — Chamber of Representatives (Belgium):
  <https://en.wikipedia.org/wiki/Chamber_of_Representatives_(Belgium)>
- Wikipedia — 2024 Belgian federal election:
  <https://en.wikipedia.org/wiki/2024_Belgian_federal_election>

### Outstanding gaps

- Verbatim text of the Code Électoral provisions on D'Hondt
  allocation and the 5% threshold (post-2002 reform language).
- Verbatim text of the Code Électoral provisions on
  *éligibilité* and intra-list reordering.
- 2024 federal election outcome data: invalid-vote rate by
  district; share of seats won via preference votes vs
  kopstem ordering.
- Cached PDF of the consolidated Code Électoral.
