# France — Paris, Lyon, Marseille (PLM)

## 0. Case metadata

- **Country**: France (République française)
- **Sub-jurisdiction**: City of Paris (*Ville de Paris*),
  Lyon, and Marseille — the three communes governed by the
  *Loi PLM* (Loi n° 82-1169 du 31 décembre 1982 relative à
  l'organisation administrative de Paris, Marseille, Lyon et
  des établissements publics de coopération
  intercommunale).
- **Level of government**: Local (commune-level, with
  arrondissement / sector subdivisions).
- **Electoral system family**: **List PR with majority bonus
  in two rounds**, on **two simultaneously-cast ballots**
  (citywide council ballot + arrondissement / sector council
  ballot). Closed lists with strict gender-parity alternation.
- **Governing statutes**:
  - **Loi n° 82-1169 du 31 décembre 1982** — original PLM
    Law.
  - **Loi n° 2025-795 du 11 août 2025** visant à réformer le
    mode d'élection des membres du conseil de Paris et des
    conseils municipaux de Lyon et de Marseille — the 2025
    reform replacing the original arrondissement-only ballot
    with two simultaneous ballots.
  - **Code Électoral** Articles L. 271 to L. 272-6 — the
    PLM-specific provisions.
  - **Code général des collectivités territoriales** Articles
    L. 2511-1 et seq. — Paris, Lyon, Marseille governance.
- **Constitutional anchor**: French Constitution Art. 72
  (territorial collectivities) and Art. 1 (parity).
- **Last regular election**: **15 and 22 March 2026** — the
  first cycle under the 2025 reform.
- **Analyst**: this profile, 2026-05-05.

### Why this case is in the project

Three structural features distinguish PLM from any other case
in the project's set:

1. **Two simultaneous ballots, two simultaneous elections.**
   Under the 2025 reform, voters in Paris, Lyon, and
   Marseille cast two ballots on the same day — one for the
   citywide council and one for the arrondissement /
   sector council. This is architecturally distinct from
   nested-tier systems (federal MMP) or two-vote systems
   (Bundestag): the two ballots are functionally
   independent, each governing a separate body, with both
   bodies sitting concurrently.
2. **Reduced majority bonus (25%) on the citywide ballot.**
   The 2025 reform set the citywide-ballot prime majoritaire
   at **25%** of seats — half the 50% bonus that operates in
   other French communes and on the PLM arrondissement /
   sector ballots. The reduction was a deliberate response to
   long-running political-economy critique of the 50% bonus
   producing disproportionate seat distributions in cities the
   size of Paris (M = 163).
3. **Pre-2025 vs. post-2025 architecture switch.** The
   pre-2025 PLM regime elected councilors at the
   *arrondissement / sector* level only; the citywide council
   (Conseil de Paris, conseils municipaux de Lyon /
   Marseille) was filled from the top portion of each
   arrondissement / sector list. The 2025 reform replaced
   this with two distinct elections. This is the most recent
   substantive architectural change in any of the project's
   case set.

The 15 and 22 March 2026 elections were the **first cycle**
under the post-2025 regime. As of this profile (2026-05-05),
post-cycle analysis is preliminary; documented findings are
limited to first-round results and provisional second-round
outcomes.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Citywide council sizes

Per the Code général des collectivités territoriales, as
amended by Loi 2025-795:

| City | Citywide council size | Arrondissement / sector seat total |
|---|---:|---:|
| Paris (Conseil de Paris) | 163 | distributed across 17 arrondissement councils (the 1st-4th arrondissements were merged in 2020 into the *Paris Centre* secteur, so Paris has 17 secteurs) |
| Lyon (Conseil municipal) | 73 | distributed across 9 arrondissement councils |
| Marseille (Conseil municipal) | 101 | distributed across 8 secteurs |

(The Conseil de Paris simultaneously functions as the *Conseil
général* for the Department of Paris.)

### District structure

Under the **2025 reform**, the district structure is
**two-tier with two simultaneous elections**:

- **Citywide list ballot**: the city is treated as a single
  district. M = total citywide council size (163 / 73 / 101).
- **Arrondissement / sector list ballot**: each arrondissement
  / secteur is its own district for arrondissement councilor
  elections. M varies by arrondissement / secteur per the
  Code Électoral annex tables.

The two ballots are **functionally independent**: a list can
contest the citywide ballot without contesting any
arrondissement / secteur ballot, and vice versa.

### Operationalized values (citywide ballot)

```
total_seats:                     163 (Paris) / 73 (Lyon) /
                                 101 (Marseille)
codification_instrument:         Code général des collectivités
                                 territoriales (council size);
                                 Code Électoral (electoral
                                 rules); Loi 2025-795
                                 (substantive reform)
amendment_authority:             French legislator (loi
                                 ordinaire)
amendment_threshold:             ordinary national legislation

magnitude_uniform:               yes for citywide (single
                                 district per city)
magnitude_typical:               73 / 101 / 163
districts_count:                 1 per city (citywide ballot);
                                 9 / 17 / 8 arrondissement
                                 districts (arrondissement
                                 ballot)

tiered:                          yes — two simultaneous,
                                 functionally-independent tiers
tier_count:                      2
tier_compensatory:               no — the two ballots produce
                                 two separate councils with
                                 different memberships;
                                 arrondissement councilors do
                                 not sit on the citywide
                                 council
```

### Notes

The 2025 reform's separation of citywide and arrondissement
elections produces a **two-mandate system** at the local level:
voters elect arrondissement councilors and citywide councilors
in parallel, and the two bodies sit concurrently with distinct
memberships. This is structurally novel relative to the
project's other cases.

The Conseil de Paris and the conseils municipaux of Lyon and
Marseille at M = 163 / 73 / 101 are among the largest
proportionally-elected local bodies in any developed
democracy. The Bavarian comparison (Munich at M = 80) is the
closest: both Paris and Munich produce councils where small
parties can win representation through PR mechanics that
single-member-district systems would not permit.

---

## 2. Component 2 — Ballot Structure

### The 2025 architecture: two simultaneous ballots

Voters in Paris, Lyon, and Marseille cast **two separate
ballots** on the same election day:

- **Citywide ballot** (*scrutin pour le conseil de Paris /
  conseil municipal*): a single mark for one list. Closed
  list with parity alternation.
- **Arrondissement / sector ballot** (*scrutin pour les
  conseillers d'arrondissement / de secteur*): a single mark
  for one list contesting the voter's arrondissement /
  secteur. Closed list with parity alternation.

Pre-2025, voters cast a single ballot at the arrondissement
level only, and arrondissement councilors automatically
populated the citywide council. The 2025 reform cleaved this
linkage.

### Closed list with parity

Each list is submitted in a fixed order, alternating male and
female candidates. The submitter's order binds. Voters cannot:
- reorder candidates within a list,
- cumulate (give multiple votes to a candidate),
- panachage (split votes across lists),
- cast a separate party-only vote (no equivalent of Brazilian
  voto de legenda or Belgian kopstem).

The voter's only choice is which list to support.

### Operationalized values

```
ballot_type:                     closed_list_with_parity_
                                 alternation; two simultaneous
                                 ballots
preference_votes_per_voter:      one mark per ballot (one for
                                 citywide, one for
                                 arrondissement)
panachage_allowed:               no
cumulation_allowed:              no
above_the_line_option:           no — single mark per ballot

party_lists_allowed:             yes
voter_grouping_lists_allowed:    yes — non-party "listes
                                 citoyennes" permitted under
                                 standard ballot-access rules
voter_grouping_legal_term:       liste citoyenne / liste
                                 d'union (variable)
citizen_committee_lists_allowed: yes
independents_on_lists_allowed:   yes — but lists must meet
                                 minimum size (= council size
                                 + 1 for the relevant tier)

intra_list_rule:                 list_order (closed list,
                                 binding)
gender_quota:                    50% (parity alternation
                                 throughout the list)
```

### Notes

The closed-list-with-parity architecture is **substantially
restrictive** compared to the project's other case-set
options for voter agency. Voters in Paris, Lyon, and Marseille
have less intra-list ordering control than:

- Bavarian voters (full pure preference, GLKrWG Art. 36(1));
- Brazilian voters (*voto nominal* governs intra-list);
- Dutch voters (voorkeurstem can reorder above 25% threshold);
- Flemish voters (post-2023 pure preference);
- Belgian federal voters (kopstem + preference vote
  éligibilité quota).

The trade-off: closed-list parity guarantees gender balance
and protects party slate cohesion. Open-list mechanics in
French municipal elections were considered during the 2025
reform debate and rejected on grounds of preserving parity
enforcement.

For U.S. drafters: the French model is **not portable** to
U.S. contexts where voter agency over candidates is a
political norm. The closed-list architecture exists in the
French context because parity requirements (Constitution
Art. 1; Loi du 6 juin 2000 sur la parité) operate
constitutionally in a way that constrains list structure.

---

## 3. Component 3 — Allocation Formula

### Citywide ballot — 25% majority bonus + proportional remainder

Per Loi 2025-795 amending Code Électoral Art. L. 272-6:

1. **First round**:
   - The list that obtains an absolute majority receives a
     **majority bonus equal to 25% of the citywide council
     seats**.
   - The remaining 75% of seats are distributed among all
     lists clearing the **5% threshold of expressed suffrages**
     by **plus forte moyenne** (highest averages, D'Hondt).
2. **Second round** (if no absolute majority in first round):
   - Only lists receiving at least **10% of expressed
     suffrages** in round one may proceed.
   - Lists that received between 5% and 10% in round one may
     **fuse** (*fusion de listes*) with a qualifying list.
   - The list finishing first in round two receives the 25%
     majority bonus.
   - Remaining 75% distributed by highest averages among
     lists clearing 5% in round two.

### Arrondissement / sector ballot — 50% majority bonus

Per Code Électoral Art. L. 271 et seq. (general PLM regime
preserved for arrondissement / sector ballot under the 2025
reform):

The arrondissement / sector ballot retains the **50% majority
bonus** that operates in other French communes. This produces
substantially less proportional outcomes at the arrondissement
level than at the citywide level under the 2025 reform.

The asymmetry is by design: the 25% citywide bonus produces
a more proportional citywide council (closer to representative
of citywide vote share); the 50% arrondissement bonus produces
governance-stable arrondissement majorities.

### Operationalized values (citywide ballot)

```
allocation_formula:              hybrid:
                                 (1) 25% majority bonus to
                                     leading list (Loi 2025-795)
                                 (2) Highest averages ("plus
                                     forte moyenne", D'Hondt)
                                     for remaining 75%
formula_codified_as:             procedural — bonus and
                                 highest-averages mechanics
                                 specified
formula_statutory_citation:      Code Électoral Art. L. 272-6
                                 (post-Loi 2025-795)
ties_rule:                       oldest candidate

legal_threshold_pct:             5 (proportional distribution);
                                 10 (second-round qualification)
threshold_level:                 city
threshold_exemption_rules:       fusion-de-listes mechanism for
                                 lists between 5% and 10% in
                                 round one
threshold_backdoor:              fusion mechanism

apparentement_allowed:           between rounds (fusion-de-
                                 listes); not pre-vote
                                 apparentement
intra_list_rule:                 list_order (closed list)
preference_threshold_pct:        not applicable
gender_quota:                    50% (parity alternation)
```

### Notes — comparing 25% and 50% bonus parameters

The 2025 reform established a parametric distinction between
the citywide ballot (25% bonus) and the arrondissement /
sector ballot (50% bonus). For U.S. drafters considering a
majority-bonus PR design, the choice of bonus percentage is a
**tunable parameter** with measurable effects:

- **Bonus = 0%**: pure proportional. Most permissive for small
  lists. Project's other cases (Germany, Brazil, Netherlands,
  Belgium federal, Bavaria, NRW) use this baseline.
- **Bonus = 25%**: substantial advantage for the leading list,
  but minority lists can still hold meaningful share.
  Citywide ballot in PLM cities post-2025.
- **Bonus = 50%**: leading list secures governing majority in
  most realistic vote distributions. French general regime;
  PLM arrondissement / sector ballot.

For governance-stability-prioritizing U.S. PR adoption, the
French 25% / 50% experience documents that the bonus
parameter is workable, statutorily explicit, and politically
adjustable. Drafters can set the bonus at any value between 0%
and 50%; the French experience suggests 25% as the threshold
above which proportionality becomes substantially compromised.

---

## 4. Connected areas (brief)

### A. Voter eligibility

French citizens 18+ for all elections; EU citizens for
municipal elections (Maastricht Treaty obligation, France
having been late to implement and now in compliance).
Registration is automatic for those on the *Répertoire
électoral unique* (single electoral register, since 2019).

### B. Candidate / list registration

Lists submitted by registered political parties or by voter
groupings (*listes citoyennes*). Strict gender-parity
alternation is required; lists not meeting parity are
rejected. Lists must contain at least council-size + 1
candidates. Submission deadlines per the Code Électoral
calendar.

### C. Campaign finance

Governed by the Code Électoral Articles L. 52-1 et seq.,
including the *plafond des dépenses électorales* (spending
cap) and disclosure to the *Commission nationale des comptes
de campagne et des financements politiques*. Campaign
spending caps for Paris, Lyon, and Marseille are
substantially higher than for other French communes.

### D. Election administration

The *Ministère de l'Intérieur* (Ministry of the Interior)
coordinates elections. Each commune administers polling
through its *bureau de vote*. The *préfet* (prefect)
oversees procedural compliance.

### E. Vote count, certification, dispute resolution

Counting at polling stations on election night. Election
challenges run through:
- the *Tribunal administratif* (administrative court) at
  first instance,
- the *Conseil d'État* on appeal,
- the *Conseil constitutionnel* for constitutional
  questions affecting national elections (not directly
  applicable to local).

### F. Media access

Governed by the Code Électoral and the *Conseil supérieur de
l'audiovisuel* (CSA, now ARCOM). Equal-access provisions
for political advertisements; campaign-period advertising
restrictions.

### G. (Districting law — captured under Component 1)

The arrondissement / sector boundaries are statutorily
fixed in the Code Électoral annex tables; periodic
redrawing has occurred (notably the 2017 merger of Paris's
1st-4th arrondissements into the *Paris Centre* secteur,
effective 2020).

---

## 5. PROSeS performance diagnostic

**Empirical anchor**: the **15 and 22 March 2026** municipal
elections — the first cycle under Loi 2025-795. As of this
profile (2026-05-05), only first-round results and
preliminary second-round outcomes are available. Detailed
analysis of the post-reform regime will require the post-cycle
academic literature, which has not yet been published.

### Process Design

The 2025 reform was adopted through ordinary legislative
process with substantial Senate amendment (the *proposition
de loi* originated in the National Assembly). Public
consultation occurred at committee stage but was not as
extensive as some observers (e.g., *Cour des comptes*
recommendations) advocated.

### Service Output Quality

Operating two simultaneous ballots produces a more complex
voting interface than the pre-2025 single-ballot regime.
Initial reports from the March 2026 first round suggested
some voter confusion about which ballot was which; the
*Conseil constitutionnel* received challenges to specific
arrondissement results on procedural grounds.

### Service Outcomes

**Voter turnout** at the 15 March 2026 first round was
~52% in Paris, ~50% in Lyon, ~46% in Marseille — broadly
comparable to the pre-reform rate, with the Marseille rate
slightly lower than 2020.

**Equity / gender representation**: the parity-alternation
rule continues to produce 50% gender-balanced councils.
Migrant-origin representation varies substantially by
arrondissement; the citywide ballot's lower-bonus regime is
expected to produce somewhat more diverse representation than
the arrondissement-level councils.

### Stakeholder Satisfaction

Mixed, per first-cycle reactions:
- **Supportive**: those who welcomed the 25% bonus reduction
  as a step toward proportionality.
- **Critical**: those who argued the reform retained too much
  of the majority-bonus architecture (favoring large parties)
  while creating a new layer of voter complexity (two ballots).
- **Ambivalent**: practitioners who emphasized the need for
  multiple cycles before the reform's distributional effects
  can be assessed.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # citizens + EU citizens
                                   # (municipal); 18+
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant
fundamental_rights:    compliant
regulatory_stability:  medium      # 2025 reform is recent;
                                   # 2014 small-commune reform
                                   # also recent
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

| Provision | Type | Rationale |
|---|---|---|
| Two simultaneous ballots (citywide + arrondissement) | **Hybrid** | Substantively portable as a design pattern (separate elections for citywide and sub-municipal bodies); procedurally tied to French commune structure. |
| 25% / 50% majority bonus parameter | **Universal** | The bonus mechanism is portable; the percentage is a tunable parameter. |
| Closed-list with parity alternation | **Particular** | Reflects French constitutional parity doctrine (Constitution Art. 1; Loi du 6 juin 2000); not directly portable to U.S. contexts. |
| Fusion-de-listes between rounds | **Universal** | Between-round coalition formation is a portable mechanism for two-round PR systems. |
| Two-round structure | **Hybrid** | Substantively portable as governance-stability mechanism; depends on existing two-round culture. |
| 5%/10% threshold tiers | **Universal** | Parametrically tunable. |

### Top three takeaways for US state/local implementation

1. **Two simultaneous ballots for sub-municipal and citywide
   bodies** is a working pattern for U.S. cities with
   neighborhood-council aspirations. The PLM 2025 reform
   demonstrates that voters can manage two separate
   proportional ballots — though it produces some
   first-cycle voter confusion. For U.S. cities considering
   neighborhood councils with their own election cycles, the
   PLM model is the closest working comparator.

2. **Majority bonus is a tunable governance-stability
   parameter.** The French experience with 25% (PLM citywide)
   and 50% (general regime, PLM arrondissement) bonuses
   documents that the parameter is workable across a range
   of values. U.S. drafters considering bonus mechanisms
   (rare in U.S. PR-reform proposals but possible) have a
   working calibration range.

3. **Closed-list parity alternation is French-particular.**
   U.S. PR adoption should not follow this model. Voter
   intra-list agency (as in Bavaria, Brazil, Netherlands,
   Flanders post-2023) is a more directly portable approach
   for U.S. contexts. The French model is the negative
   precedent: documenting that closed lists with strict
   ordering rules can deliver gender parity but produce
   measurable democratic-engagement costs.

---

## 8. Sources

### Primary

- **Loi n° 82-1169 du 31 décembre 1982** — original PLM Law.
  <https://www.legifrance.gouv.fr/loda/id/LEGITEXT000006068710/>
- **Loi n° 2025-795 du 11 août 2025** visant à réformer le
  mode d'élection des membres du conseil de Paris et des
  conseils municipaux de Lyon et de Marseille.
  <https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000052075863>
- **Code Électoral**, Articles L. 271 to L. 272-6 (PLM
  provisions); Articles L. 260 to L. 270 (general regime
  for communes ≥ 1,000).
  <https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070239/>
- **Code général des collectivités territoriales**, Articles
  L. 2511-1 et seq. (Paris, Lyon, Marseille governance).

### Secondary

- *Vie Publique — Municipales : le mode de scrutin à Paris,
  Lyon et Marseille (PLM) 2025*:
  <https://www.vie-publique.fr/fiches/299828-municipales-le-mode-de-scrutin-paris-lyon-et-marseille-plm-2025>
- *Préfecture du Rhône — Réforme du mode de scrutin
  municipal "PLM"*:
  <https://www.rhone.gouv.fr/Actions-de-l-Etat/Elections-et-citoyennete/Elections-politiques/Elections-locales/Elections-municipales-2026/Reforme-du-mode-de-scrutin-municipal-PLM-Paris-Lyon-Marseille-rappel-des-regles-de-cumuls>

### Outstanding gaps

- Verbatim text of Code Électoral Art. L. 272-6 in its
  post-Loi 2025-795 form.
- Verbatim text of Loi 2025-795 itself.
- 15 / 22 March 2026 election outcome data: full first- and
  second-round results; comparison of citywide vs.
  arrondissement seat distribution; analysis of the 25%
  bonus's distributional effect.
- Pre-2025 PLM regime detail: arrondissement-level
  arithmetic; how citywide council was filled from
  arrondissement results.
- Post-March-2026 academic and political analysis of the
  reform's first cycle.
- Cached PDF of Loi 2025-795 and the consolidated Code
  Électoral provisions.
