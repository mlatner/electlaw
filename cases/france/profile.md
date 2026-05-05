# France — case overview

France is a working comparator for two distinct propositions
relevant to U.S. PR adoption:

1. **A country with national plurality elections can operate
   list PR at the local level** without producing systemic
   incoherence. France elects its National Assembly by
   two-round single-member plurality, but elects its municipal
   councils (in communes of 1,000+ residents) by list PR with
   majority bonus. The two regimes coexist.
2. **The "majority bonus" (prime majoritaire) is a statutorily
   explicit drafting choice** for communities that prioritize
   governance stability. The list finishing first receives 50%
   of seats automatically (or 25% in Paris, Lyon, and
   Marseille post-2025); the remaining seats are allocated
   proportionally. This is structurally different from the
   project's other PR cases, which allocate all seats by formula
   without a bonus.

**Important framing correction.** French municipal lists are
**closed and gender-paritarian** (alternating male / female),
not open. Voters cast a single mark for a list; they cannot
reorder candidates within the list, cumulate, or panachage. The
"majority bonus + proportional remainder" structure is **list
PR with bonus**, not open-list PR. Drafters considering the
French model for U.S. adoption should not expect intra-list
voter agency in the Bavarian, Brazilian, Dutch, or Flemish
sense.

## Sub-profiles

- **`general_local_profile.md`** *(integrated below in this
  overview document)* — the regime for communes of 1,000+
  inhabitants under the Code Électoral.
- **`plm_profile.md`** — the **special regime** for Paris,
  Lyon, and Marseille under the *Loi PLM* (Loi n° 82-1169 du
  31 décembre 1982), as substantially reformed by **Loi n°
  2025-795 du 11 août 2025** which took effect for the **15
  and 22 March 2026** municipal elections.

## The general regime — communes ≥ 1,000 inhabitants

For communes of 1,000+ residents, French municipal elections
operate under Code Électoral Articles L. 260 to L. 273. Key
features:

### Component 1 — Council size

Council size is set by Code Électoral Article L. 2121-2 (in
the Code général des collectivités territoriales) on a
population-tiered table:

| Population | Council size |
|---|---:|
| 100 to 499 | 7 |
| 500 to 1,499 | 11 |
| 1,500 to 2,499 | 15 |
| 2,500 to 3,499 | 19 |
| 3,500 to 4,999 | 23 |
| 5,000 to 9,999 | 27 |
| 10,000 to 19,999 | 29 |
| 20,000 to 29,999 | 33 |
| 30,000 to 39,999 | 35 |
| 40,000 to 49,999 | 39 |
| 50,000 to 59,999 | 43 |
| 60,000 to 79,999 | 45 |
| 80,000 to 99,999 | 49 |
| 100,000 to 149,999 | 53 |
| 150,000 to 199,999 | 55 |
| 200,000 to 249,999 | 59 |
| 250,000 to 299,999 | 61 |
| 300,000 and above | 65 |

(Plus Paris, Lyon, Marseille — see PLM profile.)

Each commune is a single electoral district (no sub-municipal
wards in the general regime).

### Component 2 — Ballot structure

Closed list with strict parity alternation (alternating male and
female candidates throughout the list). Voters cast a single
mark for a list. No intra-list reordering, cumulation, or
panachage.

The submitter-set list order binds, subject to the parity
requirement.

### Component 3 — Allocation formula (Code Électoral Art. L. 262)

The architectural keystone:

> Au premier tour de scrutin, il est attribué à la liste qui a
> recueilli la majorité absolue des suffrages exprimés un
> nombre de sièges égal à la moitié du nombre des sièges à
> pourvoir, arrondi à l'entier supérieur lorsqu'il y a plus de
> quatre sièges à pourvoir et à l'entier inférieur lorsqu'il y
> en a moins de quatre.
>
> Cette attribution opérée, les autres sièges sont répartis
> entre toutes les listes à la représentation proportionnelle
> suivant la règle de la plus forte moyenne, sous réserve de
> l'application des dispositions du troisième alinéa ci-après.
>
> Les listes qui n'ont pas obtenu au moins 5 % des suffrages
> exprimés ne sont pas admises à la répartition des sièges.

(Translation: At the first round, the list that received an
absolute majority of expressed suffrages is awarded a number
of seats equal to half the seats to fill, rounded up where more
than four seats are to be filled and rounded down where fewer
than four are to be filled. After this attribution, the
remaining seats are distributed among all lists by proportional
representation under the highest-averages rule. Lists that have
not obtained at least 5% of expressed suffrages are not
admitted to the distribution of seats.)

The procedure:

1. **First round, majority bonus**: if a list wins an absolute
   majority, it receives **50%** of the seats (rounded up for
   councils ≥ 5 seats, down for smaller). Remaining seats
   distributed proportionally by **plus forte moyenne**
   (highest averages, mathematically D'Hondt).
2. **5% threshold**: lists below 5% are excluded from
   proportional distribution.
3. **Second round qualification**: if no list wins the absolute
   majority in round one, only lists receiving **10% of valid
   votes** in round one may proceed to round two.
4. **Second round**: same allocation rules; the list finishing
   first wins the majority bonus.

### Operationalized values (general regime)

```
total_seats:                     7 (smallest, M < 500 inhab.) —
                                 65 (M ≥ 300,000 inhab.,
                                 non-PLM); plus PLM-specific
                                 sizes
codification_instrument:         Code général des collectivités
                                 territoriales (council size);
                                 Code Électoral (election rules)

ballot_type:                     closed_list_with_parity_
                                 alternation
preference_votes_per_voter:      one mark for one list;
                                 intra-list ordering binding
panachage_allowed:               no (since 2014 reform; small-
                                 commune regime under 1,000
                                 inhab. retains some panachage)

allocation_formula:              hybrid:
                                 (1) 50% majority bonus to
                                     leading list (Art. L. 262)
                                 (2) Highest averages
                                     (D'Hondt, "plus forte
                                     moyenne") for remaining
                                     50%
formula_codified_as:             named ("plus forte moyenne")
                                 + procedural majority bonus
formula_statutory_citation:      Code Électoral Art. L. 262
ties_rule:                       oldest candidate as tie-breaker
                                 (Art. L. 262)

legal_threshold_pct:             5 (proportional distribution);
                                 10 (second-round
                                 qualification)

apparentement_allowed:           between rounds: lists that
                                 qualified for round two may
                                 fuse (*fusion de listes*) with
                                 lists that obtained at least
                                 5% in round one
intra_list_rule:                 list_order (closed list,
                                 binding)
gender_quota:                    50% (parity alternation
                                 throughout the list)
```

### Notes — France general regime

**The fusion-de-listes mechanism between rounds** is a
distinctive French feature. A list that qualifies for round two
(10%+ in round one) may merge with one or more lists that
received at least 5% in round one but did not themselves
qualify. The merged list runs in round two; the smaller list's
candidates are integrated into the merged list's order. This
is functionally a between-rounds apparentement and is the
French answer to coalition formation in proportional contests.

**For U.S. drafters**: the French general regime is the
project's working example of **list PR with majority bonus** —
a design choice U.S. PR-reform proposals have not generally
considered but which European drafters use to ensure governance
stability at the cost of strict proportionality. The 50% bonus
substantially advantages the leading list; this is intentional.
A U.S. analog could tune the bonus parameter (25% as in PLM,
50% as in general regime) according to the desired stability /
proportionality trade-off.

The fusion-de-listes mechanism is portable as a between-rounds
coalition-formation device, with the caveat that U.S. local
elections do not generally use two-round structures.

## Cross-cutting research questions for the France case

1. How does the majority bonus interact with the 5% threshold to
   produce final seat distributions in practice? What is the
   typical seat share for the leading list under the general
   regime?
2. The PLM regime's reduced 25% bonus (vs 50% general) — what
   does the March 2026 first cycle suggest about whether the
   smaller bonus produces different coalition dynamics?
3. Has the absence of intra-list voter agency (closed list with
   parity) produced documented voter-engagement effects?
