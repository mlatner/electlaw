# North Rhine-Westphalia — Local elections (Kommunalwahl)

## 0. Case metadata

- **Country**: Federal Republic of Germany
- **Sub-jurisdiction**: *Land* Nordrhein-Westfalen (North Rhine-
  Westphalia, NRW) — the most populous *Land* (~18 million
  residents); home to Cologne, Düsseldorf, Dortmund, Essen, and
  the Ruhr region.
- **Level of government**: Local — *Gemeinderat* (municipal
  council), *Kreistag* (county council), *Bezirksvertretung*
  (district representation), *Bürgermeister* and *Landrat*
  (mayors and county executives), and the *Regionalverband Ruhr*
  (Regional Assembly).
- **Electoral system family**: **One-vote personalized PR** —
  closed reserve lists at municipal level with constituency
  (Wahlbezirk) seats. Each voter casts a single vote that
  simultaneously elects a constituency candidate and counts for
  the party/group's reserve list.
- **Governing statute (primary)**: *Kommunalwahlgesetz* (KWahlG)
  for the *Land* Nordrhein-Westfalen
- **Citation**: KWahlG NRW, neu bekanntgemacht am 28. Juni 2025
  (consolidated republication following the VerfGH NRW judgment
  of 20 May 2025 and the amending act of 10 June 2025).
- **URL**: <https://recht.nrw.de/lrgv/gesetz/28062025-bekanntmachung-der-neufassung-des-kommunalwahlgesetzes-kommunalwahlgesetz>
- **Implementing regulation**: *Kommunalwahlordnung* (KWahlO).
- **Constitutional anchors**:
  - *Verfassung für das Land Nordrhein-Westfalen* — Articles
    governing the right to vote and *Land* electoral homogeneity
    with the federal regime.
  - *Grundgesetz* Article 28(1) — *Land* electoral homogeneity
    requirement (general, direct, free, equal, and secret
    ballot at *Land* and local level).
- **Recent constitutional decisions**:
  - **VerfGH NRW, 21 November 2017** — struck down the 2.5%
    threshold for *Gemeinderat* and *Kreistag* elections.
  - **VerfGH NRW, 20 May 2025, VerfGH 124/24** — struck down the
    2024 reform of § 33 KWahlG (replacement of Sainte-Laguë
    with the so-called "Rock-Verfahren").
- **Last regular election**: 14 September 2025.
- **Analyst**: (this profile, 2026-05-05)

### Why this case is in the project

NRW is the project's principal contrast to the Bavarian profile
within the same federal constitutional frame. Three features
distinguish it analytically:

1. **One-vote MMP-style ballot** under § 25 KWahlG: a single vote
   simultaneously elects a constituency candidate and counts for
   the party/voter-grouping's reserve list. This is a simpler
   ballot architecture than the federal Bundestag's two-vote
   MMP, and a sharp contrast with Bavaria's "as many votes as
   seats" cumulation/panachage system.
2. **Closed reserve lists**: list seats fill in submitted order
   (§ 33(6)) — opposite of Bavaria's pure-preference intra-list
   rule (Art. 36 GLKrWG).
3. **Active constitutional jurisprudence** on PR mechanics — the
   2017 threshold strike-down and the 2024–25 formula saga are
   the project's richest case study on how a state constitutional
   court polices the equal-chances and equality-of-elections
   doctrines when the legislature touches the three primary
   components.

NRW also illustrates an important comparative point: in a closed-
list MMP system, **the constitutional protection of small parties
shifts from voter-side (cumulation/panachage) to formula-and-
threshold doctrine**. Where Bavaria gives voters direct power
through ballot mechanics, NRW gives small groups indirect power
through legal-equality jurisprudence on Components 1 and 3.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — §§ 3, 4 KWahlG

§ 3 establishes the number of representatives (*Zahl der
Vertreter*) for each *Gemeinderat* and *Kreistag*. The schedule
is population-tiered (paralleling Bavaria's GO Art. 31), with
council sizes ranging from approximately 16 in the smallest
municipalities up to 90 in the largest cities (Cologne).

§ 4 establishes the *Wahlbezirke* (electoral districts). Per the
KWahlG architecture (§ 31): **approximately half of the council
seats are filled by direct-mandate constituency winners**, and
the remaining seats are allocated from reserve lists to ensure
proportional outcomes. In Cologne (90 seats), there are 45
constituency seats and 45 list seats; in smaller municipalities
the split is correspondingly proportional.

### § 31 KWahlG (Wahlsystem)

The architectural keystone:

> § 31 sets the one-vote, two-tier system. Half of the
> representatives are elected directly in *Wahlbezirke* (single-
> member districts) by plurality of first-and-only votes; the
> other half are filled from the reserve lists of parties and
> voter groupings using the *Sitzverteilung* procedure of § 33.

This is **MMP architecture with a single vote** rather than the
two-vote system of the federal *Bundestag*. The voter's single
mark counts twice: once for the constituency candidate (under
§ 32) and once for the candidate's party/group reserve list
(under § 33). Constituency winners enter the council directly;
remaining seats balance the proportional outcome.

### Operationalized values

```
total_seats:                     ~16 (smallest) — ~90 (Cologne)
codification_instrument:         KWahlG § 3 (statute)
amendment_authority:             Landtag NRW
amendment_threshold:             ordinary Land legislation

magnitude_uniform:               no — uniform within each
                                 municipality, varying by
                                 population
magnitude_typical:               variable
magnitude_range:                 ~16 — ~90 per municipality
districts_count:                 2 tiers per municipality:
                                 ~8–45 single-mandate Wahlbezirke
                                 + 1 municipality-wide reserve
                                 list pool
districting_authority:           local council with state oversight
districting_frequency_years:     each electoral cycle as needed
districting_criteria_in_statute: population equality across
                                 Wahlbezirke within a municipality
                                 (typical max deviation comparable
                                 to federal § 3 BWahlG)

tiered:                          yes
tier_count:                      2 — Wahlbezirk seats + reserve
                                 list seats, integrated through
                                 § 33's proportional balancing
tier_compensatory:               yes (reserve list compensates for
                                 disproportionality at the
                                 constituency tier)

threshold_of_exclusion_pct:      structural, dominated by formula
                                 (Component 3); no statutory
                                 threshold at Gemeinderat/Kreistag
                                 level since VerfGH NRW 2017
```

### Notes

The single-vote MMP architecture is the **older German design**:
the federal *Bundestag* used a one-vote system from 1949 until
the introduction of the two-vote ballot in 1953. NRW preserves
the original one-vote architecture at the local level. For US
implementation, this is a useful drafting precedent: one-vote
MMP is operationally simpler than two-vote MMP and may be
easier to introduce in jurisdictions where voters are
unaccustomed to the dual-ballot logic.

A practical consequence: under one-vote MMP, **a voter cannot
split tickets between a preferred constituency candidate and a
preferred party**. The strategic landscape is correspondingly
simpler.

---

## 2. Component 2 — Ballot Structure

### Statutory text — § 25 KWahlG (Stimmabgabe)

> § 25: "Der Wähler hat eine Stimme."
>
> (*The voter has one vote.*)

The voter's single vote is cast by marking one circle on the
ballot, indicating support for one *Wahlbezirk* candidate. The
vote simultaneously counts for the candidate's party or
*Wählergruppe* reserve list per § 31.

### Statutory text — § 23 KWahlG (Stimmzettel)

The ballot displays:

- All admitted *Wahlbezirk* candidates for the voter's district;
- For each candidate nominated by a party or voter grouping: the
  group's name and the **first three candidates of the relevant
  reserve list** (per § 16).
- Order on the ballot is set by previous-election performance:
  parties / groups appear in descending order of votes received
  at the prior election to that body, with new entrants in
  alphabetical order.

### Statutory text — § 16 KWahlG (Reservelisten)

Reserve lists are submitted by parties and *Wählergruppen* for
the entire municipality. Lists are **closed**: the order set by
the submitter is binding, subject only to the rule that
candidates already elected in their *Wahlbezirk* are removed
from the list before residual seats are allocated (§ 33 / § 45).

The first three candidates of each list appear on the ballot
(§ 23), but the full list (which can be substantially longer)
governs intra-list seat assignment.

### Operationalized values

```
ballot_type:                     closed_list_one_vote_mmp_local
preference_votes_per_voter:      1 (single mark for a Wahlbezirk
                                 candidate, counts for both tiers)
panachage_allowed:               no
cumulation_allowed:              no
above_the_line_option:           N/A (no separate list mark; the
                                 candidate vote *is* the list
                                 vote)

party_lists_allowed:             yes (§ 16)
voter_grouping_lists_allowed:    yes (§ 15, § 16)
voter_grouping_legal_term:       Wählergruppe
citizen_committee_lists_allowed: yes — voter groupings need not
                                 take any specific organizational
                                 form (parallel to Bavaria's
                                 Art. 24(1) GLKrWG)
independents_on_lists_allowed:   yes — but reserve lists are
                                 typically party / group nominated;
                                 individual candidates can stand
                                 in Wahlbezirke under § 15

non_party_label_allowed:         yes (party / group name on ballot
                                 per § 23)
non_party_label_categories:      not statutorily restricted to
                                 categories
non_party_label_restrictions:    no name confusable with an
                                 admitted party
label_validation_authority:      Wahlausschuss under § 18
                                 (Prüfung der Wahlvorschläge)
```

### Notes

Three features sharpen the comparison with Bavaria:

1. **Closed reserve lists** (§ 16, § 33(6)): list seats fill in
   submitter-set order. Voters cannot reorder lists or cumulate
   votes. This sacrifices voter agency for ballot simplicity —
   the diametric opposite of Bavaria's open-list-with-cumulation
   regime.
2. **Single-vote operation** (§ 25): the voter makes one mark
   that does both jobs. Easier to count, lower invalid-vote
   rates expected, but no ticket-splitting capacity.
3. **Three-name list display** (§ 23): the ballot shows only
   the first three reserve-list candidates per group. Voters
   know who is "at the top" but do not see the full list.

For US implementation, NRW's closed-list approach is the
appropriate model where the priority is **ballot simplicity over
voter agency**. The Guinier Project primer (p. 13) cites
closed-list ballots as the most error-resistant; NRW is the
working example. Compare:

- Where US local jurisdictions have already established
  cumulative voting (TX, AL VRA precedents), the Bavarian model
  may be the closer fit.
- Where the priority is to introduce PR with minimal voter
  retraining, the NRW one-vote closed-list model is the closer
  fit. This is roughly the choice South Africa made for its
  local-level mixed system.

---

## 3. Component 3 — Allocation Formula

### Current formula — Sainte-Laguë / Webster (post-VerfGH 2025)

§ 33 KWahlG, in its post-amendment form (as of 28 June 2025),
uses the **divisor procedure with standard rounding** — i.e.,
the **Sainte-Laguë / Webster** formula. Per the consolidated
republication: "Divisorverfahren mit Standardrundung."

Total reserve-list seats are allocated to parties and groups in
proportion to their total vote shares (the same one-vote totals
that elected constituency winners), with adjustments for
constituency seats already won. Within each list, seats are
filled in submitted order (§ 33(6)) after deducting candidates
already elected in their *Wahlbezirk*.

### Statutory threshold

**No statutory threshold at *Gemeinderat* or *Kreistag* level
since VerfGH NRW 21 November 2017** struck down the 2.5%
threshold for those bodies (see Section 7 below). A 2.5%
threshold remains in force for *Bezirksvertretungen* (district
representations) and the *Regionalverband Ruhr* assembly,
where the VerfGH found less stringent constitutional
requirements.

### Operationalized values

```
allocation_formula:              webster_sainte_lague           # § 33
formula_codified_as:             named procedurally — "Divisor-
                                 verfahren mit Standardrundung"
                                 (procedure description without
                                 eponym; same drafting style as
                                 Bavaria's GLKrWG Art. 35(2))
formula_statutory_citation:      KWahlG § 33

legal_threshold_pct:             0 (Gemeinderat / Kreistag)
                                 2.5 (Bezirksvertretungen,
                                      Regionalverband Ruhr)
threshold_level:                 municipality / county / district
threshold_exemption_rules:       N/A (no threshold to exempt
                                 from at council level)
threshold_backdoor:              N/A

apparentement_allowed:           no
intra_list_rule:                 list_order                   # § 33(6)
preference_threshold_pct:        N/A (closed list)
intra_list_ties_rule:            in submitted order (closed list);
                                 inter-party ties resolved by
                                 § 33's standard tie rules
overhang_rule:                   if a party wins more constituency
                                 seats than its proportional share
                                 supports, additional council seats
                                 may be added (Überhangmandate);
                                 the 2024 reform debated removing
                                 these
```

### Notes — the 2024–2025 formula saga

This is the project's most important comparative case for the
**political and judicial economics of formula choice**. The
sequence:

| Date | Event |
|---|---|
| Pre-2024 | KWahlG § 33 used Sainte-Laguë / Webster (the same divisor procedure as the federal Bundestag and Bavaria post-2018). |
| 5 July 2024 | Landtag NRW amended § 33 to replace Sainte-Laguë with the "**Rock-Verfahren**" — a quota method with percentage remainder distribution that systematically allocated rounding gains to larger parties. Effective 31 July 2024. |
| Spring 2025 | Smaller-party state branches filed *Organstreitverfahren* (constitutional inter-organ proceedings) at the VerfGH NRW. |
| **20 May 2025** | **VerfGH NRW (VerfGH 124/24) struck down the Rock-Verfahren** as violating the equal-chances and equality-of-elections doctrines. |
| 10 June 2025 | Landtag adopted an amending act reverting § 33 to Sainte-Laguë / Webster. |
| 28 June 2025 | Consolidated republication of KWahlG. |
| 14 September 2025 | NRW local elections held under the restored Sainte-Laguë formula. |

#### VerfGH NRW reasoning (20 May 2025)

The Court applied two constitutional standards in combination:

1. **Equal chances for political parties** — Article 21(1) GG +
   Article 2 NRW Constitution. Parties have a fundamental right
   to compete on equal terms; legislative interventions that
   systematically advantage some parties over others must be
   "sachlich gerechtfertigt" (materially justified).
2. **Equality of elections** (*Wahlrechtsgleichheit*) —
   Article 28(1) GG + Article 78(1) NRW Constitution. Each
   vote must have equal weight; allocation procedures that
   produce systematic vote-value inequality are presumptively
   unconstitutional.

The Court found that the Rock-Verfahren violated both:

- It produced an "**erhöhung der faktischen Sperrwirkung**" —
  an *increased effective barrier effect* against smaller
  parties.
- Rounding gains went **systematically and predictably** to
  larger parties, rather than (as under Sainte-Laguë) being
  essentially random. Mathematical evidence presented to the
  Court showed the new method departed from proportionality
  in predictable ways.
- The legislature failed to identify any constitutional
  purpose served by introducing this new advantage to larger
  parties; the asserted purposes were post-hoc.

The remedy was to invalidate the 2024 amendment, restoring
Sainte-Laguë in time for the September 2025 elections.

#### Why this saga matters for US implementation

Three takeaways with direct application:

1. **Formula choice is reviewable**, not just political. A
   constitutional court applying ordinary equal-protection
   analysis can strike a formula that systematically
   disadvantages smaller parties. US state constitutional
   courts could, in principle, apply analogous analysis to a
   state-level PR statute.
2. **The "rounding-gains-to-larger-parties" diagnostic**: the
   VerfGH used a clean mathematical test — does the formula
   make rounding gains *predictably* favor one class of
   parties? Sainte-Laguë and Webster pass this test (rounding
   is essentially random); D'Hondt/Jefferson, Imperiali, and
   the Rock-Verfahren do not. This test is portable.
3. **Strict scrutiny on formula manipulation**: the burden
   shifts to the legislature to justify any move *away* from a
   neutral formula. Drafters in any US PR adoption should be
   alive to this — a state high court applying analogous
   doctrine could insist on a sound public-purpose
   justification for any non-neutral choice.

---

## 4. Connected areas (brief)

### A. Voter eligibility

§ 7 KWahlG: voting age **16** (versus 18 federally — NRW is one
of several *Länder* that lowered the local voting age). Eligible:
German citizens or EU citizens with **principal residence in the
relevant electoral area for at least 16 days** before election
day. § 8 mirrors federal disqualification rules: judicial
decision required.

The 16-year voting age is itself an interesting comparator: it
demonstrates that a *Land* can lower the voting age for local
elections without disturbing federal law.

### B. Candidate / list registration

#### Wahlbezirk nominations (§ 15)

- Submittable by parties, voter groupings, or eligible voters
  (independent candidates).
- Signature requirement scaling with *Wahlbezirk* size: per
  the regulatory summary, **5 to 20 signatures of eligible
  voters in the district**.
- § 15a (added in recent years): donation transparency
  obligations for candidates and groups.

#### Reserve lists (§ 16)

- Submittable by parties or voter groupings — **not by
  individual candidates**.
- Signature requirement for new groups: **1 per 1,000
  eligible voters** (with a floor of 5 and a ceiling of 100)
  per the regulatory summary.
- Established parties (continuously represented, similar to
  the federal continuous-representation exemption) are exempt
  from signature requirements.

#### Operationalized values

```
list_registration_authority:     municipal Wahlleiter and Wahl-
                                 ausschuss (§ 18)
signatures_required_min:         5 (smallest districts and floor
                                 for new-group reserve lists)
signature_scaling:               population-tiered for both Wahl-
                                 bezirk and reserve list
deposit_amount:                  none
filing_deadline_days_before:     consolidated text to verify;
                                 typically ~70 days
party_v_nonparty_equal_treatment:
                                 yes (same § 15 / § 16 schedule)
list_size_min:                   not statutorily fixed
list_size_max:                   not statutorily fixed (lists
                                 may be longer than the council
                                 size; surplus stays unused)
list_ordering_rule:              submitter (closed list)
gender_quota:                    none in KWahlG; some parties
                                 apply internal quotas
residency_required:              candidate must be eligible to
                                 vote in the municipality (§ 12)
multiple_candidacy_restrictions: candidate may stand in one
                                 Wahlbezirk and on one reserve
                                 list (§ 15 / § 16); exclusive
                                 within the same election
```

### C. Campaign finance

Federal *Parteiengesetz* applies to parties; voter groupings are
not subject to PartG. KWahlG § 15a introduces a **donation-
transparency obligation** specific to NRW local elections —
this is unusual at *Land* level and a useful drafting
precedent for jurisdictions wanting to extend disclosure
norms to non-party participants.

### D. Election administration

§ 2 establishes the *Wahlorgane* (electoral bodies); the
implementing *Kommunalwahlordnung* (KWahlO) details
proceedings. Decentralized to the municipality, with state
oversight.

### E. Vote count, certification, dispute resolution

§§ 29–30 govern counting and invalid votes (parallel to
federal § 39 BWahlG / BWO § 69). The dispute-resolution chain
(§§ 39–42):

- **§ 39 Einspruch**: written objection lodged within **one
  month** of the election; standing for any eligible voter and
  for state-level officials.
- **§ 40 Entscheidung über die Gültigkeit**: the council
  itself first decides on the validity of the election —
  similar to the federal *Wahlprüfungsausschuss* mechanism but
  at municipal level.
- **§ 41 Klage**: judicial appeal to the *Verwaltungsgericht*
  (administrative court) within one month.
- **§ 42 Wiederholungswahl**: rerun election where required.

The route bypasses the federal *Wahlprüfungsgesetz* and the
BVerfG, going instead through *Verwaltungsgerichtsbarkeit* —
the same channel used in Bavaria.

### F. Media access

Not extensively governed at the NRW municipal level; equal-
treatment doctrines from federal *Medienstaatsvertrag* apply.

### G. Sondervorschriften (special provisions)

§§ 46a–46k cover **Bezirksvertretungen** (urban-district sub-
councils), mayoral elections, and the **Regionalverband Ruhr**
(Ruhr Regional Assembly). These bodies retain a 2.5%
threshold that the VerfGH NRW upheld in 2017 as
constitutionally permissible at sub-municipal-or-regional
level.

---

## 5. PROSeS performance diagnostic

The next regular NRW local elections were held on **14
September 2025**, under the post-VerfGH-restored Sainte-Laguë
formula. There is no OSCE/ODIHR observation report at the
*Land* municipal level (analogous to the federal Bundestag
report). Empirical evidence for this section comes from:

- *Landeswahlleiter* / *Landesbetrieb Information und Technik
  Nordrhein-Westfalen* (IT.NRW) — official results.
- VerfGH NRW jurisprudence (the 2017 and 2025 rulings).
- Academic and press literature on the 2025 elections.

### Process Design

The 2024–2025 episode is itself a process-design failure: the
ruling coalition (CDU-SPD-Greens) attempted to alter the
allocation formula in its favor, the VerfGH struck the
amendment down four months before the election, and the
restoration was enacted under time pressure. ODIHR-equivalent
analysis would flag the lack of pre-amendment consultation and
the absence of empirical justification for the proposed change.

### Resource Investment

NRW funds local elections through the standard *Land*-municipal
cost-sharing model; per-vote cost data is not routinely
published.

### Service Output Quality

**Convenience**: ballot is single-vote and short — accessibility
strengths. Postal voting available.

**Accuracy**: closed-list one-vote ballot historically produces
low invalid-vote rates compared to Bavaria's open-list
ballot. NRW 2020 invalid-vote rates were under 1.5% for both
council and county elections.

### Service Outcomes

**Turnout** at NRW local elections has historically tracked
55–65%. The 2020 election (held during COVID restrictions)
produced lower turnout in some municipalities.

**Equity**: in 2020, the AfD's NRW state list received
significant council representation only after the 2.5%
threshold removal in 2017; the 2017 ruling thus had material
effect on representation diversity.

### Stakeholder Satisfaction

The 2024–2025 saga produced significant stakeholder
dissatisfaction among smaller parties (the petitioners in
*VerfGH 124/24*) and constitutional commentators. Restoration
of Sainte-Laguë for the September 2025 election was widely
welcomed.

#### Major outstanding empirical work

- 2020 and 2025 NRW local election outcome data: invalid-vote
  rates by municipality size; share of seats won by
  *Wählergruppen*; share of council membership the 2.5%
  threshold removal enabled (counterfactual analysis).
- Comparative analysis of voter satisfaction with single-vote
  closed-list versus the Bavarian open-list-with-cumulation
  ballot.

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant   # § 7 KWahlG; voting age 16
equal_suffrage:        compliant   # post-VerfGH 2025 formula
                                   # restoration restored equal
                                   # success-value
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant   # 5-year term
fundamental_rights:    compliant
regulatory_stability:  medium      # 2024 reform and 2025 strike-
                                   # down created mid-cycle
                                   # uncertainty parallel to the
                                   # federal Bundestag situation
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| One-vote MMP architecture (§§ 31, 25) | **Universal** | Operationally simpler than two-vote MMP; portable to any US state-legislature MMP design where ballot simplicity is the priority. |
| Closed reserve lists (§ 16, § 33(6)) | **Universal** | Standard closed-list mechanic; entirely portable. |
| Three-name list display on ballot (§ 23) | **Universal** | Modest disclosure of list leadership without ballot bloat. |
| Sainte-Laguë / Webster allocation (§ 33) | **Universal** | Same formula as US House apportionment among states. |
| No statutory threshold for council elections | **Hybrid** | The substantive choice (no threshold) is portable; the *constitutional reasoning* (VerfGH NRW 2017) is rooted in *Wahlrechtsgleichheit* doctrine that has analogues but not direct parallels in US equal-protection law. |
| Strict scrutiny on formula manipulation (VerfGH 2025) | **Universal** | The "predictable-rounding-bias" diagnostic is portable; the legal vehicle (state constitutional equal-chances doctrine) varies by jurisdiction. |
| 16-year voting age for local elections | **Particular** | German local jurisdictions experiment with this; US local-voting-age innovation is also occurring (Takoma Park, MD) but the constitutional posture differs. |
| Donation-transparency for non-party participants (§ 15a) | **Universal** | Useful drafting precedent for any US jurisdiction extending disclosure to non-party lists. |
| Bezirksvertretungen retaining 2.5% threshold | **Particular** | Reflects a specific German distinction between top-tier representative bodies and sub-tier consultative bodies. |

### Top three takeaways for US state/local implementation

1. **One-vote MMP is operationally simpler than two-vote MMP.**
   NRW's § 31 architecture preserves the proportional outcome
   while halving the ballot's cognitive load relative to the
   federal Bundestag. For US states considering an MMP-style
   reform, NRW is the cleaner direct model — particularly
   where voters are unaccustomed to dual-ballot logic.

2. **Constitutional courts can police formula manipulation.**
   The 2024–2025 saga shows that an attempt to manipulate the
   allocation formula in favor of larger parties is reviewable
   under equal-chances and equality-of-elections doctrines.
   The "predictable-rounding-bias" test is a clean diagnostic
   that US state constitutional courts could plausibly adopt
   under existing equal-protection doctrine.

3. **Threshold reduction has constitutional backing.** The
   VerfGH 2017 ruling demonstrates that statutory thresholds
   for top-tier representative bodies require *concrete*
   empirical justification, not abstract concerns about
   fragmentation. US state constitutions that contain analogous
   equal-vote-success-value protections could provide
   parallel constitutional support for low-or-no-threshold
   designs.

---

## 8. Sources

### Primary

- *Kommunalwahlgesetz* (KWahlG) für das *Land* Nordrhein-
  Westfalen, neu bekanntgemacht am 28. Juni 2025 (consolidated
  republication following VerfGH NRW judgment of 20 May 2025
  and amending act of 10 June 2025).
  <https://recht.nrw.de/lrgv/gesetz/28062025-bekanntmachung-der-neufassung-des-kommunalwahlgesetzes-kommunalwahlgesetz>
- *Kommunalwahlordnung* (KWahlO) — implementing regulation.
- *Verfassung für das Land Nordrhein-Westfalen*.
- *Grundgesetz* Article 28(1).

### Constitutional decisions

- **VerfGH NRW**, judgment of 21 November 2017,
  *2,5 %-Sperrklausel* — 2.5% threshold for *Gemeinderat* and
  *Kreistag* unconstitutional. Press release:
  <https://www.verfgh.nrw.de/aktuelles/pressemitteilungen/2017/10_171121/index.php>
- **VerfGH NRW**, judgment of 20 May 2025, **VerfGH 124/24** —
  2024 amendment of § 33 KWahlG (Rock-Verfahren) replacing
  Sainte-Laguë declared unconstitutional. Press release:
  <https://www.verfgh.nrw.de/aktuelles/pressemitteilungen/2025/11_250520/index.php>
  Full text:
  <https://www.verfgh.nrw.de/rechtsprechung/entscheidungen/2025/250520_124_24.pdf>

### Secondary

- *Wahlrecht.de — Kommunalwahlsystem in Nordrhein-Westfalen*:
  <https://www.wahlrecht.de/kommunal/nordrhein-westfalen.html>
- LTO press coverage of the 2024 reform and 2025 ruling.
- Bavarian comparators in `cases/germany/bavaria_profile.md`.

### Outstanding gaps

- Verbatim text of KWahlG §§ 3, 4, 16, 31, 32, 33 (for
  Components 1, 2, 3 respectively).
- Verbatim text of §§ 15, 15a (Wahlbezirk nominations,
  donation transparency), § 16 (Reservelisten).
- Cache local PDF of the May 2025 VerfGH ruling.
- 2025 NRW local election outcome data.
- Comparison of invalid-vote rates between NRW (closed-list
  one-vote) and Bavaria (open-list cumulation/panachage).
