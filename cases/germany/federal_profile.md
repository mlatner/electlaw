# Germany — Federal level (Bundestag MMP)

## 0. Case metadata

- **Country**: Federal Republic of Germany
- **Sub-jurisdiction**: Federal level (Bund)
- **Level of government**: National
- **Electoral system family**: Mixed-Member Proportional (MMP)
- **Governing statute (primary)**: *Bundeswahlgesetz* (BWahlG) —
  *Federal Elections Act*
- **Citation**: BWahlG in der Fassung der Bekanntmachung vom 23.
  Juli 1993 (BGBl. I S. 1288, 1594), zuletzt geändert durch Artikel
  1 des Gesetzes vom 7. März 2024 (BGBl. 2024 I Nr. 91).
- **URL**: <https://www.gesetze-im-internet.de/bwahlg/>
- **Year**: 1956 originally; current consolidated 23 July 1993; last
  amended 7 March 2024.
- **Language**: German (official). Official English translation
  available from the Federal Returning Officer; cached locally at
  `sources/germany/Bundeswahlgesetz_EN_official.pdf`.
- **Constitutional anchor**: Grundgesetz (Basic Law) Articles 38–41.
- **Governing implementing regulation**: *Bundeswahlordnung* (BWO).
- **Recent constitutional decision**: BVerfG, judgment of 30 July
  2024, 2 BvF 1/23 et al. (*Wahlrechtsreform 2023*).
- **Analyst**: (this profile, 2026-05-04)

### Why this case is in the project

Germany's federal regime is the canonical working example of MMP.
Its 2023 reform (Article 1 of the Act of 8 June 2023, BGBl. 2023 I
Nr. 147), as modified by the BVerfG ruling of 30 July 2024,
represents the most recent serious attempt by a mature MMP
democracy to fix Bundestag size and eliminate overhang seats while
preserving proportional outcomes. For any US state-legislature-
level reform considering MMP, this is the strongest comparator.

The federal regime is **structurally partisan** — Land lists may
only be submitted by registered political parties under the
*Parteiengesetz* — and so does *not* directly model non-partisan
list administration. That role is filled by the *Länder* municipal
profiles (Bavaria, Baden-Württemberg, Hesse) to follow.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — § 1 BWahlG

> **§ 1 Composition of the German Bundestag and Principles of
> Franchise**
>
> (1) The German Bundestag consists of 630 members. They are
> elected in a general, direct, free, equal and secret ballot by
> the Germans eligible to vote.
>
> (2) The principles of proportional representation apply in
> elections to the German Bundestag. Each voter has two votes, a
> first vote to be cast in an election based on constituency
> nominations and a second vote to be cast in an election based on
> Land lists where the parties admitted to participate in the
> election name their candidates.
>
> (3) When the seats going to the Land lists are allocated to
> individual candidates, priority is given, subject to the
> provisions of section 6, to candidates determined in 299
> constituencies in an election based on constituency nominations.
> In each Land, each party gets as many seats for those of its
> candidates who have won the most first votes in the constituencies
> of the Land as are backed by the number of second votes cast for
> that party (seat allocation based on second votes).
>
> (4) Candidates who have not been nominated by a party may stand
> for election in the constituencies in accordance with the
> requirements resulting from this Act.

(German original of § 1(1): "Der Deutsche Bundestag besteht aus
630 Abgeordneten. Sie werden in allgemeiner, unmittelbarer,
freier, gleicher und geheimer Wahl von den wahlberechtigten
Deutschen gewählt.")

### Statutory text — § 3 BWahlG (Constituency Commission)

§ 3 fixes the criteria for drawing constituencies (excerpts):

> (1) The following principles must be observed in the division of
> the electoral area into constituencies:
>
> 1. The Länder boundaries must be respected.
> 2. The number of constituencies in the individual Länder must
>    correspond, as far as possible, to their share of the
>    population. The number is calculated in accordance with
>    section 5.
> 3. The population in a constituency should not be more than
>    fifteen percent above or below the average figure for all
>    constituencies; in cases where the difference is greater than
>    twenty-five percent, the constituency boundaries must be
>    redrawn. *[As of 1 January 2026: ten percent / fifteen percent
>    respectively.]*
> 4. Each constituency should form a coherent area.
> 5. The boundaries of the municipalities, districts and urban
>    districts are respected, where possible.
>
> Foreigners (section 2, subsection (1) of the Residence Act) are
> not taken into account in the determination of population
> figures.
>
> (2) The Federal President appoints a permanent Constituency
> Commission. It consists of the President of the Federal
> Statistical Office, a judge from the Federal Administrative
> Court, and five other members.

### Operationalized values

```
total_seats: 630                                            # § 1(1)
codification_instrument: federal statute (BWahlG)
amendment_authority: Bundestag (Bundesrat involvement for
  Land-affecting provisions)
amendment_threshold: ordinary federal legislation
last_change_year: 2024 (BGBl. 2024 I Nr. 91)

magnitude_uniform: no
magnitude_typical: 1 (constituency tier)
magnitude_range: 1 (constituency); variable per Land list
districts_count: 299                                        # § 1(3)
districting_authority: Constituency Commission (§ 3(2))
districting_frequency_years: report due within 15 months of each
  Bundestag legislative term (§ 3(4))
districting_criteria_in_statute: see § 3(1) numbers 1–5 above
population_deviation_target_pct: 15 (tightening to 10 from 2026-01-01)
population_deviation_redraw_pct: 25 (tightening to 15 from 2026-01-01)

tiered: yes
tier_count: 2 (constituency tier, integrated with Land list pool)
tier_compensatory: yes (Land list pool covers proportional balance;
  no overhang seats since 2023 reform — § 4(2) sentence 2 number 1)

threshold_of_exclusion_pct: structural value dominated by the legal
  5% threshold (Component 3); see § 4(2) and footnote (Grundmandats-
  klausel transitional rule per BVerfG 30 July 2024)
```

### Notes

The 2023 reform introduced **Zweitstimmendeckung** — translated as
"seat allocation based on second votes" in the official English
translation. This eliminates overhang and balance seats: a
constituency candidate who wins the most first votes is **only
seated** if the party's second-vote share supports the seat. The
mechanism is set in three places: § 1(3) (priority rule); § 4(2)
sentence 2 number 1 (excluding the second votes of voters whose
first-vote candidate won); and § 6 (candidate-level allocation).

The BVerfG upheld Zweitstimmendeckung as constitutional in 2 BvF
1/23 (30 July 2024).

The 630-member figure is fixed by § 1(1). The single statutory
exception is in § 4(4): if a party wins more than half the second
votes but would otherwise be allocated fewer than half the seats,
additional seats are added until the party holds half-plus-one,
and the total Bundestag size increases accordingly. This is a
last-resort majoritarian guarantee, not a routine mechanism.

---

## 2. Component 2 — Ballot Structure

### Statutory text — § 1(2) BWahlG (two-vote ballot)

The two-vote design is the central architectural choice; it appears
above in Component 1.

### Statutory text — § 30 BWahlG (Ballot Papers)

> (1) The ballot papers and the required envelopes for the postal
> ballot (section 36 subsection (1)) must be produced by the
> government.
>
> (2) The ballot paper contains:
>
> 1. for constituency elections, the names of the candidates from
>    the admitted constituency nominations; in the case of
>    constituency nominations by parties, also the names of these
>    parties as well as any shortened form of the party name that
>    the party may use; in the case of other non-party
>    constituency nominations, also the identifying name;
>
> 2. for Land list elections, the names of the parties and any
>    shortened form of the party name that the party may use as
>    well as the names of the first five candidates from the
>    admitted Land lists.
>
> (3) The order of the Land lists of parties is determined by the
> number of second votes that the parties received at the last
> Bundestag election in the Land concerned. The remaining Land
> lists then follow in alphabetical order of the names of the
> parties. The order of the constituency nominations is determined
> by the order of the corresponding Land lists. Other constituency
> nominations then follow in alphabetical order of the names of
> the parties or identifying names.

### Statutory text — § 34 BWahlG (Voting by Means of Ballot Papers)

> (1) Voting is by means of official ballot papers.
>
> (2) The voter
>
> 1. casts his or her first vote by marking the ballot paper with
>    a cross or other sign so as to clearly indicate which
>    candidate the vote is intended for,
>
> 2. casts his or her second vote by marking the ballot paper
>    with a cross or other sign so as to clearly indicate which
>    Land list the vote is intended for.
>
> The voter then folds the ballot paper in such a way that it is
> not possible to see how he or she has voted, and places the
> ballot paper in the ballot box.

### Statutory text — § 45 BWO (Ballot Papers — Implementing Detail)

The BWahlG § 30 sets the high-level ballot rules; the
*Bundeswahlordnung* § 45 sets the detailed specifications:

- **Size**: at least DIN A4; **paper white or off-white**.
- **Privacy**: per § 45(1), "*Das Papier muss so beschaffen sein,
  dass nach Kennzeichnung und Faltung durch den Wähler andere
  Personen nicht erkennen können, wie er gewählt hat*" — the
  paper must be of such quality that after marking and folding
  by the voter, other persons cannot discern how the voter has
  voted.
- **Layout**: constituency candidates printed in **black** with
  party / shortened-name annotations and circles for marking;
  Land list candidates printed in **blue** with party name and
  the first five candidates' names, circles for marking
  positioned to the left.
- **Personal information**: only registered doctoral degrees
  (*Doktorgrad*) and registered artist names (*Künstlername*)
  may appear; family names must appear in full.
- **Accessibility**: § 45(2) requires that ballot papers be
  perforated or cut at the upper right corner so that templates
  for blind voters (produced and distributed by associations of
  the blind) can register against the perforation. Sample
  ballots must be provided promptly to those associations.
- **Postal voting**: § 45(3) requires postal-vote ballot
  envelopes to be white and opaque; § 45(4) requires return
  envelopes to be **light red** and to follow a specified
  pattern. When concurrent elections occur, federal envelopes
  must be visually distinguishable.
- **Distribution**: per § 45(6), the Constituency Returning
  Officer (*Kreiswahlleiter*) provides ballots and supplies
  envelopes to municipal authorities.

#### Notes on the BWO ballot regime for US implementation

Three drafting points stand out:

1. **Government-produced, statutorily standardized ballots**.
   Color, paper grade, perforation, and font are all set in the
   implementing regulation. This delivers the simplicity the
   Guinier primer prescribes (p. 13) with minimal voter cognitive
   load. US states have varying ballot-uniformity statutes; the
   German pattern is a useful model for high-uniformity drafting.
2. **Differentiated ink color (black vs. blue)** as a visual cue
   for distinguishing the two ballot tiers. Simple, but
   demonstrably effective: the 2025 invalid-vote rate of 0.8% /
   0.6% is among the lowest globally.
3. **Statutory accessibility infrastructure**. The perforation /
   cut for blind-voter templates is set in the regulation
   itself, not left to election-administration discretion. US
   Help America Vote Act (HAVA) and ADA accessibility provisions
   could be paired with comparably specific implementing rules.

---

#### Notes on Component 2 ballot mechanics from these sections:

- **Government production of ballots** (§ 30(1)): the federal
  government, not parties, produces the ballot — a non-trivial
  drafting choice. US implementation may inherit this from
  existing election-administration norms, but the principle is
  worth flagging in any model statute.
- **Land list display** (§ 30(2) no. 2): only the **first five
  candidates** of each Land list are printed on the ballot, even
  though the list may be much longer. This is a ballot-simplicity
  trade-off: the voter sees enough of the list to identify it but
  not enough to constitute a reordering opportunity.
- **Ballot ordering** (§ 30(3)): based on prior-election second
  votes per Land for established parties; alphabetical for new
  parties. Simple, mechanical, no discretion.
- **Mark requirement** (§ 34(2)): "a cross or other sign so as to
  clearly indicate" — the standard for valid voter intent. § 39(1)
  no. 4 invalidates ballots that "do not clearly show the voter's
  intent."

### Operationalized values

```
ballot_type: mmp_two_vote
preference_votes_per_voter: 2 (one Erststimme, one Zweitstimme)
panachage_allowed: no (Land lists are closed)
cumulation_allowed: no
above_the_line_option: not applicable

party_lists_allowed: yes
voter_grouping_lists_allowed: no — federal Land lists are
  party-only (§ 27)
citizen_committee_lists_allowed: no
independents_on_lists_allowed: no
independents_at_constituency_level: yes — § 1(4); § 20(3)
  Einzelbewerber path

non_party_label_allowed: no (federal level — labels are restricted
  to registered parties under PartG)
```

### Notes — partisan vs. non-partisan posture

The federal regime is structurally partisan. Land lists may only
be submitted by registered parties under the *Parteiengesetz*
(PartG). Voter groupings (*Wählervereinigungen*) — which dominate
the local-level analysis in this project — have **no path to the
proportional Land-list seats** at the federal level. Their access
is limited to the *Einzelbewerber* (independent candidate)
constituency path under § 1(4) and § 20(3).

For US implementation, this divides the lessons:
- **Partisan US contexts** (most state-legislature reform
  scenarios): the federal German MMP design is a strong direct
  model.
- **Non-partisan US contexts** (most local charter reform
  scenarios): look to the *Länder* municipal profiles instead.

---

## 3. Component 3 — Allocation Formula

### Statutory text — § 4 BWahlG (Principles of Seat Distribution among Parties)

> (1) The total number of seats (section 1 subsection (1)) is first
> distributed among the parties and then among the Land lists of
> each party according to the principles of proportional
> representation. The number of successful constituency candidates
> as per section 6 subsection (2) is subtracted from the total
> number of seats.
>
> (2) The seats are distributed among the parties in proportion to
> the number of second votes cast for the Land lists of each party
> in the electoral area as laid down in section 5 (upper level
> distribution). This procedure does not consider
>
> 1. the second votes of the voters who have cast their first votes
>    for a candidate who has been successful as per section 6
>    subsection (2) and
>
> 2. parties which have received less than 5 percent of the valid
>    second votes cast in the electoral area.
>
> Sentence 2 number 2 does not apply to the lists submitted by
> parties representing national minorities.
>
> (3) The seats allocated to each party pursuant to subsection (2)
> are distributed among the party's Land lists in proportion to the
> number of second votes cast for the Land lists in accordance with
> section 5 (lower level distribution).
>
> (4) If a party which has won more than half of the total number
> of second votes cast for all parties to be considered does not
> receive more than half of the seats in the distribution process,
> it is allocated further seats until the number of seats it has is
> equal to half of the seats plus one. The total number of seats
> (section 1 subsection (1)) increases by the difference in such a
> case.

#### Statutory footnote (BVerfG-modified threshold)

The official text now carries the following footnote to § 4(2)
sentence 2 number 2, reflecting the 30 July 2024 BVerfG ruling:

> Section 4 subsection (2), second sentence, number 2: Provision
> incompatible with Article 21 paragraph (1) and Article 38
> paragraph (1), first sentence, of the Basic Law according to the
> reasons stated by the Federal Constitutional Court in its ruling
> of 30 July 2024 I No. 281 - 2 BvF 1/23 etc. -. Section 4
> subsection (2), second sentence, number 2 of the Federal
> Elections Act will continue to apply until amendments are
> enacted, subject to the condition that political parties that
> receive less than 5 percent of the valid second votes cast in
> the electoral area will be excluded from the distribution of
> seats only if their candidates secure the most first votes in
> fewer than three constituencies.

This is the *Grundmandatsklausel* — the "basic mandate clause" —
restored as a transitional rule by the Court.

### Statutory text — § 5 BWahlG (Seat Distribution Calculation)

> (1) To determine the upper level distribution, the number of
> second votes to be considered in the electoral area is divided
> by a divisor for the allocation of seats, which is determined as
> per subsection (2), and the result of the division is rounded as
> per subsection (3). To determine the lower level distribution,
> the number of second votes going to each Land list of a party is
> divided by a divisor for the allocation of seats to be determined
> as per subsection (2), and the result of the division is rounded
> as per subsection (3).
>
> (2) The divisor for the allocation of seats is determined in a
> way that ensures that all available seats are distributed. To
> determine the divisor, the total of the votes on which the
> apportionment is based is divided by the number of available
> seats. If, using this divisor, more seats are distributed in
> total than are actually available, the divisor must be increased
> so that the result of the distribution process, when repeated,
> matches the number of seats available; if too few seats are
> allocated to the parties, the divisor must be reduced
> accordingly.
>
> (3) The division results as calculated pursuant to subsection (1)
> are rounded, whereby decimal fractions under 0.5 are rounded down
> to the nearest whole number and decimal fractions above 0.5 are
> rounded up to the nearest whole number. Decimal fractions equal
> to 0.5 are rounded up or down to ensure that the number of
> available seats is maintained; if there are various seat
> allocation options as a consequence, the Federal Returning
> Officer decides by drawing lots.

### Statutory text — § 6 BWahlG (Allocation of Seats to Candidates)

> (1) A constituency candidate of a party (section 20 subsection
> (2)) is elected as the constituency representative in the
> Bundestag if he or she wins the most first votes and is awarded a
> seat in the seat allocation procedure based on second votes
> (fourth sentence). In each Land, a party's candidates who have
> won the most first votes in the constituencies are ranked by
> descending proportion of first votes. The proportion of first
> votes is calculated by dividing the number of first votes cast
> for the candidate by the total number of valid first votes cast
> in the particular constituency. The seats determined for a
> party's Land list as per section 4 subsection (3) are awarded to
> the constituency candidates in the order established in
> accordance with the second sentence (allocation procedure based
> on second votes).
>
> (2) A candidate nominated pursuant to section 20 subsection (3)
> is elected as the constituency representative in the Bundestag
> if he or she wins the most votes.
>
> (3) If votes are tied and the proportions of first votes are
> equal, a lot is drawn to determine the winner. The lot is drawn
> by the Constituency Returning Officer if candidates competing in
> a constituency are concerned (subsection (1), first sentence;
> subsection (2)) and by the Federal Returning Officer if there is
> a tie in the allocation of seats based on second votes
> (subsection (1), fourth sentence).
>
> (4) A Land list candidate is elected as a member of the Bundestag
> if he or she is awarded a seat during the process of distributing
> the Land list seats (section 4, subsection (3)) that remained
> after the completion of the seat allocation procedure based on
> second votes; the seats are awarded in the order of the Land
> list. Candidates who have been elected pursuant to subsection
> (1), first sentence, are not considered as Land list candidates.
> If the number of seats allocated to a Land list exceeds the
> number of candidates listed, the respective seats remain vacant.

### Operationalized values

```
allocation_formula: webster_sainte_lague                    # via § 5
formula_codified_as: procedural (the rounding rule in § 5(3) — round
  to nearest, ties to maintain seat count, fall through to lot — is
  the defining characteristic of Sainte-Laguë / Webster, also called
  Sainte-Laguë/Schepers in German practice. The BWahlG specifies the
  procedure fully without using the eponym.)
formula_statutory_citation: BWahlG § 5
ties_rule: drawing of lots by Federal Returning Officer (§ 5(3),
  § 6(3))

legal_threshold_pct: 5                                      # § 4(2)
threshold_level: national (electoral area)
threshold_exemption_rules:
  - National minorities: § 4(2) third sentence — exempted entirely
  - Grundmandatsklausel (transitional, per BVerfG 30 July 2024):
    parties under 5% admitted if their candidates win the most
    first votes in 3 or more constituencies
threshold_backdoor: yes (Grundmandatsklausel — see above)

apparentement_allowed: no
intra_list_rule: list_order (closed list; no preference votes)
preference_threshold_pct: N/A
```

### Notes

The **Sainte-Laguë / Webster method** is implemented procedurally
in § 5 without using the name. The combination of (a) divisor
adjusted to fit available seats and (b) standard arithmetic
rounding (with 0.5 → maintain seat count, fallback to lot) is
mathematically equivalent to Webster / Sainte-Laguë. In German
electoral commentary the procedure is called *Sainte-Laguë/
Schepers* after Hans Schepers, who developed the divisor-iteration
implementation.

The German federal allocation works in **two levels**:

- *Oberverteilung* (upper level distribution, § 5(1) sentence 1):
  total 630 seats are allocated among parties nationally based on
  second votes.
- *Unterverteilung* (lower level distribution, § 5(1) sentence 2):
  each party's national allocation is then distributed among its
  16 Land lists in proportion to the Land-level second votes.

Within each Land list, **Zweitstimmendeckung** (§ 1(3)) ensures
that constituency winners are seated first up to the Land
allocation, with the remainder going to the closed Land list in
its submitted order (§ 6(4)). If a Land list runs out of
candidates, the remaining seats stay vacant (§ 6(4) third
sentence).

The 5% threshold is currently in legal transition. The BVerfG
ruled on 30 July 2024 (2 BvF 1/23 et al.) that the 5% threshold
without the *Grundmandatsklausel* is unconstitutional under
Articles 21(1) and 38(1) of the Basic Law. The Court ordered the
*Grundmandatsklausel* (basic mandate clause) — abolished by the
2023 reform — to apply transitionally until the legislature
enacts a new rule. That transitional rule is now reflected in a
footnote to § 4 of the BWahlG itself.

#### BVerfG reasoning — three-part test

The Court applied a three-part test to the 5% threshold (per the
official English press release; full reasoning available in the
ruling itself):

1. **Legitimate purpose**: Safeguarding proper Bundestag
   functioning by preventing parliamentary fragmentation. The
   Court found this purpose constitutionally legitimate.
2. **Suitability**: The 5% threshold is adequate to serve that
   purpose.
3. **Necessity**: The 5% threshold *exceeds what is necessary*
   under current legal and factual circumstances. The Court's
   key example: the CSU is structurally a regional party
   confined to Bavaria but joins a permanent parliamentary group
   with the CDU. A pure 5% threshold without exception would
   exclude a party whose Members would in fact join a joint
   group in the Bundestag — a result not required for the
   functioning of the Bundestag.

The Court's transitional rule restores the prior
*Grundmandatsklausel*: a party below 5% is admitted to seat
allocation if its candidates win the most first votes in **at
least three constituencies**. The Court justified the choice of
this transitional rule on the ground that the prior clause is
"familiar to the political parties and voters alike."

The Court also upheld a separate challenge to the unchanged
signature requirements (BVerfG, ruling of 22 January 2025),
holding that signature quorums "serve to ensure only
well-established political parties take part in the elections"
and that the unchanged provisions remained justified even under
the shortened timelines of an early election.

#### Why this matters for US implementation

Three points are particularly relevant for US drafting:

1. **The threshold is constitutional only with a backdoor.**
   Germany's experience confirms that any pure percentage
   threshold creates legitimacy problems for parties with
   significant local strength. A US adoption should anticipate
   either a Grundmandatsklausel-style exception, an
   apparentement-style pooling provision, or both.
2. **The "joint parliamentary group" reasoning is portable.**
   The Court's necessity analysis turned on whether excluding a
   party would actually advance Bundestag functioning given
   real-world coalition behavior. A US court applying analogous
   equal-protection analysis to a state PR threshold would face
   a structurally similar question.
3. **The transitional rule was rooted in voter familiarity.**
   The Court treated existing political-process expectations as
   load-bearing. US legislatures contemplating threshold reform
   should be alive to the same consideration: a familiar fallback
   pathway is easier to defend in court than a novel one.

#### Worked example: 23 February 2025 Bundestag election

Final results (per OSCE/ODIHR Final Report, p. 36; Federal
Returning Officer, certified 14 March 2025):

| Party | First vote % | Second vote % | Seats | Status |
|---|---:|---:|---:|---|
| CDU | 25.5 | 22.6 | 164 | over 5%; first-place plurality |
| AfD | 20.6 | 20.8 | 152 | over 5% |
| SPD | 20.1 | 16.4 | 120 | over 5% |
| Greens | 11.0 | 11.6 | 85 | over 5% |
| Left (Die Linke) | 7.9 | 8.8 | 64 | over 5% |
| CSU | 6.6 | 6.0 | 44 | over 5% (Bavaria-only) |
| SSW | 0.1 | 0.2 | 1 | national-minority exemption |

Total seats: 630 (no overhang increase under the 2023 reform).

Turnout: **82.5%** — highest since reunification in 1990.

Invalid-vote rates: **0.8%** first vote / **0.6%** second vote.

Key features visible in this contest:

1. **Threshold operation**: All major parties cleared the 5%
   threshold on second vote, so the *Grundmandatsklausel* was not
   invoked in 2025. The South Schleswig Voters' Association (SSW)
   seated one MP under the § 4(2) third-sentence national-minority
   exemption with only 0.2% of second votes.

2. **Zweitstimmendeckung in operation**: 23 candidates won the
   most first votes in their constituencies but did not receive a
   Bundestag mandate (18 CDU, 5 CSU). These constituencies were
   represented in the Bundestag not by the constituency-winning
   candidate but by the next eligible candidate on the relevant
   Land list (§ 6(4); § 1(3); § 4(2) sentence 2 number 1).

3. **Sainte-Laguë / Webster allocation** was applied at the
   *Oberverteilung* level (national: 11,196,374 CDU second votes
   against 49,649,512 valid second votes total → 22.6% → 164
   seats) and again at *Unterverteilung* (each party's national
   total split among its 16 Land lists in proportion to
   Land-level second votes). The full procedural rule of § 5
   produced integer seat allocations summing to 630.

4. **Gender outcome**: 426 men (67.6%) / 204 women (32.4%) —
   *decreased* from 35.3% in 2021. Statutory law contains no
   gender quota for federal elections; the 2023 Reform Commission
   established under § 55 was tasked with proposing such
   measures, but no measure has been enacted.

#### Counterfactual: what the 2021 election would have looked like under the 2023 reform

The Left (Die Linke) received **4.9% of second votes in 2021** —
below the 5% threshold — but won **3 constituency seats**,
satisfying the (then-still-applicable) *Grundmandatsklausel* and
so retaining parliamentary representation with 39 seats. Without
the *Grundmandatsklausel* — as the 2023 reform initially
provided — the Left would have been excluded from the 2021
Bundestag entirely.

The BVerfG cited this kind of result as central to its
constitutional necessity analysis (BVerfG 30 July 2024, 2 BvF
1/23): excluding a party with significant local wins solely on
the basis of the 5% threshold goes beyond what is necessary to
safeguard parliamentary functioning. The Court's restoration of
the *Grundmandatsklausel* as a transitional rule means the 2025
Left result (8.8% second vote, 64 seats) would have been admitted
to allocation in any case, but the rule remains live for future
contests where a party falls between roughly 4% and 5% but wins
≥3 constituencies.

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

#### Statutory text — § 12 (Eligibility to Vote)

> (1) All Germans as defined in Article 116 paragraph (1) of the
> Basic Law are eligible to vote, provided that, on the day of
> the election, they
>
> 1. have reached the age of eighteen years,
> 2. have had an abode or have otherwise been habitually resident
>    in the Federal Republic of Germany for at least three months,
>    and
> 3. are not disqualified from voting under section 13.
>
> (2) Provided the other conditions are fulfilled, Germans as
> defined in Article 116 paragraph (1) of the Basic Law who are
> resident outside the Federal Republic of Germany on the day of
> election are also eligible to vote provided that,
>
> 1. after reaching the age of fourteen years, they have had an
>    abode or have been habitually resident in the Federal Republic
>    of Germany for a minimum of three months without interruption,
>    provided that this stay took place within the last twenty-five
>    years, or
>
> 2. for other reasons, they have become familiar, personally and
>    directly, with the political situation in the Federal Republic
>    of Germany and are affected by it.

#### Statutory text — § 13 (Disqualification from Voting)

> A person is disqualified from voting if he or she is not eligible
> to vote owing to a judicial decision.

#### Statutory text — § 14 (Exercise of the Right to Vote, excerpts)

> (1) Only persons who are listed in an electoral register or have
> a polling card may vote.
>
> (4) Each person eligible to vote may vote only once and must do
> so personally. It is not permitted for the right to vote to be
> exercised by a proxy instead of the person eligible to vote.
>
> (5) Persons eligible to vote who are illiterate or prevented by
> a disability from casting their vote may seek the assistance of
> another person for that purpose. Such support is limited to
> practical assistance in communicating an electoral decision
> which has been taken and expressed by the person eligible to
> vote.

#### Statutory text — § 15 (Eligibility to Stand for Election)

> (1) A person is eligible to stand for election if, on election
> day, he or she
>
> 1. is German as defined in Article 116 paragraph (1) of the
>    Basic Law and
> 2. has reached the age of eighteen years.
>
> (2) A person is ineligible to stand for election if he or she
>
> 1. is disqualified from voting under section 13 or
> 2. has been deprived by judicial decision of the eligibility to
>    stand for election or the ability to hold public office.

#### Notes

The federal regime is **citizenship-restricted**: eligibility runs
through Article 116 GG (the constitutional definition of "German",
which extends beyond bare citizenship). Non-citizens — including
long-term resident foreigners — are excluded.

§ 12(2) creates **out-of-country voting rights** with a 25-year
sunset for departed Germans, an interesting comparator for any US
overseas-voting reform. Note the alternative path in § 12(2) no. 2
("personally and directly familiar with the political situation"
and "affected by it"), which is unusual and deserves citation in
US implementation discussions.

§ 14(4) **bars proxy voting**. § 14(5) permits assistance for
illiterate or disabled voters, with strict limits to "practical
assistance in communicating an electoral decision which has been
taken and expressed by the person eligible to vote." This is a
useful drafting model for US accessibility provisions.

The electoral register is maintained by **municipal authorities**
per § 17(1); each polling district has its own register.
Right-to-verify provisions (§ 17(1)) extend only between the
twentieth and sixteenth day before the election, with limited
rights to inspect others' entries on the register.

### B. Candidate / list registration

#### Statutory text — § 2 *Parteiengesetz* (Definition of "Party")

The legal boundary between *Partei* (party) and *Wählervereinigung*
(voter grouping) is set in § 2 of the *Parteiengesetz* (PartG):

> (1) Parteien sind Vereinigungen von Bürgern, die dauernd oder
> für längere Zeit für den Bereich des Bundes oder eines Landes
> auf die politische Willensbildung Einfluß nehmen und an der
> Vertretung des Volkes im Deutschen Bundestag oder einem Landtag
> mitwirken wollen, wenn sie nach dem Gesamtbild der tatsächlichen
> Verhältnisse, insbesondere nach Umfang und Festigkeit ihrer
> Organisation, nach der Zahl ihrer Mitglieder und nach ihrem
> Hervortreten in der Öffentlichkeit eine ausreichende Gewähr für
> die Ernsthaftigkeit dieser Zielsetzung bieten.

(English translation: "Parties are associations of citizens who,
permanently or for an extended period, seek to influence political
opinion-formation at the federal or *Land* level and to participate
in the representation of the people in the Bundestag or a *Landtag*,
provided that, on the overall picture of actual circumstances — in
particular the scope and stability of their organization, the
number of their members, and their public profile — they offer
sufficient guarantee of the seriousness of this purpose.")

§ 2(1) sentence 2 limits party membership to natural persons.

§ 2(2): a party loses *Partei* status if it does not contest
federal or *Land* elections with its own candidates for six
consecutive years, or if it fails to submit financial-disclosure
reports under § 23 PartG for six years.

§ 2(3): an association cannot have *Partei* status if (a) the
majority of members or board members are foreign nationals, or
(b) its headquarters or management is outside the territorial
scope of the Act.

#### Notes on the partisan / non-partisan boundary

§ 2(1)'s "permanently or for an extended period" plus the
"sufficient guarantee of seriousness" test draw the legal line:

- An organization that satisfies § 2(1) is a **Partei** and may
  submit Land lists (BWahlG § 27(1)) and partisan constituency
  nominations (BWahlG § 20(2)).
- An organization that does *not* satisfy § 2(1) — typically a
  *Wählervereinigung* / *Wählergruppe* at the local level — has
  no path to federal Land lists. At local level, separate *Land*
  electoral law governs (see planned `bavaria_profile.md` and
  others).
- A non-party individual may stand at federal constituency level
  via the *Einzelbewerber* path (BWahlG § 1(4), § 20(3)).

The Federal Electoral Committee makes the binding determination
of party status under BWahlG § 18(2)–(4); a party or association
denied recognition has a **four-day window** to appeal to the
BVerfG (BWahlG § 18(4a)).

#### Three nomination tracks at the federal level

1. **Established-party constituency and Land list nominations**
   (no signature requirement) — for parties continuously
   represented by ≥5 members in Bundestag or any Landtag.
2. **New-party constituency and Land list nominations**
   (signature thresholds apply) — for parties below that
   continuous-representation threshold.
3. **Non-party / independent constituency nominations**
   (Einzelbewerber) — at constituency level only; no Land list
   access for independents.

#### Statutory text — § 18 (Right to Nominate Candidates, Notification of Participation)

> (1) Nominations of candidates may be submitted by parties and
> by persons eligible to vote in accordance with section 20.
>
> (2) Parties which have not been continuously represented by at
> least five representatives in the German Bundestag or in a
> Landtag since the last election to that assembly on the basis of
> nominations made by the party itself may only submit nominations
> as parties if they have given notification of their participation
> in the election to the Federal Returning Officer in writing not
> later than 6 p.m. on the ninety-seventh day before the election
> and have been recognised as parties by the Federal Electoral
> Committee. Such notification must include the name under which
> the party intends to participate in the election. It must bear
> the personal handwritten signatures of at least three members of
> the national executive committee, including the chairperson or
> his or her deputy. […] The party's written statutes and written
> programme as well as proof that the executive committee has been
> duly appointed in accordance with the statutes must be enclosed
> with the notification. As a rule, proof of party status in
> accordance with section 2 subsection (1), first sentence, of the
> Political Parties Act is to be enclosed with the notification.
>
> (4) The Federal Electoral Committee confirms as binding for all
> electoral bodies not later than the seventy-ninth day before the
> election
>
> 1. which parties have been continuously represented by at least
>    five representatives in the German Bundestag or in a Landtag
>    since the last election […],
>
> 2. which associations, having given notification of their
>    participation pursuant to subsection (2), must be recognised
>    as parties for the election; a two-thirds majority is
>    necessary to refuse an association recognition as a party
>    for the election. […]
>
> (4a) A party or association may lodge a complaint with the
> Federal Constitutional Court against a confirmation pursuant to
> subsection (4) preventing it from submitting nominations within
> four days of the announcement. In such case the party or
> association must be treated by the electoral bodies as a party
> entitled to submit nominations until a decision has been taken
> by the Federal Constitutional Court, at the latest until the end
> of the fifty-ninth day before the election.
>
> (5) A party may submit only one constituency nomination in each
> constituency and only one Land list in each Land.

#### Statutory text — § 19 (Submission of Nominations)

> Constituency nominations must be submitted in writing to the
> Constituency Returning Officer and Land lists to the Land
> Returning Officer not later than 6 p.m. on the sixty-ninth day
> before the election.

#### Statutory text — § 20 (Content and Form of Constituency Nominations)

> (1) A constituency nomination may only contain the name of one
> candidate. Each candidate may only be named in one constituency,
> and only in one nomination for that constituency. A person may
> only be nominated as a candidate if he or she has given his or
> her written consent to the nomination; such consent is
> irrevocable.
>
> (2) Constituency nominations of parties must bear the personal
> handwritten signatures of the members of the executive committee
> of the Land branch of the party or, where such Land branches do
> not exist, the personal handwritten signatures of the members of
> the executive committee of the next lower regional branches in
> whose area the constituency lies. They may only be admitted if a
> Land list of the party is admitted in the respective Land.
> Constituency nominations of the parties specified in section 18
> subsection (2) must in addition bear the personal handwritten
> signatures of at least 200 persons eligible to vote in the
> constituency; they must be eligible to vote at the time they
> sign the nomination and proof of this must be furnished when the
> nomination is submitted. The requirement to provide 200
> signatures does not apply to constituency nominations of parties
> representing national minorities.
>
> (3) Non-party constituency nominations must bear the personal
> handwritten signatures of at least 200 persons eligible to vote
> from the constituency concerned. Subsection (2), third sentence,
> second half-sentence, applies accordingly.
>
> (4) Constituency nominations of parties must contain the name of
> the submitting party and any shortened form of the party name
> that the party may use, non-party constituency nominations must
> contain an identifying name.

#### Statutory text — § 21 (Selection of Party Candidates), excerpt

> (1) A person may only appear as a party candidate on a
> constituency nomination form if he or she is not a member of
> another party and has been elected for this purpose at a
> members' assembly convened to elect a constituency candidate or
> at a special or general delegates' assembly. […]
>
> (3) The candidates and the delegates for the delegates'
> assemblies are elected by secret ballot. Proposals can be
> submitted by all those attending the assembly who have voting
> rights. Candidates must be given the opportunity and time to
> duly introduce themselves and present their programmes to the
> assembly. Elections may take place no earlier than thirty-two
> months after the commencement of the legislative term of the
> German Bundestag, in the case of the delegates' assembly no
> earlier than twenty-nine months; this does not apply if the
> term ends prematurely.

#### Statutory text — § 27 (Land Lists)

> (1) Land lists may only be submitted by political parties. They
> must bear the personal handwritten signatures of the members of
> the executive committee of the Land branch or, where Land
> branches do not exist, those of the members of the executive
> committees of the next lower regional branches that lie within
> the territory of the Land and, in the case of the parties
> specified in section 18 subsection (2), the personal handwritten
> signatures of one per thousand of the persons eligible to vote
> in the Land at the last Bundestag election, but of not more
> than 2,000 eligible voters. The signatories of a nomination of
> one of the parties specified in section 18 subsection (2) must
> be eligible to vote at the time they sign the nomination and
> proof of this must be furnished when the Land list is
> submitted. The requirement to present additional signatures
> does not apply to Land lists of parties representing national
> minorities.
>
> (2) Land lists must contain the name of the party submitting the
> lists as well as any shortened form of the party name that the
> party may use.
>
> (3) The names of the candidates must be listed in a recognisable
> order.
>
> (4) A candidate may only be nominated in one Land, and in only
> one Land list in said Land. A candidate may only be nominated
> in a Land list if he or she has not been nominated pursuant to
> section 20 subsection (3). A person may only be nominated in a
> Land list if he or she has given his or her written consent to
> the nomination; such consent is irrevocable.

#### Operationalized values

```
list_registration_authority: Federal Electoral Committee
  (Bundeswahlausschuss) for party recognition under § 18(2)–(4);
  Land Electoral Committee (Landeswahlausschuss) for Land list
  admission under § 28; Constituency Electoral Committee for
  constituency nomination admission under § 26
party_recognition_deadline_days_before: 97 (§ 18(2))
party_recognition_decision_deadline_days_before: 79 (§ 18(4))
party_recognition_BVerfG_appeal_window_days: 4 (§ 18(4a))
party_recognition_BVerfG_decision_deadline_days_before: 59 (§ 18(4a))
nomination_submission_deadline_days_before: 69 (§ 19)
nomination_admission_decision_days_before: 58 (§§ 26(1), 28(1))

# Constituency nominations
party_constituency_signatures_established_party: 0 (§ 20(2) — only
  Land branch executive committee handwritten signatures required)
party_constituency_signatures_new_party: 200 eligible voters in
  the constituency (§ 20(2) third sentence)
nonparty_constituency_signatures: 200 eligible voters in the
  constituency (§ 20(3))
national_minority_party_signatures_exempt: yes (§ 20(2) fourth
  sentence)

# Land lists
party_land_list_signatures_established_party: 0 (§ 27(1) — only
  Land branch executive committee handwritten signatures required)
party_land_list_signatures_new_party: 1 per 1,000 eligible voters
  in the Land at the last Bundestag election, capped at 2,000
  (§ 27(1))
voter_grouping_land_lists_allowed: NO — § 27(1): "Land lists may
  only be submitted by political parties"
citizen_committee_land_lists_allowed: NO

# List composition
list_size_max: not statutorily capped
list_size_min: not statutorily fixed; if list runs out of
  candidates, remaining seats stay vacant per § 6(4)
list_ordering_rule: "recognisable order" set by submitter, by
  secret ballot at members'/delegates' assembly (§§ 27(3),
  27(5)/21(1))
gender_quota: none in BWahlG. § 55 (Reform Commission) tasked
  with proposing measures for "equal representation of men and
  women on the lists of candidates"; no statutory quota enacted
  to date.
residency_required: candidate residency not statutorily required
  beyond eligibility-to-stand under § 15
multiple_candidacy_restrictions:
  - candidate may appear in only one constituency (§ 20(1))
  - candidate may appear on only one Land list (§ 27(4))
  - candidate may not appear on a Land list AND as a non-party
    constituency Einzelbewerber (§ 27(4))
  - candidates of one party may not be members of another party
    (§ 21(1))
identifying_name_for_nonparty: required by § 20(4) — non-party
  constituency nominations "must contain an identifying name"
```

#### Notes

The party-vs-non-party boundary at the federal level is sharp:

- **Parties (registered)** can submit constituency nominations
  *and* Land lists.
- **Non-party (Einzelbewerber)** can submit only **constituency**
  nominations under § 20(3); they have no path to Land list seats.

Established parties (continuously represented by ≥5 members in
Bundestag or any Landtag) are exempt from signature requirements;
this is the **continuous-representation threshold**, a
significant practical incumbency advantage.

The **97-day / 79-day / 69-day / 58-day cascade** is a useful
drafting model: a fixed deadline backbone with each subsequent
authority deciding by a known date, plus an explicit BVerfG
appeal track for refused parties (§ 18(4a)).

For US implementation, three features are particularly notable:

1. **Continuous-representation incumbency advantage** (§ 18(2)) —
   exempts established parties from signature requirements. US
   ballot-access law generally treats all parties symmetrically
   under *Williams v. Rhodes*; the German asymmetry would need
   careful constitutional defense if adopted.
2. **Internal party democracy as a statutory requirement**
   (§ 21) — candidates must be selected at a members' or
   delegates' assembly by secret ballot, with timing windows
   tied to the legislative term. This intervenes in party
   internal governance to a degree no US ballot-access law does.
3. **Identifying name requirement for non-party nominations**
   (§ 20(4)) — the seed of a labeling regime, but the BWahlG
   does not regulate what an identifying name may be (no
   protection against deceptive labels analogous to a party
   name). This gap is filled at the local *Länder* level, which
   is where the project's most useful comparative work on
   non-partisan labeling will sit.

### C. Campaign finance

The substantive campaign-finance regime sits in the *Parteiengesetz*
(PartG) §§ 18–31a — public matching funds, donation disclosure,
absolute and relative funding caps. The BWahlG itself contains a
single provision — § 49b — addressing the analogous regime for
non-party constituency candidates.

#### Statutory text — § 18 PartG (State Funding Principles)

§ 18 establishes the public-funding regime for parties. Key
provisions (as set in current consolidated text; the figures are
indexed annually):

- **§ 18(1)**: state funding is a *partial* contribution to a
  party's constitutionally mandated activities; it is allocated on
  the basis of three criteria — electoral success at European,
  federal, and state-legislative level; membership and office-
  holder dues; and donations received.
- **§ 18(2)**: an **absolute upper limit** (*absolute Obergrenze*)
  on total annual public funding to all parties combined. Set in
  statute (€184,793,822 as the 2018 reference figure) and indexed
  annually 70%/30% to consumer prices and public-sector wages.
- **§ 18(3)**: per-vote payments. Currently:
  - €1.00 per valid vote for the first 4 million votes a party
    receives (in the most recent federal/European elections);
  - €0.83 per valid vote thereafter;
  - **€0.45 per €1.00 of private contributions** (membership
    dues, office-holder contributions, and donations from natural
    persons up to €3,300 per donor per year).
- **§ 18(4)**: eligibility threshold for any payment. A party must
  receive **at least 0.5%** of valid second votes at the most
  recent European or federal election, **or 1.0%** of valid second
  votes at the most recent state election in the relevant Land,
  to receive any state funding. Independent constituency
  candidates are eligible if they reached 10% of valid first
  votes in their district. National-minority parties are exempt
  from the eligibility threshold.
- **§ 18(5)** (relative cap): a party's state funding may not
  exceed its private income (membership dues, donations,
  office-holder contributions, etc.). This is the
  *Selbstfinanzierungsgrundsatz* — the principle that public
  funding tops up but does not replace private support.
- **§ 18(7)**: parties banned by the BVerfG (Article 21(2) GG)
  forfeit funding; a party excluded from state funding under
  Article 21(3) GG is excluded for six years (BVerfG ruling of
  January 2024 against *Die Heimat*).

The 2024 amendments to PartG (per OSCE 2025 Final Report) lowered
the immediate-disclosure threshold and tightened sponsorship and
third-party-campaigning rules.

#### Statutory text — § 25 PartG (Donations) — key provisions

§ 25 governs donations to parties. Key provisions:

- **§ 25(1)**: cash donations capped at **€1,000**. Members
  receiving donations on behalf of the party must forward them
  immediately to a designated finance officer.
- **§ 25(2)**: prohibited categories of donation include:
  - public bodies and parliamentary factions;
  - charitable organizations and foundations;
  - foreign donors (with exceptions for German citizens abroad,
    EU citizens, and non-Germans donating under €1,000);
  - professional associations passing through funds;
  - companies with more than 25% public ownership;
  - **anonymous donations exceeding €500**;
  - donations given as consideration for political or economic
    advantage;
  - donations solicited by third parties charging more than 25%
    commission.
- **§ 25(3)**: **annual disclosure threshold** — donations from a
  single donor totaling more than **€10,000 per year** must be
  reported with donor identification in the party's annual
  statement. **Immediate-publication threshold** — donations
  exceeding **€35,000** must be notified immediately to the
  Bundestag President, who publishes them as a Bundestag printed
  paper.
- **§ 25(4)**: prohibited donations must be forwarded to the
  Bundestag President promptly, no later than with the annual
  report. Sanctions: up to **three times the unlawfully obtained
  amount**.

#### Notes — annual disclosure thresholds and oversight gap

The €10,000 / €35,000 thresholds are the operative numbers in any
US-comparable analysis. Note three structural features that ODIHR
flagged as gaps in the 2025 Final Report (Recommendations 6, 21,
22, 24):

1. **No annual donation cap**: parties may receive donations of
   any amount, subject only to disclosure obligations. The OSCE
   recommendation cites Council of Europe Recommendation
   Rec(2003)4 advising "reasonable limits" on contributions.
2. **No independent oversight body**: oversight is performed by
   the President of the Bundestag through an administrative unit
   of ten employees with **no investigative authority**.
   Sanctions can be imposed (administrative orders contestable in
   court); but the unit cannot itself audit.
3. **No campaign-period reporting**: the PartG requires only
   annual reports submitted by 30 September of the following
   year, with delayed publication. Voters cannot consult
   contribution and expenditure data before voting.

For US implementation: the German model demonstrates that even a
well-regulated public-funding regime can have substantial
oversight gaps. A US adoption should pair statutory thresholds
with an **independent oversight body** — analogous to the FEC at
federal level — with explicit investigative authority.

#### Statutory text — § 49b (State Funds for Non-Party Constituency Nominations)

> (1) If candidates of a nomination submitted by eligible voters
> pursuant to sections 18 and 20 have obtained at least ten
> percent of the valid first votes cast in a constituency they
> will receive, per valid vote, four times the amount quoted in
> section 18 subsection (3), first sentence, number 1 of the
> Political Parties Act and increased until election day in
> accordance with section 18 subsection (3), third sentence, of
> the Political Parties Act. The funds are to be provided for in
> the federal budget.
>
> (2) The candidate must apply to the President of the German
> Bundestag in writing for the establishment and disbursement of
> state funds within two months from the day of the constituent
> assembly of the German Bundestag […].
>
> (3) The provisions of the Political Parties Act on absolute and
> relative upper limits do not apply.

#### Notes

§ 49b is a small but instructive provision. It establishes a
**performance-based public funding floor** for non-party
constituency candidates: clear a 10% threshold and the federal
budget provides four times the per-vote rate that the
*Parteiengesetz* sets for parties.

The 10% threshold is high enough that very few independents
qualify in practice, but the *existence* of the rule is the
analytically interesting feature: federal law extends a fragment
of the public-funding regime to non-party candidates, breaking
what could otherwise be a hard partisan/non-partisan boundary.
For US implementation in non-partisan local contexts, this is a
useful structural model.

### D. EMB (Electoral administration)

§§ 8–11 BWahlG. Decentralized structure (§ 8(1)):

- *Bundeswahlleiterin* (Federal Returning Officer) and Federal
  Electoral Committee for the electoral area;
- *Landeswahlleiter* (Land Returning Officer) and Land Electoral
  Committee for each Land;
- *Kreiswahlleiter* (Constituency Returning Officer) and
  Constituency Electoral Committee for each of 299 constituencies;
- Electoral Officer and Electoral Board for each polling district;
- Electoral Officer(s) and Electoral Board(s) per constituency for
  postal ballot results.

The Bundeswahlleiterin is currently held by the President of the
Federal Statistical Office.

### E. Vote count, certification, recounts, dispute resolution

#### Statutory text — § 37 (Establishment of the Election Result in the Polling District)

> After polling has closed, the Electoral Board establishes how
> many votes have been cast in the polling district for the
> individual constituency nominations and Land lists.

#### Statutory text — § 39 (Invalid Votes), excerpts

> (1) Votes are invalid if the ballot paper
>
> 1. has not been produced by the government,
> 2. contains no markings,
> 3. is valid for another constituency,
> 4. does not clearly show the voter's intent,
> 5. contains any addendum or reservation.
>
> In the cases specified in numbers 1 and 2, both votes are
> invalid; in the case specified in number 3, only the first vote
> is invalid if the ballot paper is valid for another constituency
> in the same Land. […] Where only one vote has been cast on the
> ballot paper, the missing vote is considered invalid.

#### Statutory text — §§ 41–42 (Establishment in Constituency and for Land Lists)

> § 41. The Constituency Electoral Committee establishes how many
> votes have been cast in the constituency for the individual
> constituency nominations and Land lists.
>
> § 42(1). The Land Electoral Committee establishes how many votes
> have been cast in the Land for the individual Land lists. The
> Federal Electoral Committee determines how many seats go to the
> individual Land lists.
>
> § 42(3). The Federal Electoral Committee establishes the
> election result and conclusively determines which candidates
> have been elected. The Federal Returning Officer notifies the
> candidates.

#### Statutory text — § 49 BWahlG (Contestation)

> Any decisions and measures directly affecting the electoral
> procedure may only be contested by means of the legal remedies
> provided by this Act and the Federal Electoral Regulations and
> by way of the electoral scrutiny procedure.

#### Statutory text — *Wahlprüfungsgesetz* (Law on the Scrutiny of Elections)

The *Wahlprüfungsgesetz* implements Article 41 GG and BWahlG § 49.
Key provisions:

> **§ 1(1)**: "Über die Gültigkeit der Wahlen zum Bundestag und
> die Verletzung von Rechten bei der Vorbereitung oder
> Durchführung der Wahl … entscheidet vorbehaltlich der
> Beschwerde nach Artikel 41 Abs. 2 des Grundgesetzes der
> Bundestag."

(*The Bundestag decides — subject to appeal under Article 41(2) GG
— on the validity of elections to the Bundestag and on
infringements of rights in the preparation or conduct of the
election.*)

§ 1(2) provides that if rights of complainants were infringed but
the election is not declared invalid, the Bundestag must
formally establish the infringement.

> **§ 2**:
>
> (1) Die Prüfung erfolgt nur auf Einspruch.
>
> (2) Den Einspruch kann jeder Wahlberechtigte, jede Gruppe von
> Wahlberechtigten und in amtlicher Eigenschaft jeder
> Landeswahlleiter, der Bundeswahlleiter und der Präsident des
> Bundestages einlegen.
>
> (3) Der Einspruch ist schriftlich beim Bundestag einzureichen
> und zu begründen; bei gemeinschaftlichen Einsprüchen soll ein
> Bevollmächtigter benannt werden.
>
> (4) Der Einspruch muß binnen einer Frist von zwei Monaten nach
> dem Wahltag beim Bundestag eingehen. Werden dem Präsidenten des
> Bundestages nach Ablauf dieser Frist in amtlicher Eigenschaft
> Umstände bekannt, die einen Wahlmangel begründen könnten, kann
> er innerhalb eines Monats nach Bekanntwerden dieser Umstände
> Einspruch einlegen.

(*Translation: (1) The examination occurs only upon objection. (2)
Any eligible voter, any group of eligible voters, and in official
capacity any Land Returning Officer, the Federal Returning
Officer, and the President of the Bundestag may lodge an
objection. (3) The objection must be submitted in writing to the
Bundestag with reasons; for joint objections an authorised
representative should be designated. (4) The objection must be
received by the Bundestag within two months after election day;
if circumstances suggesting an electoral defect become known to
the President of the Bundestag in his official capacity after
expiry of this deadline, he may lodge an objection within one
month of learning of those circumstances.*)

§ 13 governs the Bundestag's decision on the Wahlprüfungsausschuss
(election scrutiny committee) recommendation:

> § 13(1): "Der Bundestag beschließt über den Antrag des
> Ausschusses mit einfacher Mehrheit. Soweit er ihm nicht
> zustimmt, gilt er als an den Ausschuß zurückverwiesen. Dabei
> kann der Bundestag dem Ausschuß die Nachprüfung bestimmter
> tatsächlicher oder rechtlicher Umstände aufgeben."

(*The Bundestag decides on the committee's motion by simple
majority. To the extent that the Bundestag does not adopt the
motion, it is deemed referred back to the committee. The Bundestag
may direct the committee to re-examine specific factual or legal
circumstances.*)

§ 18 governs appeal to the BVerfG:

> "Für die Beschwerde an das Bundesverfassungsgericht gelten die
> Vorschriften des Gesetzes über das Bundesverfassungsgericht."

(*The provisions of the Federal Constitutional Court Act apply to
the appeal to the Federal Constitutional Court.*)

#### Statutory text — § 69 BWO (Vote Counting)

The *Bundeswahlordnung* (Federal Electoral Regulations, the
implementing instrument authorized by BWahlG § 52) sets the
detailed counting procedure. § 69 specifies the count at the
polling-station level, including the **stack-sorting protocol**:

- Ballots with valid first and second votes for candidates of the
  same party form one stack;
- Ballots with **split votes** (first vote for one party,
  second for another) form a separate stack;
- Ballots with no marks form a third stack;
- Disputed ballots are set aside for review.

After the polling-station chair (*Wahlvorsteher*) announces stack
contents aloud, two assistants count each stack under mutual
supervision. The split-vote stack is then re-sorted by second
votes and again by first votes to produce final tallies. The
Electoral Board adjudicates disputed ballots. Any board member
may demand a recount before the record is signed; the reasons
must be documented.

#### Notes — the German contestation chain

```
2 months              → Bundestag receives Einspruch (§ 2(4) WPrüfG)
↓
Wahlprüfungsausschuss → Examination by 9-member committee
↓
Bundestag plenary    → Vote by simple majority (§ 13(1) WPrüfG)
↓
2 months              → Beschwerde to BVerfG (Art. 41(2) GG)
                        per § 18 WPrüfG and BVerfGG
```

OSCE notes that this process can take **6 months to 2 years** in
practice; ODIHR Recommendation 5 calls for shorter statutory
deadlines.

The 2023 federal election produced the **first-ever partial
invalidation** of a federal election: the BVerfG declared the
2021 election invalid in 455 of 2,256 polling districts in Berlin
in December 2023, ordering repeat elections held on 11 February
2024.

#### Notes

The German federal scrutiny procedure (*Wahlprüfungsverfahren*)
runs as follows:

1. The **Bundestag itself** decides election contests in the
   first instance, under Article 41 of the Basic Law and the
   *Wahlprüfungsgesetz* (separate statute).
2. **Appeal to the BVerfG** is then available under Article 41(2)
   GG.

The aggregation chain is **strictly hierarchical**:
polling-district board → Constituency Returning Officer →
Constituency Electoral Committee → Land Electoral Committee →
Federal Electoral Committee. The Federal Electoral Committee
issues the conclusive determination of which candidates are
elected (§ 42(3)).

Three features for US implementation:

1. **Government-produced ballots are a per-se validity rule**
   (§ 39(1) no. 1): a ballot not produced by the government is
   invalid in toto. This is a strong administrative-uniformity
   principle.
2. **Single-vote-cast ballots are partially valid** (§ 39(1)
   final sentence): voters may cast one vote without the other
   being treated as invalid. This is friendlier to voter intent
   than US plurality-style strict-validity rules.
3. **Bundestag-as-first-instance for election contests** (§ 49,
   Art. 41 GG): the legislative body decides its own membership
   contests. US practice splits this between courts and
   chambers; the German model concentrates the decision and is
   probably less portable to the US.

### F. Media access

Not in the BWahlG; governed by the *Medienstaatsvertrag* and
party-broadcast allocations under public-broadcaster law.

### G. (Districting law — captured under Component 1, § 3)

---

## 5. PROSeS performance diagnostic

Anchored on the OSCE/ODIHR Election Assessment Mission Final
Report on the 23 February 2025 Bundestag election (Warsaw, 23 June
2025; cached locally at
`sources/germany/OSCE_ODIHR_Germany_2025_election_report.pdf`).
The 2025 election was the first under the 2023 reform and the
first applying the BVerfG-modified threshold rule, so it is the
key empirical reference for evaluating the current regime.

### Process Design

**Public participation.** ODIHR concluded that the Federal
Electoral Committee held its two pre-election sessions in public,
with minutes and video recordings made available online.
**However, *Land* Electoral Committee sessions were closed**
("in order to abide by the personal data protection rules, as
among others, they dealt with the verification of supporting
signatures"); minutes were not available. ODIHR recommended that
the election administration at all levels hold public sessions
and publish draft agendas and minutes (Recommendation 11).

**Probity and impartiality.** The decentralized four-tier
structure — Federal Electoral Committee, 16 *Land* Electoral
Committees, 299 Constituency Electoral Committees, ~65,000
Electoral Boards — operated without significant integrity
concerns. ODIHR found that "the election authorities at all
levels acted professionally and efficiently" and that "all ODIHR
EAM interlocutors expressed a high level of trust in the integrity
and professionalism of the election administration, including in
the conduct of election day."

**Accountability.** Election contests run through the
*Wahlprüfungsverfahren* (BWahlG § 49; *Wahlprüfungsgesetz*).
Several ODIHR interlocutors flagged "potential conflict of
interests in parliamentarians deciding upon the validity of their
own mandate." ODIHR found that **investigations can take between
six months and one year, with FCC appeals taking up to two years**;
ODIHR recommended that timely deadlines be established
(Recommendation 5).

### Resource Investment

**Sustainability.** Funding is decentralized: the federal
government reimburses *Länder* and municipalities for election
costs (§ 50 BWahlG), with fixed per-voter sums (currently €0.56
per eligible voter in municipalities under 100,000 and €0.87
above; § 50(3)). Public funding for parties is set by the
*Parteiengesetz* and is indexed annually (€1.18 per vote for the
first 4 million votes; €0.97 thereafter, plus matching for private
contributions).

**Transparency.** 2024 amendments to the *Parteiengesetz*
introduced separate reporting obligations for sponsorship,
defined third-party campaigning, and **lowered the immediate-
disclosure threshold from €50,000 to €35,000** (annual disclosure
threshold: €10,000). Reports are submitted by 30 September of the
following year and published with significant delay; disaggregated
campaign-period reports are not required.

**Legitimacy.** No annual cap on donations. ODIHR recommended
introducing one (Recommendation 21). Foreign donations are
restricted to €1,000 except from German citizens abroad, EU
citizens, and EU-based companies majority-owned by EU citizens;
anonymous donations capped at €500.

**Contingency.** The 2024 election was triggered by a 16 December
2024 vote of no confidence; the postal-voting preparation window
collapsed from approximately 6 weeks to 14 days. ODIHR observed
that the election administration mitigated the compressed timeline
through prioritization (overseas postal ballots first) and adding
postal voting centers, but flagged that the deadlines may have
disenfranchised some overseas voters. Several interlocutors
opined that "the mechanism to enfranchise German citizens abroad
is in dire need of reform."

### Service Output Quality

**Convenience.** Postal voting available since 2008 to all voters
without justification. **Postal share dropped from 47.3% in 2021
to 37% in 2025**, plausibly reflecting the early-election
compression. 65,000 polling stations on election day; 25,000
postal voting centers operating in the two weeks prior. ID checks
were not uniformly applied across *Länder* — Berlin checked ID
*after* the voter marked the ballot; Brandenburg checked
*before*. ODIHR recommended uniform checking of ID and voter-list
entry prior to issuing the ballot (Recommendation 13).

**Accuracy.** Final invalid-vote rates were **0.8% (first vote)
and 0.6% (second vote)** — among the lowest globally and reflecting
the simplicity of the two-vote ballot under § 30 BWahlG. ODIHR
EAM observed orderly counting and noted no major incidents on
election day. Isolated technical errors with double polling cards
in Berlin and North Rhine-Westphalia were addressed by
invalidating the duplicate cards.

**Enforcement.** The four-tier electoral-body structure (BWahlG
§§ 8–11) applies and verifies rules consistently. The Federal
Electoral Committee's binding determination of party status
(BWahlG § 18(4)) is rule-bound and reviewable by the BVerfG; in
2025, of 66 parties applying, 41 were registered, 25 denied; one
denial was appealed to the FCC and rejected on formal grounds.

**Efficiency.** Election costs are per-voter indexed (§ 50(3)) and
formally reviewed annually by the President of the Federal
Statistical Office. The compressed 2025 timeline was met without
budget overruns.

### Service Outcomes

**Voter turnout** at the 23 February 2025 election was **82.5%
(49,928,653 of 60,510,631 eligible voters)** — the highest
turnout in federal parliamentary elections since reunification
in 1990.

**Register accuracy and completeness.** ODIHR reported that "no
municipality met by the ODIHR EAM had received complaints
regarding omissions or inaccuracies in the voter lists. All ODIHR
EAM interlocutors expressed confidence in the accuracy of the
voter register and inclusiveness of the voter lists." Voter
registration is **passive** — drawn from municipal civil
registers; no opt-in or active step required.

**Equity.** Two notable equity concerns:

- **Gender representation**: 32.4% women in the new 630-seat
  Bundestag (204 of 630). This is a **decrease from 35.3% in the
  2021 parliament**. Among 4,506 candidates, 31.6% were women.
  35% of party-list candidates were women; only 27% of district
  candidates. The legislation contains no temporary special
  measures (no statutory quota); a parity proposal failed to
  gather sufficient support during the 2023 reform debate.
- **Online violence against women candidates** was widely
  reported; ODIHR cited a HateAid study finding 63% of women
  politicians in Germany affected by violence vs 53% of men.

**Diffuse impact**: ODIHR cited disinformation campaigns
(including documented Russian-linked campaigns "Storm 1516",
"Doppelgänger", "Operation Overload") and noted "deterioration
of civic space" reported by interlocutors. The CDU/CSU
post-election parliamentary inquiry questioning political
neutrality of civil-society organizations involved in protests
"was perceived as an attack on civic engagement."

**Cost per vote cast**: not directly published in OSCE report;
to be derived from Bundeswahlleiterin financial statements.

#### The Zweitstimmendeckung in operation

Under the 2023 reform, **23 candidates won the most first votes
in their constituencies but did not receive a Bundestag mandate**
(18 from CDU, 5 from CSU) because their parties' second-vote
share did not support the seat. This is the operational signature
of the reform: § 1(3) BWahlG produced the predicted result of
unseated constituency winners.

#### The Grundmandatsklausel transitional rule in operation

The Left (Die Linke) won 8.8% of second votes nationally — above
the 5% threshold, so the transitional rule was not necessary in
its case. **In the 2021 election, by contrast, Die Linke received
4.9% of second votes but won 3 constituency seats**, satisfying
the (then-still-applicable) Grundmandatsklausel and so retaining
parliamentary representation. Without the transitional rule
restored by BVerfG 2024, the Left would have been excluded from
the Bundestag in 2021 — and the BVerfG cited this kind of result
as part of the constitutional defect.

### Stakeholder Satisfaction

**Citizen satisfaction**: not directly surveyed in the OSCE
report, but turnout (82.5%) and trust expressed by interlocutors
suggest robust satisfaction with election administration.

**Staff satisfaction**: ~675,000 poll workers were recruited and
trained; ODIHR did not separately survey staff satisfaction.
Training was assessed as "comprehensive, well attended and
contained interactive elements."

**Parties / civil society**: high level of trust in
administration was the dominant report. Concerns were
substantive: tight signature deadlines for smaller parties, the
restriction against signing in support of more than one electoral
list (contrary to ODIHR good practice), online violence against
women and migrant-origin candidates, and disinformation. ODIHR
filed Recommendation 17 to remove the single-list signature
restriction.

### Key recommendations from OSCE/ODIHR (final report, 23 June 2025)

Priority recommendations (selection):
- Comprehensive legislative reform implementing outstanding ODIHR
  recommendations (Rec. 1).
- Effective temporary special measures for women's participation,
  including legislative gender quotas (Rec. 2).
- Effective dispute resolution: judicial review with public
  hearing at all stages, timely deadlines (Rec. 5).
- Independent campaign finance oversight body with sufficient
  resources and investigative powers (Rec. 6).
- Periodic, detailed campaign-finance reporting before election
  day (Rec. 7).
- Publish results disaggregated by polling station (Rec. 8).
- Explicitly guarantee citizen and international observer access
  in legislation (Rec. 9).

---

## 6. Venice Commission compliance check

```
universal_suffrage:    compliant  # § 1(1); GG Art. 38(1)
equal_suffrage:        compliant
free_suffrage:         compliant
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant  # GG Art. 39 — every 4 years
fundamental_rights:    compliant
regulatory_stability:  medium     # 2023 reform + 2024 BVerfG
                                  # ruling produced mid-cycle
                                  # uncertainty; transitional rule
                                  # awaiting legislative replacement
procedural_safeguards: compliant
```

The five Venice principles are textually enshrined in § 1(1)
itself: "general, direct, free, equal and secret ballot."

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| Two-vote MMP design | **Universal** | The two-vote architecture is reproducible in any federal/state system. |
| Sainte-Laguë / Webster allocation | **Universal** | Webster is already used for US House apportionment among states. |
| Two-level distribution (Ober-/Unterverteilung) | **Hybrid** | Substantively universal; procedurally presupposes a federal/state structure. The Land tier maps cleanly onto US states. |
| 5% nationwide threshold | **Particular** | Rooted in Weimar-era trauma about splinter parties. US adoption would need its own legitimating narrative. |
| *Grundmandatsklausel* | **Particular** | German-specific compromise between systemic threshold and constituency wins. Useful as a policy concept; not directly portable. |
| Zweitstimmendeckung | **Universal** | The mechanism for solving overhang is portable; the specific implementation is German. |
| Independent constituency candidacy with no list-tier access (§ 1(4); § 20(3)) | **Universal** | Clean drafting solution to the partisan/non-partisan boundary at federal level. |

### Top three takeaways for US state-legislature implementation

1. **MMP can be statutorily compact.** Six sections of the BWahlG
   (§§ 1–6, 24 paragraphs total) define the entire electoral
   system. A US state-legislature MMP statute can be similarly
   compact; complexity belongs in implementing regulations
   (analogous to the *Bundeswahlordnung*), not in primary
   legislation.

2. **The allocation formula can be expressed purely procedurally.**
   § 5 specifies Sainte-Laguë in three subsections without using
   the eponym. The calculation is reproducible from the statutory
   text alone — a useful drafting model for US adoption, where
   familiarity with formula names cannot be assumed.

3. **Threshold design must account for outliers.** Germany's
   experience with the *Grundmandatsklausel* shows that a pure
   percentage threshold creates political legitimacy problems
   when a party with significant local support falls just short.
   Any US adoption should anticipate this with a fallback pathway
   analogous to the Grundmandatsklausel — and should expect the
   pathway itself to be politically and constitutionally
   contested.

---

## 8. Sources

### Primary

- *Bundeswahlgesetz* (BWahlG) in der Fassung der Bekanntmachung
  vom 23. Juli 1993 (BGBl. I S. 1288, 1594), zuletzt geändert
  durch Artikel 1 des Gesetzes vom 7. März 2024 (BGBl. 2024 I
  Nr. 91). <https://www.gesetze-im-internet.de/bwahlg/>
- *Federal Elections Act* (official English translation of BWahlG),
  Federal Returning Officer.
  <https://www.bundeswahlleiterin.de/en/dam/jcr/4ff317c1-041f-4ba7-bbbf-1e5dc45097b3/bundeswahlgesetz_engl.pdf>.
  Cached locally: `sources/germany/Bundeswahlgesetz_EN_official.pdf`.
- *Grundgesetz für die Bundesrepublik Deutschland* (GG), Articles
  38–41.
- *Parteiengesetz* (PartG).
- *Bundeswahlordnung* (BWO) — implementing regulation.
- BVerfG, Urteil vom 30. Juli 2024 — 2 BvF 1/23 et al. —
  *Wahlrechtsreform 2023*. Press release in English:
  <https://www.bundesverfassungsgericht.de/SharedDocs/Pressemitteilungen/EN/2024/bvg24-064.html>

### Secondary (orientation)

- Deutscher Bundestag, "Das geltende Wahlrecht nach der Reform
  2023". <https://www.bundestag.de/parlament/wahlen/wahlrecht-inhalt-975000>
- Bundeszentrale für politische Bildung (bpb), "FAQ:
  Wahlrechtsreform zur Verkleinerung des Bundestages".
  <https://www.bpb.de/kurz-knapp/hintergrund-aktuell/520271/>

### Outstanding gaps

The following are nice-to-have but the profile is now substantively
complete on the primary statute:

- BVerfG, 2 BvF 1/23 — full text of the ruling. The press release
  reasoning is incorporated into Component 3; the full opinion
  would deepen the analysis on the proportionality/necessity
  test, but the substantive result and its drafting implications
  are captured.
- *Bundeswahlordnung* (BWO) — additional sections beyond § 45 and
  § 69 (e.g., § 67 result determination, §§ 76–78 constituency
  and Land-level result certification, §§ 34–41 implementing
  detail on candidate and list nomination forms).
- *Parteiengesetz* §§ 19, 19a (administration of the funding
  award), § 23 (annual financial report content), § 31a
  (sanctions for irregular contributions).

### Resolved in iterations to date

**2026-05-04** (initial profile):
- §§ 1, 3, 4, 5, 6 quoted in Components 1, 2, 3.

**2026-05-05** (gap-filling, first pass):
- §§ 12, 13, 14, 15 quoted in Connected Area A.
- §§ 18, 19, 20, 21, 27 quoted in Connected Area B.
- § 30, § 34 quoted in Component 2 / ballot mechanics.
- § 49b quoted in Connected Area C.
- §§ 37, 39, 41, 42, 49 quoted in Connected Area E.
- *Parteiengesetz* § 2 (definition of "party") quoted in
  Connected Area B.
- BVerfG 2 BvF 1/23 (30 July 2024) reasoning summary added to
  Component 3 (from the official English press release).
- BVerfG ruling of 22 January 2025 on signature requirements
  noted.
- PROSeS section populated from OSCE/ODIHR Final Report on the
  23 February 2025 Bundestag election.
- Worked example added to Component 3 using 2025 election
  results.

**2026-05-05** (second pass, remaining outstanding):
- *Parteiengesetz* §§ 18 (state funding formula) and 25
  (donations) quoted in Connected Area C.
- *Wahlprüfungsgesetz* §§ 1, 2, 13, 18 quoted in Connected Area E.
- *Bundeswahlordnung* § 45 (ballot paper specifications)
  quoted in Component 2.
- *Bundeswahlordnung* § 69 (vote counting protocol) quoted in
  Connected Area E.
- 2024 Berlin partial-invalidation precedent (BVerfG December
  2023) noted in Connected Area E.
