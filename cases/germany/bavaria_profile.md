# Bavaria — Local elections (Gemeinde- und Landkreiswahlen)

## 0. Case metadata

- **Country**: Federal Republic of Germany
- **Sub-jurisdiction**: Free State of Bavaria (*Freistaat Bayern*)
- **Level of government**: Local — municipal (*Gemeinde*) councils,
  county (*Landkreis*) councils, mayors, and county heads
- **Electoral system family**: Open-list PR with **cumulation and
  panachage**; *Wählergruppen* (voter groupings) compete on equal
  footing with parties
- **Governing statute (primary)**: *Gemeinde- und Landkreiswahl-
  gesetz* (GLKrWG) — Bavarian Municipal and District Elections Act
- **Citation**: GLKrWG in der Fassung der Bekanntmachung vom 7.
  November 2006 (GVBl. S. 834), zuletzt geändert durch § 1 des
  Gesetzes vom 24. Juli 2023 (GVBl. S. 385). BayRS 2021-1/2-I.
  Articles 1–61.
- **URL**: <https://www.gesetze-bayern.de/Content/Document/BayGLKrWG/true>
- **Implementing regulation**: *Gemeinde- und Landkreiswahlordnung*
  (GLKrWO), 7. November 2006 (GVBl. S. 852), §§ 1–103.
  <https://www.gesetze-bayern.de/Content/Document/BayGLKrWO/true>
- **Constitutional anchors**:
  - *Bayerische Verfassung* (Bavarian Constitution) Art. 11(2) —
    municipal self-governance and the right of municipalities to
    elect mayors and councils.
  - *Bayerische Gemeindeordnung* (Municipal Code, GO) Art. 17 —
    municipal-citizen election of council and mayor.
  - *Bayerische Gemeindeordnung* (GO) Art. 31 — composition and
    size of the *Gemeinderat* (set by population).
  - *Bayerische Landkreisordnung* (LKrO) — parallel framework for
    county councils.
- **Next regular election**: March 2026.
- **Analyst**: (this profile, 2026-05-05)

### Why this case is in the project

Bavaria is the project's analytical center for **non-partisan list
administration in local elections**. Three features are diagnostic:

1. **Wählergruppen** — voter groupings — compete on equal footing
   with registered parties under GLKrWG Art. 24. The legal
   definition of a *Wählergruppe* is unusually permissive: "all
   other associations or groups of natural persons whose purpose
   is to participate in municipal or county elections." No fixed
   organizational structure is required.
2. **Cumulation (up to 3 votes per candidate) and panachage**
   under GLKrWG Art. 34 give voters extensive intra-list and
   cross-list power. The combination of high district magnitude
   (M up to 80 in Munich) with these mechanics produces what is
   commonly cited as the most permissive open-list system in
   continental Europe at the local level.
3. **Sainte-Laguë / Webster** allocation under GLKrWG Art. 35
   (since 2018, replacing Hare-Niemeyer 2014, replacing D'Hondt
   pre-2010). Bavaria's trajectory toward the least-biased
   formula is itself a useful drafting precedent.

In contrast to the federal profile, the Bavarian regime is
**substantively non-partisan**: parties and voter groupings are
treated symmetrically in the statute, and Wählergruppen
historically win significant council representation in many
Bavarian municipalities.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — Art. 31 *Bayerische Gemeindeordnung*

Assembly size for municipal councils is set in the *Gemeindeordnung*
(GO), not in the elections act:

> Art. 31 Abs. 1: Der Gemeinderat besteht aus der ersten
> Bürgermeisterin oder dem ersten Bürgermeister und den
> Gemeinderatsmitgliedern.

(*The Gemeinderat consists of the First Mayor and the council
members.*)

The number of council members (*Gemeinderatsmitglieder*) scales
with population:

| Einwohnerzahl (population) | Mitgliederzahl (members) |
|---|---:|
| up to 1,000 | 8 |
| 1,001 – 2,000 | 12 |
| 2,001 – 3,000 | 14 |
| 3,001 – 5,000 | 16 |
| 5,001 – 10,000 | 20 |
| 10,001 – 20,000 | 24 |
| 20,001 – 30,000 | 30 |
| 30,001 – 50,000 | 40 |
| 50,001 – 100,000 | 44 |
| 100,001 – 200,000 | 50 |
| 200,001 – 500,000 | 60 |
| Nürnberg | 70 |
| München | 80 |

Augsburg (the third-largest Bavarian municipality, ~300,000) sits
in the 200,001–500,000 tier with 60 members.

For *Landkreis* councils, the *Landkreisordnung* (LKrO) sets the
parallel population-tiered table (50, 60, or 70 members).

### Statutory text — Art. 11 GLKrWG (Wahlkreis, Stimmbezirke)

The Bavarian municipality is, by default, a **single electoral
district**: each municipality is its own *Wahlkreis* for the
purposes of *Gemeinderat* elections. This means the **district
magnitude equals the assembly size** — M = 8 for the smallest
municipalities, M = 80 for Munich.

The municipality is then sub-divided into *Stimmbezirke* (polling
districts) for administrative purposes only; this does not
fragment the proportional pool.

### Operationalized values

```
total_seats:                     8 (smallest) — 80 (Munich)
codification_instrument:         Bayerische Gemeindeordnung Art. 31
                                 (statute); GO is the basic Land
                                 statute, not the elections act
amendment_authority:             Bayerischer Landtag
amendment_threshold:             ordinary Land legislation

magnitude_uniform:               yes within each municipality
magnitude_typical:               variable by population
magnitude_range:                 8 — 80 (municipalities); 50 — 70
                                 (Landkreise)
districts_count:                 1 per municipality / Landkreis
districting_authority:           N/A — district is the
                                 municipality itself
districting_frequency_years:     N/A
districting_criteria_in_statute: N/A

tiered:                          no
tier_count:                      1
tier_compensatory:               not applicable

threshold_of_exclusion_pct:      11.1% (M=8) → 1.23% (M=80)
                                 [structural; no legal threshold]
```

### Notes

The **assembly-size table** is the structural keystone of Bavarian
local PR. By tying assembly size to population in statute, GO
Art. 31 forecloses the political fight over council size that
dominates US local-reform proposals and that the primer documents
extensively (pp. 5–8).

The **single-district-per-municipality** structure is the second
keystone. Where US local reform commonly debates whether to
preserve geographic districts or move to at-large representation,
Bavaria has settled on **at-large representation with high
magnitude** as the default for proportional outcomes. The
equivalent US challenge — that at-large election under block
plurality vote produces winner-take-all outcomes (primer pp. 5–8)
— is solved in Bavaria by the combination of high M with open-list
PR (Components 2 and 3).

For US implementation, the threshold-of-exclusion math is
diagnostic:

- Munich (M=80) → 1.23% threshold of exclusion. Effectively no
  barrier for any organized minority constituency.
- Nuremberg (M=70) → 1.41%.
- Augsburg / large cities (M=60) → 1.64%.
- Mid-size cities (M=44) → 2.22%.
- Small towns (M=8) → 11.1%. The smallest Bavarian municipalities
  function effectively as small-magnitude PR, and at this M the
  formula choice (Sainte-Laguë vs. D'Hondt) starts to matter.

---

## 2. Component 2 — Ballot Structure

### Statutory text — Art. 34 GLKrWG (Stimmenzahl und Vergabe der Stimmen)

The architecturally central provision. Translated paragraph by
paragraph:

> **Art. 34 Stimmenzahl und Vergabe der Stimmen**
>
> Liegen mehrere Wahlvorschläge vor, wird das Stimmrecht nach den
> Grundsätzen der Verhältniswahl unter Beachtung der nachstehenden
> Bestimmungen ausgeübt:
>
> 1. Die stimmberechtigte Person hat so viele Stimmen, wie
>    ehrenamtliche Gemeinderatsmitglieder oder Kreisrätinnen und
>    Kreisräte zu wählen sind.
>
> 2. Die stimmberechtigte Person kann ihre Stimmen nur sich
>    bewerbenden Personen geben, deren Namen in einem zugelassenen
>    Wahlvorschlag enthalten sind.
>
> 3. Die stimmberechtigte Person kann durch Kennzeichnung eines
>    Wahlvorschlags diesen unverändert annehmen. Eine unveränderte
>    Annahme liegt nicht vor, wenn die stimmberechtigte Person
>    außerdem in einem oder mehreren Wahlvorschlägen einzelnen
>    sich bewerbenden Personen Stimmen gibt.
>
> 4. Die stimmberechtigte Person kann innerhalb der ihr zustehenden
>    Stimmenzahl einer sich bewerbenden Person bis zu drei Stimmen
>    geben.
>
> 5. Die stimmberechtigte Person kann innerhalb der ihr zustehenden
>    Stimmenzahl ihre Stimmen sich bewerbenden Personen aus
>    verschiedenen Wahlvorschlägen geben.

(*English: Where multiple electoral nominations are submitted, the
right to vote is exercised according to the principles of
proportional representation, subject to the following provisions:*

*1. The voter has as many votes as honorary members of the
*Gemeinderat* or *Kreistag* are to be elected.*

*2. The voter may give votes only to candidates whose names are
listed in an admitted electoral nomination.*

*3. The voter may accept an electoral nomination unchanged by
marking it. Unchanged acceptance does not exist if the voter
also gives votes to individual candidates in one or more
nominations.*

*4. The voter may give a single candidate up to three votes,
within the voter's total vote allocation.*

*5. The voter may give votes to candidates from different
electoral nominations, within the voter's total vote allocation.*)

### Mechanics

Three voting strategies are statutorily available:

1. **Listenkreuz only** (no. 3): mark a single list to accept it
   unchanged. Votes flow to candidates in list order until the
   voter's total vote allocation is exhausted.
2. **Cumulation** (no. 4, *kumulieren* / *häufeln*): give a
   single candidate up to three votes. Used to boost preferred
   candidates within a list.
3. **Panachage** (no. 5, *panaschieren*): give votes to
   candidates across different lists, regardless of party or
   group affiliation.

These strategies can be combined: a voter with 80 votes (Munich)
might cumulate 3 votes for each of 6 favored candidates across 4
different lists (18 votes used) and then mark a list header for
the remaining 62 votes to flow in list order.

Per Art. 34 no. 3 second sentence: **the list-mark (Listenkreuz)
is overridden by individual candidate votes in the same or
another list**, but the residual flows in list order.

### Statutory text — Art. 16 GLKrWG (Stimmzettel)

> Art. 16: "Für die Wahl wird amtlicher Stimmzettel verwendet."

Detailed ballot specifications are in the *Gemeinde- und
Landkreiswahlordnung* (GLKrWO) §§ 38–40 (not yet quoted in this
profile). Each electoral nomination has its own column with the
nomination's *Kennwort* (label), candidate names with personal
data (occupation, address, year of birth), and circles for
marking.

### Operationalized values

```
ballot_type:                     open_list_with_cumulation_and_panachage
preference_votes_per_voter:      = number of seats to fill
                                 (8 to 80 depending on municipality)
panachage_allowed:               yes (Art. 34 no. 5)
cumulation_allowed:              yes (Art. 34 no. 4)
cumulation_max:                  3 votes per candidate
above_the_line_option:           yes — *Listenkreuz* (Art. 34 no. 3)
list_vote_only_distribution:     in list order (Art. 36 by
                                 implication: residual list-mark
                                 votes are added to each
                                 candidate's personal total in
                                 list order)

party_lists_allowed:             yes
voter_grouping_lists_allowed:    yes (Art. 24(1))
voter_grouping_legal_term:       Wählergruppe / Wählervereinigung
citizen_committee_lists_allowed: yes — any "association or group of
                                 natural persons" qualifies (Art.
                                 24(1) sentence 2)
independents_on_lists_allowed:   yes (an individual may form a
                                 single-name *Wahlvorschlag*)

non_party_label_allowed:         yes (the list's *Kennwort* — see
                                 GLKrWO and Art. 25)
non_party_label_categories:      not statutorily restricted to
                                 categories (geographic / civic /
                                 advocacy / generic — all permitted)
non_party_label_restrictions:    no name confusable with a party
                                 already on the ballot; no
                                 misleading state-organ implication
label_validation_authority:      Wahlausschuss (electoral committee)
                                 under Art. 32 (Zulassung der
                                 Wahlvorschläge)
```

### Notes

Bavaria's ballot structure is at the **most permissive end of the
list-PR spectrum** the Guinier Project primer describes (pp. 11–12).
It is more permissive than the federal Bundestag closed list, more
permissive than Spanish closed-list LOREG, and roughly comparable
to Finnish open-list practice but with cumulation added.

Trade-off: **ballot complexity**. The Munich ballot, with 80 vote
slots and frequently 8–12 lists each running 80 candidates, is one
of the most cognitively demanding ballots in any developed
democracy. The 2020 Munich ballot was reported to be over a meter
in length. The primer's "value of simplicity" caution (p. 13)
applies — the Bavarian system delivers high voter agency at the
cost of long counting times and non-trivial voter-error risk.

For US implementation:

1. **Cumulation (kumulieren) up to 3 votes per candidate** is
   directly portable. US precedents (Texas, Alabama local
   cumulative-vote remedies) already establish constitutional
   tractability. Bavaria's specific 3-vote cap is one drafting
   choice; the US precedents use varying caps.
2. **Panachage** has no direct US precedent. US implementation
   would need to reckon with state ballot-uniformity laws and
   anti-fusion rules.
3. **The Listenkreuz default** (mark one list, votes flow in list
   order) is the simplicity backstop. A US implementation could
   adopt this as the only voting mode, with cumulation and
   panachage as opt-in advanced options — analogous to the
   Australian above-the-line / below-the-line distinction
   (`cases/australia/README.md`).

---

## 3. Component 3 — Allocation Formula

### Statutory text — Art. 35 GLKrWG (Verteilung der Sitze auf die Wahlvorschläge)

> **Art. 35 Verteilung der Sitze auf die Wahlvorschläge**
>
> (1) Die Sitze werden auf die Wahlvorschläge nach dem Verhältnis
> der Gesamtzahlen der gültigen Stimmen verteilt, welche für die
> in den Wahlvorschlägen aufgeführten sich bewerbenden Personen
> abgegeben worden sind.

(*Seats are allocated among electoral nominations in proportion
to the total numbers of valid votes given to candidates in those
nominations.*)

> (2) [The seat distribution proceeds by the Sainte-Laguë method:]
> die Gesamtstimmenzahlen, die für die einzelnen Wahlvorschläge
> festgestellt worden sind, [werden] nacheinander so lange durch
> 1, 3, 5, 7, 9 und so weiter geteilt [...].

(*The total vote counts for each electoral nomination are
successively divided by 1, 3, 5, 7, 9 and so on. Seats are
awarded by descending order of the resulting quotients. Ties are
resolved by the higher personal vote total of the affected
candidate, or failing that, by lot.*)

> (3) Fallen einem Wahlvorschlag mehr Sitze zu, als er sich
> bewerbende Personen enthält, bleiben die übrigen Sitze
> unbesetzt.

(*If more seats fall to an electoral nomination than the nomination
has candidates listed, the surplus seats remain vacant.*)

### Statutory text — Art. 36 GLKrWG (Verteilung der Sitze an Personen)

> **Art. 36 Verteilung der Sitze an Personen**
>
> (1) Die einem Wahlvorschlag zugefallenen Sitze werden den darin
> enthaltenen sich bewerbenden wählbaren Personen in der
> Reihenfolge ihrer Stimmenzahlen zugewiesen.
>
> (2) Haben mehrere sich bewerbende Personen die gleiche
> Stimmenzahl erhalten, entscheidet das Los.

(*(1) Seats assigned to an electoral nomination are allocated to
its eligible candidates in the order of their vote totals.
(2) If several candidates have received the same vote total, lot
decides.*)

### Operationalized values

```
allocation_formula:              webster_sainte_lague           # Art. 35(2)
formula_codified_as:             procedural — the divisor sequence
                                 "1, 3, 5, 7, 9 und so weiter" is
                                 stated explicitly in the statute,
                                 without using the eponym
formula_statutory_citation:      GLKrWG Art. 35
ties_rule:                       higher personal vote total of the
                                 affected candidate, then lot
                                 (Art. 35(2)); for intra-list ties,
                                 lot only (Art. 36(2))

legal_threshold_pct:             none (Bavaria sets no statutory
                                 threshold for local PR)
threshold_level:                 not applicable
threshold_exemption_rules:       not applicable
threshold_backdoor:              not applicable

apparentement_allowed:           no (the statute speaks of
                                 individual *Wahlvorschläge*; joint
                                 lists submitted by multiple groups
                                 are permitted under Art. 24 / 27
                                 *as a single Wahlvorschlag* with
                                 attendant equal-treatment rules,
                                 but post-vote pooling between
                                 separate Wahlvorschläge is not
                                 provided for)

intra_list_rule:                 pure_preference                # Art. 36(1)
preference_threshold_pct:        not applicable — every personal
                                 vote counts; there is no
                                 "reordering threshold" as in
                                 some flexible-list systems
intra_list_ties_rule:            lot (Art. 36(2))
```

### Notes

**Three features distinguish the Bavarian allocation regime from
the federal Bundestag regime**:

1. **No legal threshold**. Bavarian local PR has only the natural
   threshold imposed by district magnitude. In Munich (M=80,
   threshold of exclusion ≈ 1.23%), this means small civic groups
   can win representation on the strength of a few thousand
   first-vote-totals. In smaller municipalities (M=8), the
   ≈11% natural threshold filters fragmentation without any
   statutory percentage threshold being needed.
2. **Pure preference voting within lists** (Art. 36(1)): the list
   order set by the submitter is **non-binding**. Candidates are
   seated in descending order of personal vote totals only. This
   is the maximally voter-driven intra-list rule on the spectrum
   `dimensions: list_order < hybrid_threshold < pure_preference`.
3. **Sainte-Laguë / Webster** at the inter-list step (Art. 35(2))
   means the formula choice itself is minority-friendly at the
   small-M end of the population scale. The combination of pure
   preference + Webster + no threshold is, mathematically, the
   most representation-permissive set of choices Bavaria could
   make.

#### The Bavarian formula trajectory

| Period | Formula | Source |
|---|---|---|
| Pre-2010 | D'Hondt (Jefferson) | original GLKrWG |
| 2014 only | Hare-Niemeyer (Hamilton) | one-time amendment |
| 2018 onward | Sainte-Laguë (Webster) | statutory amendment, in force for the 2020 and 2026 elections |

This trajectory mirrors academic and primer-aligned thinking that
Webster is the least-biased divisor formula. The 2014 single-cycle
use of Hamilton (Hare quota) demonstrates that legislatures *can*
switch formulas between cycles where the political will exists; it
is also a useful precedent that small parties can shift formula
choice through ordinary legislation.

#### Why this matters for US implementation

1. **No statutory threshold** demonstrates that high-M PR can
   function without one — a useful answer to the political concern
   that PR will lead to splinter-party fragmentation. Bavaria
   relies on **structural threshold from M alone**.
2. **The pure-preference intra-list rule** (Art. 36) is a
   drafting solution to the criticism that closed-list PR
   "disempowers voters." Voters retain full control over which
   list candidates are seated.
3. **The named-divisor formulation** (Art. 35(2): "durch 1, 3, 5,
   7, 9 und so weiter") is a model of statutory drafting clarity:
   the formula is reproducible from the statutory text alone, no
   reference to the eponym Sainte-Laguë required.

---

## 4. Connected areas (brief)

### A. Voter eligibility

GLKrWG Art. 1 (Wahlrecht) extends the franchise to:

- German citizens (Art. 116(1) GG);
- **Citizens of other EU member states** resident in the
  municipality (per EU directives transposed into Bavarian law).

Other criteria (cumulative): age 18 on election day; principal
residence in the municipality for at least **two months** before
election day. § 6 of the GLKrWO sets the registration
infrastructure. Disqualification under Art. 2 GLKrWG runs through
judicial decision (cross-reference to BWahlG § 13 federally).

### B. Candidate / list registration — *full subsection*

The single most analytically central area for the project. The
core statutory text:

#### Statutory text — Art. 24(1) GLKrWG (Wahlvorschlagsrecht)

> Art. 24(1): Wahlvorschläge können von Parteien und von
> Wählergruppen eingereicht werden (Wahlvorschlagsträger).
> **Wählergruppen sind alle sonstigen Vereinigungen oder Gruppen
> natürlicher Personen, deren Ziel es ist, sich an Gemeinde- oder
> an Landkreiswahlen zu beteiligen.** Neue Wahlvorschlagsträger
> sind solche, die im Gemeinderat oder Kreistag seit der letzten
> Wahl bis 90 Tage vor dem Wahltag nicht ununterbrochen vertreten
> waren.

(*Electoral nominations may be submitted by parties and by voter
groupings (list-bearing entities). **Voter groupings are all
other associations or groups of natural persons whose purpose is
to participate in municipal or county elections.** New
list-bearing entities are those that have not been continuously
represented in the *Gemeinderat* or *Kreistag* since the last
election until 90 days before election day.*)

The **definitional sentence** (emphasized) is the project's
single most important quoted text. Three features deserve
specific attention:

1. **"Sonstige Vereinigungen oder Gruppen"** — "other
   associations or groups." The set is residual: anything that
   is not a *Partei* (under PartG § 2) but is organized to
   contest the election. This is intentionally permissive.
2. **"Natürlicher Personen"** — natural persons only. This
   excludes corporations, associations of associations, etc.
3. **"Deren Ziel es ist, sich an Gemeinde- oder an
   Landkreiswahlen zu beteiligen"** — "whose purpose is to
   participate in municipal or county elections." The
   organizational purpose itself defines the group; no minimum
   membership, registration history, or organizational form is
   required.

The German Wikipedia article on Bavarian municipal electoral law
summarizes this as: "ein festes Organisationsgefüge ist also
nicht Voraussetzung" — *a fixed organizational structure is
therefore not a prerequisite*.

#### Statutory text — Art. 27 GLKrWG (Unterstützung von Wahlvorschlägen)

Signature requirements apply only to **new** list-bearing
entities (per Art. 24(1) third sentence). Established
*Wahlvorschlagsträger* (those continuously represented in the
relevant body since the last election) are exempt, as are parties
or voter groupings that received at least 5% of valid votes in
the most recent state, federal, or European Parliament election.

The signature thresholds scale with municipal population. Per
Art. 27(3):

| Municipality / Landkreis population | Required signatures |
|---|---:|
| up to 1,000 | 40 |
| 1,001 – 2,000 | 50 |
| 2,001 – 3,000 | 60 |
| 3,001 – 5,000 | 80 |
| 5,001 – 10,000 | 100 |
| 10,001 – 20,000 | 140 |
| 20,001 – 30,000 | 180 |
| 30,001 – 50,000 | 240 |
| 50,001 – 100,000 | 320 |
| 100,001 – 200,000 | 400 |
| 200,001 – 500,000 | 540 |
| 500,001 – 1,000,000 | 720 |
| over 1,000,000 | 1,000 |

(Intermediate brackets reconstructed from the OSCE / Bavarian
Ministry of the Interior synopse; verify exact numbers in
Art. 27(3) before drafting model legislation.)

#### Statutory text — Art. 28 GLKrWG (Eintragung in Unterstützungslisten)

The unusually rigorous mechanism: signatures are **not** collected
by the list-bearing entity itself. Instead, supporters must appear
**in person at the municipal administration office** and sign a
public *Unterstützungsliste* maintained by the *Wahlleiter*
(Returning Officer). This converts signature-gathering into a
quasi-public act and forecloses door-to-door or online
collection.

#### Operationalized values

```
list_registration_authority:     municipal Wahlleiter / Wahlausschuss
                                 (Art. 4–5)
signatures_required_min:         40 (smallest municipalities)
signature_scaling:               population-tiered (Art. 27(3))
signature_geographic_distribution:
                                 N/A — signatures must be from
                                 registered voters of the
                                 municipality, no geographic spread
                                 required within
signature_collection_mode:       in-person at municipal office only
                                 (Art. 28); not collected by the
                                 list-bearing entity
deposit_amount:                  none
deposit_currency:                N/A
deposit_refund_threshold:        N/A
filing_deadline_days_before:     to be confirmed (typically 90 days
                                 before election day per other
                                 GLKrWG provisions)
party_v_nonparty_equal_treatment:
                                 yes — the same Art. 27 signature
                                 schedule applies to both parties
                                 and Wählergruppen if "new"
list_size_min:                   not statutorily fixed
list_size_max:                   1.5 × number of seats (typical
                                 cap in GLKrWO; verify exact text)
list_ordering_rule:              submitter — but Art. 36(1) makes
                                 list order non-binding;
                                 candidates are seated by personal
                                 vote totals
gender_quota:                    none (Bavaria has rejected
                                 statutory quotas; see "Bayerische
                                 Verfassungsgerichtshof" decisions
                                 paralleling the federal pattern)
gender_quota_pct:                N/A
residency_required:              candidate must be eligible to
                                 vote in the municipality
                                 (Art. 21)
multiple_candidacy_restrictions:
                                 candidate may appear on only one
                                 Wahlvorschlag in the election
```

#### Notes — the most important comparative finding for US implementation

Three features of the Bavarian non-party list regime have
**direct application** to US local non-partisan reform:

1. **The residual definition of *Wählergruppe* (Art. 24(1))**
   solves the labeling problem the primer flags (p. 12) at the
   conceptual level. Any organized group with the purpose of
   contesting the election qualifies — no professional-association,
   advocacy-cause, geographic-region, ethnic-affiliation, or
   generic-letter requirement. The list submits a *Kennwort*
   (label) which the Wahlausschuss approves at admission stage.
2. **The in-person municipal-office signature mechanism (Art.
   28)** is unusually rigorous and would be politically novel in
   the US. It both prevents fraudulent signatures and creates
   visible barriers; ODIHR equivalent body would likely flag the
   in-person requirement as exceeding international good
   practice. For US implementation, a hybrid (online + in-person
   verification) is the more likely path.
3. **Equal-treatment with parties** (the same Art. 27 schedule,
   the same Art. 25 nomination-form requirements) is the
   *legislative-drafting* answer to the partisan/non-partisan
   asymmetry primer p. 12 raises. The Bavarian statute does not
   contain *one* word that distinguishes parties from voter
   groupings in any of Components 1–3 — only the predicate
   "Wahlvorschlagsträger" applies throughout.

### C. Campaign finance

Local-level campaign finance is **decentralized** in Germany.
Federal *Parteiengesetz* applies to *parties* (per PartG § 2)
including their local activities; **Wählergruppen are not subject
to the Parteiengesetz**. There is no Bavarian-level analog to
PartG with comparable detail; local campaign finance for voter
groupings is largely unregulated beyond general municipal
transparency norms.

This is itself a significant finding: **the partisan/non-partisan
distinction in Bavarian law produces a regulatory asymmetry** in
which Wählergruppen face less stringent disclosure than party
local branches. ODIHR has flagged the broader gap in Germany's
campaign-finance regime; the local-level gap is narrower but
structurally similar.

For US implementation, this is a cautionary tale: a model statute
that *only* regulates parties leaves a ready-made loophole.

### D. Election administration

The four-tier structure under GLKrWG Art. 4–8:

- **Wahlleiterin/Wahlleiter** (Returning Officer) for each
  municipality / *Landkreis* — the administrative head;
- **Wahlausschuss** (Electoral Committee) — the multi-member
  decision body for list admission and result certification;
- **Wahlvorsteherin/Wahlvorsteher** (Polling Station Chair) —
  per polling district;
- **Wahlvorstand** (Polling Board) — members assisting the chair.

Returning Officers are typically civil servants; the chair
position rotates among polling stations. Decentralization is
strong: each municipality runs its own elections, with state-level
oversight only for compliance.

### E. Vote count, certification, dispute resolution

Counting and certification are governed by the *GLKrWO* (the
implementing regulation) §§ 75–87 (full text not yet quoted in
this profile — primary outstanding gap).

Dispute resolution is in:
- **GLKrWG Art. 50** — *Wahlprüfung* (election review): formal
  examination of the election by a designated reviewing authority.
- **GLKrWG Art. 51** — *Wahlanfechtung* (election challenge):
  the formal contestation procedure; a challenge may be lodged
  by eligible voters of the municipality.
- **GLKrWG Art. 51a** — *Rechtsweg*: appeal lies to the
  *Verwaltungsgerichte* (administrative courts) per general
  Bavarian administrative law.

The federal *Wahlprüfungsgesetz* and the BVerfG appeal route do
*not* apply at the municipal level; election challenges run
through the *Verwaltungsgerichtsbarkeit* (administrative
jurisdiction) instead.

### F. Media access

Not extensively governed at the Bavarian municipal level; equal-
treatment doctrines from federal *Medienstaatsvertrag* and
public-broadcaster law apply. No municipality-specific broadcast-
allocation rules.

---

## 5. PROSeS performance diagnostic

The project's empirical anchor for Bavaria is the **2020 Bavarian
local elections** (15 March 2020). The next regular election is
**8 March 2026**, falling within the project's planning window —
an OSCE-style assessment specific to Bavaria is not customary, so
empirical evidence comes from:

- *Bayerisches Landesamt für Statistik* — official results.
- Academic literature on the 2020 elections.
- Bayerischer Verfassungsgerichtshof (BayVerfGH) decisions on
  electoral disputes.

Subsections below note evidence where it exists; absences are
themselves findings (per the PROSeS posture in
`framework/performance.md`).

### Process Design

The Bavarian regime decentralizes administration to the
municipality. This produces **high local accountability** but
makes systemic process review (along the lines of OSCE/ODIHR
federal-election observation) harder. There is no regular
publication of consolidated *Bavaria-wide* process-design
metrics.

### Resource Investment

Election cost reimbursement is governed by GLKrWG Art. 54
(*Kosten*) and is shared between the *Land* and the
*Gemeinden*. No publicly disaggregated per-vote cost data is
routinely published.

### Service Output Quality

**Convenience**: postal voting available; in-person registration
required for non-party support signatures (Art. 28) is at the
restrictive end of OSCE good practice.

**Accuracy**: ballot complexity (cumulation + panachage + 80
candidates per list) is a known driver of invalid-vote rates.
Comparative data on invalid-vote rates between Bavarian
municipal and other German *Land* municipal elections is a
useful empirical project in its own right.

**Enforcement**: the *Wahlausschuss* (electoral committee)
applies admission rules under Art. 32 with limited discretion;
appeals run to administrative courts.

**Efficiency**: counting cumulated and panachaged ballots is
substantially more time-consuming than counting plurality or
closed-list ballots. The 2020 election in Munich produced final
results approximately 24 hours after polls closed.

### Service Outcomes

**Turnout** at Bavarian local elections has historically tracked
around 55–65%, with 2020 reflecting pandemic-era effects.

**Equity**: the system's principal equity-relevant feature is its
hospitability to **small civic groups**. In 2020, **over 30% of
seats in Bavarian municipalities went to candidates of
*Wählergruppen* rather than political parties**. This is the
clearest empirical confirmation that the regime functions as a
non-party list system at scale.

**Diffuse impact**: the prevalence of Wählergruppen has been
linked to higher rates of local political engagement and lower
rates of straight-party voting, though formal causal evidence is
limited.

### Stakeholder Satisfaction

Not systematically surveyed. Anecdotally, Bavarian voters are
reported to value the cumulation/panachage system despite its
complexity; periodic legislative debates about simplification
have not produced reform.

#### Major outstanding empirical work

This profile would benefit from:

- 2020 election outcome data: invalid-vote rates by municipality
  size; share of seats won by *Wählergruppen*; share of seats
  won where the list-mark default produced the seat (Listenkreuz)
  vs. cumulated/panachaged voting.
- A 2026 follow-up after the next regular election.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # GLKrWG Art. 1 + EU citizens
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant   # GLKrWG Art. 18
direct_suffrage:       compliant
periodic_elections:    compliant   # 6-year term per GO Art. 31
fundamental_rights:    compliant
regulatory_stability:  high        # GLKrWG amended infrequently;
                                   # last major reform 2018 (formula)
                                   # and 2023 (technical amendments)
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| Single-district at-large municipality | **Universal** | Most US municipalities already use this geometry; Bavaria's contribution is the ballot/allocation overlay. |
| Sainte-Laguë / Webster allocation | **Universal** | Webster is already the US House apportionment formula. |
| Cumulation (up to 3 votes per candidate) | **Universal** | US precedents in TX and AL local jurisdictions establish constitutional tractability. |
| Panachage | **Hybrid** | The substantive logic (cross-list voting) is universal; specific implementation interacts with US anti-fusion law and ballot-uniformity statutes. |
| Pure preference voting within lists (Art. 36) | **Universal** | Clean drafting solution to closed-list-disempowerment criticism. |
| Residual definition of *Wählergruppe* (Art. 24(1)) | **Universal** | The legal-drafting move — define the non-party list residually rather than enumerate categories — is portable to any non-partisan local charter. |
| In-person municipal-office signature collection (Art. 28) | **Particular** | Reflects German administrative-law tradition and *Verwaltungsgerichtsbarkeit*; less well-suited to US administrative environment. |
| Population-tiered assembly size (GO Art. 31) | **Hybrid** | Substantively universal (avoids the political fight over council size); procedurally embedded in Bavaria's constitutional and municipal structure. |
| 2018 switch from Hare-Niemeyer to Sainte-Laguë | **Universal** | Demonstrates that formula choice is a politically tractable ordinary-legislation question, not a constitutional one. |

### Top three takeaways for US state/local implementation

1. **Define the non-party list residually.** Art. 24(1) sentence
   2 — "voter groupings are all other associations or groups of
   natural persons whose purpose is to participate in elections"
   — is the most directly importable single sentence in the
   project's comparative set. A US local charter implementing
   non-partisan list PR can adopt this definitional approach
   without statutory enumeration of permissible categories.

2. **Pair high-magnitude single-district structure with
   open-list ballot mechanics.** The Bavarian recipe — assembly
   size set by population tier, single municipal district,
   open-list with cumulation, Sainte-Laguë allocation — is the
   project's clearest worked example of the primer's central
   thesis (pp. 5–8) that the right combination of Components 1, 2,
   and 3 transforms a previously winner-take-all at-large
   structure into a proportional one.

3. **Treat formula choice as ordinary legislation, but write it
   procedurally.** Bavaria's switch from D'Hondt (pre-2010) →
   Hare-Niemeyer (2014) → Sainte-Laguë (2018) demonstrates that
   formula choice is reversible and not constitutionally locked.
   Art. 35(2) writes the Sainte-Laguë procedure out — "by 1, 3,
   5, 7, 9 and so on" — without using the eponym. US drafting
   should follow this pattern: the calculation should be
   reproducible from the statutory text alone.

---

## 8. Sources

### Primary

- *Gemeinde- und Landkreiswahlgesetz* (GLKrWG) in der Fassung der
  Bekanntmachung vom 7. November 2006 (GVBl. S. 834), zuletzt
  geändert durch § 1 des Gesetzes vom 24. Juli 2023 (GVBl. S.
  385). BayRS 2021-1/2-I.
  <https://www.gesetze-bayern.de/Content/Document/BayGLKrWG/true>
- *Gemeinde- und Landkreiswahlordnung* (GLKrWO), 7. November
  2006 (GVBl. S. 852).
  <https://www.gesetze-bayern.de/Content/Document/BayGLKrWO/true>
- *Bayerische Gemeindeordnung* (GO) Art. 17, Art. 31.
  <https://www.gesetze-bayern.de/Content/Document/BayGO>
- *Bayerische Landkreisordnung* (LKrO).
- *Bayerische Verfassung* (BV) Art. 11(2).

### Synopses (Bavarian Ministry of the Interior)

- *Synopse Gemeinde- und Landkreiswahlgesetz* (GLKrWG), 28
  August 2023 (V10.1):
  <https://www.stmi.bayern.de/media/03_wahlen-und-abstimmungen/PDFs/synopse_glkrwg.pdf>
- *Synopse Gemeinde- und Landkreiswahlordnung* (GLKrWO),
  15 November 2024:
  <https://www.stmi.bayern.de/media/03_wahlen-und-abstimmungen/PDFs/glkrwo-synopse-2024.pdf>

### Secondary

- *Kommunalwahlrecht (Bayern)* — Wikipedia summary (orientation
  only).
- Bavarian Ministry of the Interior portal:
  <https://www.stmi.bayern.de/wahlen-und-abstimmungen/kommunalwahlen/>
- *Wahlrecht.de — Kommunalwahlsystem in Bayern*:
  <https://www.wahlrecht.de/kommunal/bayern.html>

### Outstanding gaps

The following remain to be retrieved or developed:

- Verbatim text of GLKrWG Art. 25 (Inhalt und Form der
  Wahlvorschläge), Art. 28 (Eintragung in Unterstützungslisten),
  Art. 32 (Zulassung der Wahlvorschläge), Art. 50, 51, 51a
  (Wahlprüfung, Wahlanfechtung, Rechtsweg).
- Verbatim text of GLKrWO §§ 38–40 (ballot specifications), §§
  75–87 (counting and result determination).
- 2020 Bavarian local election outcome data: share of seats won
  by Wählergruppen; invalid-vote rates by municipality size.
- BayVerfGH (Bavarian Constitutional Court) decisions on
  electoral matters, especially on signature requirements and
  equal treatment of Wählergruppen.
- Worked example using actual 2020 results for one
  municipality (preferred: Munich; alternatively: Augsburg as a
  mid-size contrast).
- Cache local PDFs of the Bavarian Ministry synopses to
  `sources/germany/bavaria/`.

### Resolved in iterations to date

**2026-05-05** (initial profile):
- GO Art. 31 quoted in Component 1 (assembly size table).
- GLKrWG Art. 11 noted in Component 1 (single-district
  municipality).
- GLKrWG Art. 16 noted in Component 2 (ballot papers).
- GLKrWG Art. 24, 27 quoted in Connected Area B.
- GLKrWG Art. 28 noted (in-person signature mechanism).
- GLKrWG Art. 34 quoted in Component 2 (cumulation, panachage,
  Listenkreuz).
- GLKrWG Art. 35 quoted in Component 3 (Sainte-Laguë formula).
- GLKrWG Art. 36 quoted in Component 3 (intra-list
  pure-preference rule).
- GLKrWG Art. 50, 51, 51a noted in Connected Area E.
- 2018 reform trajectory (D'Hondt → Hare-Niemeyer → Sainte-
  Laguë) documented.
