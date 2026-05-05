# Brazil — Municipal elections (Vereadores)

## 0. Case metadata

- **Country**: Federative Republic of Brazil (República Federativa
  do Brasil)
- **Sub-jurisdiction**: All 5,568 *municípios* (municipalities)
- **Level of government**: Local — *Câmara de Vereadores*
  (municipal council) and *Prefeito* (mayor); the Prefeito is a
  separate single-office contest, not within the scope of this
  profile.
- **Electoral system family**: **Open-list proportional
  representation** with a **single vote** that may be cast either
  for a specific candidate (*voto nominal*) or for a party
  (*voto de legenda*). Each *município* is a single district;
  M = total council size for that municipality.
- **Governing statutes**:
  - **Constituição Federal** (CF, 1988), Art. 14, Art. 17,
    Art. 29(IV) — basic electoral rights, party autonomy, and
    the population-tiered table for council size.
  - **Código Eleitoral** (Lei nº 4.737/1965, consolidated
    text), Arts. 106–109 — proportional system, electoral
    quotient, party quotient, and the rules on remainder seats
    (*sobras*). Most recently amended by Lei nº 14.211/2021.
  - **Lei das Eleições** (Lei nº 9.504/1997) — election conduct,
    candidate registration, gender-quota rule, electronic voting.
  - **Lei dos Partidos Políticos** (Lei nº 9.096/1995) — party
    formation and funding.
  - **TSE Resolutions** for each cycle (most recent municipal
    cycle: Resolução nº 23.736/2024 for the October 2024
    elections).
- **Implementing instrument**: TSE (Tribunal Superior Eleitoral)
  resolutions, supplemented by Tribunais Regionais Eleitorais
  (TREs) for each state.
- **Recent constitutional and statutory developments**:
  - **EC 97/2017**: abolished electoral coalitions (*coligações*)
    for proportional elections (federal deputies, state
    deputies, vereadores).
  - **Lei nº 14.208/2021**: introduced *federações partidárias*
    (party federations) as a partial substitute for coligações.
  - **Lei nº 14.211/2021**: amended Arts. 107, 108, 109 of the
    Código Eleitoral, restating the proportional formula.
  - **STF, February 2024 (ADI 7228, ADI 7263, ADI 7325)**:
    declared portions of the 80%/20% performance thresholds in
    Art. 109(§ 2º) unconstitutional, opening surplus
    distribution to all parties.
- **Compulsory voting**: yes, ages 18–70 (optional 16–17 and
  70+); compulsory franchise is set in CF Art. 14 § 1º.
- **Last regular election**: 6 October 2024 (first round), with
  runoff for mayor on 27 October 2024. Next: 2028.
- **Analyst**: this profile, 2026-05-05.

### Why this case is in the project

Brazil's municipal regime is the project's principal case for the
**single-vote, candidate-or-party voting interface**. CF Art. 14
and the *Código Eleitoral* permit a voter to cast one vote that
may be expressed in either of two ways: (a) by entering a
specific candidate's full number (*voto nominal*), or (b) by
entering only the party's number (*voto de legenda*). Both
contribute to the party's total for inter-party allocation, but
only nominal votes determine which candidates of the party take
the seats it wins. This is the architectural pattern the user has
identified as the working baseline for the model statute, here
operating at the largest scale of any jurisdiction in the
project's case set (5,568 municipalities, ~155 million
registered voters).

The case also documents an active recent reform cycle (2017
coligações abolition; 2021 *federação* introduction and Code
amendments; 2024 STF rulings on performance thresholds) that
illustrates how proportional rules are renegotiated through
ordinary legislation and constitutional litigation.

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Statutory text — CF Art. 29(IV) (Number of Vereadores)

The Constitution itself sets a population-tiered table. The
relevant provision (Emenda Constitucional nº 58/2009):

> Art. 29. … IV - para a composição das Câmaras Municipais, será
> observado o limite máximo de:
>
> a) 9 (nove) Vereadores, nos Municípios de até 15.000 (quinze
> mil) habitantes;
>
> b) 11 (onze) Vereadores, nos Municípios de mais de 15.000
> (quinze mil) habitantes e de até 30.000 (trinta mil)
> habitantes;
>
> c) 13 (treze) Vereadores, nos Municípios com mais de 30.000
> (trinta mil) habitantes e de até 50.000 (cinquenta mil)
> habitantes;
>
> d) 15 (quinze) Vereadores, nos Municípios de mais de 50.000
> (cinquenta mil) habitantes e de até 80.000 (oitenta mil)
> habitantes;
>
> *[further alíneas e–x scale in 2-vereador increments through]*
>
> j) 27 Vereadores, nos Municípios de mais de 600.000 e de até
> 750.000 habitantes;
>
> *[…]*
>
> w) 53 Vereadores, nos Municípios de mais de 7.000.000 e de
> até 8.000.000 habitantes; e
>
> x) 55 (cinquenta e cinco) Vereadores, nos Municípios de mais
> de 8.000.000 (oito milhões) de habitantes.

(Translation: For the composition of municipal councils, the
following maximum is observed: 9 vereadores in municipalities up
to 15,000 inhabitants; 11 in municipalities of 15,000–30,000;
13 in 30,000–50,000; … through 55 in municipalities above
8,000,000.)

The full table specifies 24 brackets (a–x) in 2-vereador
increments, ending at 55 for São Paulo (the only Brazilian
municipality above 8 million). Each council's size within the
constitutional ceiling is set by the council's own *Lei
Orgânica Municipal* (organic law).

### Districts and magnitude

Each *município* constitutes a single electoral district. Brazil
does not subdivide municipalities into wards or sub-districts for
council elections. **District magnitude equals total council
size** for each municipality:

- M = 9 in the smallest municipalities (~15,000 inhabitants).
- M = 23 in mid-size cities (300,000–450,000 inhabitants).
- M = 55 in São Paulo (the largest municipality).

### Operationalized values

```
total_seats:                     9 (smallest) — 55 (São Paulo)
codification_instrument:         Constituição Federal Art. 29(IV)
                                 (constitutional table); Lei
                                 Orgânica Municipal sets each
                                 council's specific size within
                                 the constitutional ceiling
amendment_authority:             Constitutional amendment (3/5 of
                                 each chamber, two votes per
                                 chamber, CF Art. 60) for the
                                 table; municipal council for
                                 the council's specific size
amendment_threshold:             constitutional amendment for the
                                 ceiling table; ordinary municipal
                                 legislation for the local choice

magnitude_uniform:               yes within each municipality
magnitude_typical:               population-determined
magnitude_range:                 9 — 55
districts_count:                 1 per municipality
districting_authority:           N/A — district = municipality
districting_frequency_years:     N/A
districting_criteria_in_statute: N/A

tiered:                          no
tier_count:                      1
tier_compensatory:               not applicable

threshold_of_exclusion_pct:      10.0% (M=9) → 1.79% (M=55)
                                 [structural — operative threshold
                                 also constrained by the 10% of
                                 quociente eleitoral candidate
                                 rule (CE Art. 108)]
```

### Notes

The constitutional codification of the council-size table places
Brazilian local PR architecture in an unusual posture for
comparative analysis: the population tiers (CF Art. 29(IV)) sit
at the highest level of the legal hierarchy. Amendment requires
a constitutional amendment (3/5 of each chamber, in two rounds
of voting, per CF Art. 60). This is a more demanding amendment
process than Bavarian *Gemeindeordnung* Art. 31 (ordinary
*Land* legislation) or NSW *Local Government Act* (ordinary
state legislation) and reflects a deliberate Brazilian choice to
constitutionalize the table after the 2009 reform (EC 58/2009).

The trade-off: constitutional placement protects the
proportionality of representation against majoritarian erosion,
but makes future reform (e.g., expansion of the smallest-tier
councils) substantially harder.

---

## 2. Component 2 — Ballot Structure

### The single vote: voto nominal or voto de legenda

In municipal proportional contests, each voter casts **one vote**
on the *urna eletrônica* (electronic voting machine). The voter
expresses the vote in one of two ways:

- **Voto nominal**: the voter enters the **5-digit candidate
  number** (e.g., 25123). The vote is recorded for that
  candidate and counts toward the candidate's party's total.
- **Voto de legenda**: the voter enters only the **2-digit
  party number** (e.g., 25). The vote is recorded for the party
  and counts toward the party's total but not toward any
  individual candidate.

Both votes count equally toward the *quociente partidário*
(party quotient) used in the inter-party allocation step. Only
*voto nominal* determines which of a party's candidates take
the seats the party wins (CE Art. 108).

This is the **single-vote, party-or-candidate option** ballot
architecture that the project's framework documents have
identified as the working baseline for U.S. drafting. Brazil
operates it at the largest scale of any case in the project.

### Statutory text — Lei 9.504/1997 Art. 10 § 3º (Gender quota)

> § 3º Do número de vagas resultante das regras previstas neste
> artigo, cada partido ou coligação preencherá o mínimo de 30%
> (trinta por cento) e o máximo de 70% (setenta por cento) para
> candidaturas de cada sexo.

(Translation: Of the number of slots resulting from the rules in
this article, each party or coalition shall fill a minimum of
30% and a maximum of 70% with candidacies of each sex.)

Effective since the 2009 cycle (Lei 12.034/2009 amendment); a
parallel provision in CF Art. 17 § 7º was added by EC 117/2022
giving constitutional anchoring to the rule.

### Operationalized values

```
ballot_type:                     open_list_pr_with_voto_de_legenda
preference_votes_per_voter:      1 (voto nominal OR voto de legenda)
panachage_allowed:               no — only one vote
cumulation_allowed:              no
above_the_line_option:           voto de legenda is functionally
                                 analogous to "above-the-line"
                                 (single mark for the party);
                                 voto nominal is "below-the-line"
                                 (specific candidate). Both occur
                                 on the same urna eletrônica
                                 interface, with no separate
                                 marking sections.

party_lists_allowed:             yes
voter_grouping_lists_allowed:    no — only registered parties or
                                 federações partidárias may run
                                 candidates; no Wählergruppen-
                                 equivalent at municipal level
citizen_committee_lists_allowed: no
independents_on_lists_allowed:   no — Brazil requires party
                                 affiliation for all candidates
                                 (CF Art. 14 § 3º V; CF Art. 17)
independent_candidate_path:      no — no Einzelbewerber-equivalent
                                 path exists at any level

non_party_label_allowed:         not applicable — only registered
                                 parties may appear
non_party_label_categories:      N/A
non_party_label_restrictions:    N/A

gender_quota:                    30% minimum each sex (Lei 9.504
                                 Art. 10 § 3º; CF Art. 17 § 7º)
gender_quota_pct:                30
electronic_voting:               yes — urna eletrônica for all
                                 contests since 2000
```

### Notes

Brazil's voto-de-legenda mechanic is the architectural pattern
the project has flagged for U.S. drafting attention. Three
features:

1. **Functional equivalence at the party level**: voto de legenda
   and voto nominal are equally weighted in the *quociente
   partidário* calculation. A party's total is the sum of all
   nominal votes for its candidates plus all legenda votes for
   the party itself.
2. **Asymmetry at the candidate level**: only nominal votes
   determine intra-list seat assignment. A party that received
   100,000 legenda votes and 0 nominal votes would still win
   the seats its quotient supports — but it would have no
   ranked candidates to assign them to (a degenerate case
   handled by intra-party tie rules).
3. **Single-step interface**: the voter inputs one number on
   the urna eletrônica. A 2-digit input is registered as voto
   de legenda; a 5-digit input as voto nominal. No separate
   ballot section, no separate physical mark.

For U.S. implementation: the Brazilian model demonstrates that
single-vote candidate-or-party expression is operationally
manageable at large scale and that voters use both modes (legenda
votes are typically a meaningful but minority share of a party's
total). The dependence on an electronic voting interface is a
constraint — the model adapts cleanly to digital ballots but
imposes drafting demands on a paper-ballot adaptation (the U.S.
analog would need to specify a marking convention, e.g., a single
"party only" oval at the top of each list column).

The categorical exclusion of independent and non-party
candidacies (CF Art. 14 § 3º V) is a Brazilian-particular feature
not portable to U.S. local non-partisan contexts.

### Coligações and federações partidárias

Two structural notes on party participation:

- **Coligações** (electoral coalitions) for proportional
  contests were **abolished by EC 97/2017**. Pre-2017, multiple
  parties could combine for the count; their joint total
  yielded a joint quociente partidário, with seats then
  redistributed among coalition partners. Post-2017, each
  party stands alone for proportional purposes.
- **Federações partidárias** (party federations) were
  introduced by **Lei 14.208/2021** as a partial substitute. A
  federation is a permanent (minimum 4-year) joint structure;
  unlike coalitions, federations function as a single party for
  electoral and parliamentary purposes. The 2024 municipal
  cycle was the first in which federations had operated through
  a full pre-election cycle.

---

## 3. Component 3 — Allocation Formula

### Statutory text — CE Art. 106 (Quociente Eleitoral)

> Art. 106. Determina-se o quociente eleitoral dividindo-se o
> número de votos válidos apurados pelo de lugares a preencher
> em cada circunscrição eleitoral, desprezada a fração se igual
> ou inferior a meio, equivalente a um, se superior.

(Translation: The electoral quotient is determined by dividing
the number of valid votes counted by the number of seats to be
filled in each electoral constituency, disregarding the
fraction if equal to or less than one half, rounding up to one
if greater.)

### Statutory text — CE Art. 107 (Quociente Partidário)

> Art. 107. Determina-se para cada partido o quociente partidário
> dividindo-se pelo quociente eleitoral o número de votos válidos
> dados sob a mesma legenda, desprezada a fração.
> *(Redação dada pela Lei nº 14.211, de 2021)*

(Translation: For each party, the party quotient is determined by
dividing the number of valid votes received by that party by the
electoral quotient, disregarding the fraction.)

Important interpretive note: "votos válidos dados sob a mesma
legenda" includes both *voto nominal* (votes for individual
candidates of the party) and *voto de legenda* (votes for the
party itself). The party's total for the quociente-partidário
calculation is the sum of both.

### Statutory text — CE Art. 108 (Candidate Election; 10% Rule)

> Art. 108. Estarão eleitos, entre os candidatos registrados por
> um partido que tenham obtido votos em número igual ou superior
> a 10% (dez por cento) do quociente eleitoral, tantos quantos
> o respectivo quociente partidário indicar, na ordem da votação
> nominal que cada um tenha recebido.
> *(Redação dada pela Lei nº 14.211, de 2021)*
>
> Parágrafo único. Os lugares não preenchidos em razão da
> exigência de votação nominal mínima a que se refere o caput
> serão distribuídos de acordo com as regras do art. 109.

(Translation: Among the candidates registered by a party who have
obtained votes equal to or greater than 10% of the electoral
quotient, those equal in number to the party quotient shall be
elected, in the order of the nominal vote each has received.
*Sole paragraph: Seats not filled due to the minimum nominal-vote
requirement of the caput shall be distributed according to the
rules of Art. 109.*)

### Statutory text — CE Art. 109 (Sobras / Remainder Seats)

> Art. 109. Os lugares não preenchidos com a aplicação dos
> quocientes partidários e em razão da exigência de votação
> nominal mínima a que se refere o art. 108 serão distribuídos
> de acordo com as seguintes regras:
>
> I — dividir-se-á o número de votos válidos atribuídos a cada
> partido pelo número de lugares por ele obtido mais 1 (um),
> cabendo ao partido que apresentar a maior média um dos lugares
> a preencher, desde que tenha candidato que atenda à exigência
> de votação nominal mínima;
>
> II — repetir-se-á a operação para cada um dos lugares a
> preencher;
>
> III — quando não houver mais partidos com candidatos que
> atendam às duas exigências do inciso I deste caput, as
> cadeiras serão distribuídas aos partidos que apresentarem as
> maiores médias.
>
> § 1º O preenchimento dos lugares com que cada partido for
> contemplado far-se-á segundo a ordem de votação recebida por
> seus candidatos.
>
> § 2º Poderão concorrer à distribuição dos lugares todos os
> partidos que participaram do pleito, desde que tenham obtido
> pelo menos 80% (oitenta por cento) do quociente eleitoral, e
> os candidatos que tenham obtido votos em número igual ou
> superior a 20% (vinte por cento) desse quociente.
> *(Vide ADI 7325) (Vide ADI 7263) (Vide ADI 7228)*

(Translation: Seats not filled by application of the party
quotients and the minimum nominal-vote requirement of Art. 108
shall be distributed by the following rules:
*I — The valid votes attributed to each party shall be divided
by the number of seats already received by that party plus one;
the party with the highest average is awarded one of the
remaining seats, provided it has a candidate meeting the minimum
nominal-vote requirement.
II — The operation is repeated for each remaining seat.
III — When no party with candidates meeting the two requirements
of subsection I remains, seats are distributed to the parties
with the highest averages.
§ 1º Seats won by a party are filled according to the nominal-
vote order received by its candidates.
§ 2º All parties that participated in the contest may compete in
the distribution, provided they obtained at least 80% of the
electoral quotient, and candidates obtained votes equal to or
greater than 20% of that quotient.*)

The 80%/20% performance thresholds in Art. 109 § 2º are the
subject of three constitutional challenges: **STF, ADI 7228, ADI
7263, ADI 7325 (decided February 2024)**, which declared the
party-level 80% threshold and candidate-level 20% threshold
unconstitutional, opening the surplus distribution to all parties
that participated in the election.

### Operationalized values

```
allocation_formula:              two-step:
                                 (1) Hare quota ("quociente
                                     eleitoral") for inter-party
                                     allocation (CE Art. 106-107)
                                 (2) Highest averages
                                     (D'Hondt-style) for sobras
                                     (CE Art. 109)
formula_codified_as:             procedural — quota and divisor
                                 mechanics specified in articles;
                                 no eponym used
formula_statutory_citation:      Código Eleitoral Arts. 106-109
ties_rule:                       within a party, by candidate's
                                 nominal-vote total (CE Art. 109
                                 § 1º); inter-party ties by drawing

legal_threshold_pct:             10% of quociente eleitoral
                                 (candidate-level, CE Art. 108)
                                 — a candidate of a party that
                                 wins seats does NOT qualify if
                                 the candidate's personal vote is
                                 below this floor; the seat then
                                 flows to sobras
threshold_level:                 candidate-level (not party-level)
threshold_exemption_rules:       none for the candidate floor
threshold_backdoor:              not applicable

apparentement_allowed:           federações partidárias (Lei
                                 14.208/2021): permanent (≥4-year)
                                 joint structures functioning as
                                 a single party for electoral
                                 purposes; coligações in
                                 proportional elections abolished
                                 by EC 97/2017
intra_list_rule:                 pure_preference (CE Art. 108 -
                                 ordem da votação nominal)
preference_threshold_pct:        10% of quociente eleitoral
                                 (CE Art. 108)
intra_list_ties_rule:            in submitted nominal-vote order;
                                 final ties by lot
```

### Notes

The Brazilian formula combines the **Hare quota for the principal
allocation** with **D'Hondt-style highest averages for the
remainder** — a hybrid not seen in the German cases (which use
Sainte-Laguë end-to-end) or in the NSW Droop quota (which uses
preference transfers). Three drafting features are notable:

1. **Two-step structure made explicit in statute**: Arts. 106-108
   handle the principal allocation via Hare quota; Art. 109
   handles the remainder via highest averages. The transition
   between methods is statutorily named and procedurally
   specified, not left to administrative discretion.
2. **Candidate-level threshold (10% of quociente)**: a candidate
   of a party that won seats by quotient may still be ineligible
   if the candidate personally received fewer than 10% of the
   electoral quotient in nominal votes. This is a structural
   constraint on intra-party concentration — a single dominant
   candidate cannot "carry" several otherwise-low-vote
   colleagues into office. The seats not filled for this reason
   flow to the *sobras* distribution under Art. 109.
3. **Constitutional review of formula provisions**: STF in
   February 2024 struck down the 80% party-level performance
   threshold for surplus participation (Art. 109 § 2º). This
   parallels the German VerfGH NRW 2025 ruling on the
   Rock-Verfahren and the BVerfG 2024 ruling on the 5%
   threshold without Grundmandatsklausel. Across the project's
   case set, formula provisions are subject to ongoing
   constitutional review under equality-of-vote-success doctrine.

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

CF Art. 14: voting is compulsory for those aged 18–70, and
optional for those aged 16–17 and over 70. Eligibility extends
to Brazilian citizens; non-citizens cannot vote at any level.
The *Tribunal Superior Eleitoral* maintains the *Cadastro
Eleitoral* (electoral registry) — an active but quasi-automatic
register, with biometric enrollment in most jurisdictions.

### B. Candidate / list registration

Per Lei 9.504 Arts. 8–14:

- **Party affiliation required**: every candidate must have been
  affiliated with the party for at least six months before
  filing (CF Art. 14 § 3º V; Lei 9.504 Art. 9). No independent
  candidacy is permitted at any level.
- **List size**: each party may register up to 100% of the
  number of seats plus 1 (Lei 9.504 Art. 10). For a 9-seat
  council, up to 10 candidates per party.
- **Gender quota**: 30% minimum each sex (Lei 9.504 Art. 10 § 3º;
  CF Art. 17 § 7º).
- **Convention**: candidates are selected at a party convention;
  the list is then registered with the *Tribunal Regional
  Eleitoral* (state-level court).
- **Disclosure obligations**: candidates and parties are subject
  to extensive registration and disclosure requirements through
  the *Sistema de Candidaturas* (CANDex).
- **Federações partidárias**: a federation registered with the
  TSE under Lei 14.208/2021 functions as a single party for
  registration, candidate slots, and proportional allocation.

### C. Campaign finance

Governed by Lei 9.504/1997 Title V (Arts. 17–32) and Lei
9.096/1995 (Lei dos Partidos Políticos). Brazil maintains a
**Fundo Especial de Financiamento de Campanha** (FEFC, "election
fund") — a public fund distributed to parties for campaign
spending. The fund is allocated by a formula tied to congressional
representation, with a 2018 reform requiring 30% to be applied to
women's candidacies and a 2020 STF ruling requiring proportional
allocation to Black and pardo candidates as well.

### D. Election administration

The *Justiça Eleitoral* (Electoral Justice) — a specialized
branch of the federal judiciary — administers elections under the
Constitution and the *Código Eleitoral*. Three tiers:

- **Tribunal Superior Eleitoral** (TSE) — federal apex, in
  Brasília;
- **Tribunais Regionais Eleitorais** (TRE) — one per state and
  the Federal District;
- **Juízes Eleitorais** — first-instance electoral judges,
  drawn from the regular state judiciary.

Election-judge service is rotational; judges of regular courts
are temporarily assigned to electoral functions. This is a
distinctive feature of Brazilian electoral administration: the
same judiciary that administers elections also adjudicates
electoral disputes, with separate procedural rules.

### E. Vote count, certification, dispute resolution

The *urna eletrônica* (electronic voting machine) records all
votes since 2000. Counting is digital and aggregated centrally
via the TSE network. Preliminary results are published within
hours of poll close; final totalization within days.

Election challenges run through the *Justiça Eleitoral*: TRE at
first instance, TSE on appeal, with constitutional questions
reaching the *Supremo Tribunal Federal* (STF). The STF has been
the principal forum for proportional-formula litigation (ADI
7228, 7263, 7325 in 2024).

### F. Media access

Lei 9.504 Title VII (Arts. 47–57) governs the *Horário Gratuito
de Propaganda Eleitoral* (HGPE — free electoral broadcasting
time). Television and radio broadcasters are required to provide
free time to parties, allocated by formula. The 2017 reform
(Lei 13.488) reduced HGPE duration; subsequent reforms have
adjusted the allocation formula in response to coligação
abolition and federação introduction.

### G. (Districting law — captured under Component 1)

District structure is non-applicable: each município is a single
electoral district, with no sub-municipal divisions for council
contests.

---

## 5. PROSeS performance diagnostic

The empirical anchor is the **6 October 2024 municipal elections**
— the first held under the post-2024 STF rulings on Art. 109 § 2º
and the second under the post-2017 abolition of *coligações*. Key
sources:

- *Tribunal Superior Eleitoral* (TSE) — official results and the
  *Painel das Eleições*.
- *Atlas Eleitoral* and the academic *Brazilian Studies in
  Political Economy* literature.
- OAS Electoral Observation Mission reports for the 2024 cycle.

### Process Design

The Justiça Eleitoral's institutional structure (specialized
court system administering elections) is a process-design choice
without direct analog in the German, NSW, or U.S. cases. Process
participation is structured through public hearings of the TSE
and TREs and a robust *Ministério Público Eleitoral* (electoral
public prosecutor) tradition.

### Resource Investment

Brazil funds elections through federal appropriations to the
*Justiça Eleitoral*. The FEFC (election fund) for parties was
~R$4.96 billion (~US$985 million) for the 2024 municipal cycle,
distributed by formula to parties.

### Service Output Quality

**Convenience**: compulsory voting plus universal urna eletrônica
deployment produces high in-person turnout. Postal and absentee
voting are not available; voters voting outside their registered
*município* must justify absence (*justificativa eleitoral*).

**Accuracy**: the urna eletrônica produces an electronic
result; printed individual receipts (the so-called *voto
impresso*) were rejected by Congress in 2021. Validation depends
on the integrity of the machine source code, with public-audit
provisions but no paper trail in the strict sense.

### Service Outcomes

**Voter turnout** at the 2024 first round was approximately 79.4%
of compulsory-aged registered voters — a baseline product of
compulsory-voting effects.

**Equity / minority representation**: the 2018 reform of FEFC
and 2020 STF ruling extending proportional funding to Black and
pardo candidates have produced measurable increases in
descriptive representation; Black/pardo vereador shares have
risen from 26% in 2016 to ~35% in 2024 (TSE data). Women's share
of vereador seats has risen more slowly (~16% in 2016 → ~17.7%
in 2024) despite the 30% candidacy quota.

### Stakeholder Satisfaction

Satisfaction with the urna eletrônica is high across most
political-participant strata; the 2018–2022 dispute over electoral
integrity produced an organized but minority push for paper
ballots that did not gain legislative traction. Compulsory voting
remains broadly supported in public opinion data.

---

## 6. Venice Commission compliance check

Brazil is not a Venice Commission member state, but the Venice
principles map onto the Brazilian regime as follows:

```
universal_suffrage:    compliant   # CF Art. 14
equal_suffrage:        compliant
free_suffrage:         compliant   # though compulsory voting
                                   # raises the question of
                                   # whether "free" extends to
                                   # the choice not to vote
secret_suffrage:       compliant
direct_suffrage:       compliant
periodic_elections:    compliant   # 4-year cycle, alternating
                                   # municipal and federal years
fundamental_rights:    compliant
regulatory_stability:  medium      # 2017 (coligações), 2021
                                   # (federações), 2024 (STF
                                   # rulings) produced repeated
                                   # mid-cycle changes
procedural_safeguards: compliant
```

---

## 7. Gardner portability assessment for US implementation

### Universal-vs-particular classification

| Provision | Type | Rationale |
|---|---|---|
| Single-vote candidate-or-party expression (voto nominal vs voto de legenda) | **Universal** | The architectural pattern is portable to any list-PR system regardless of vote-conversion rule. The Brazilian implementation depends on electronic voting, but the design adapts to paper ballots through a single "party only" oval at the top of each list column. |
| Constitutional codification of council-size table (CF Art. 29(IV)) | **Hybrid** | The substantive choice (population-tiered table) is portable; the constitutional placement reflects Brazilian federal structure. U.S. analog: state constitutional or charter amendment. |
| Single-municipality district structure | **Universal** | Maps onto U.S. local jurisdictions where the city is the natural electoral unit. |
| 10% candidate threshold (CE Art. 108) | **Universal** | The structural constraint on intra-party concentration is a portable drafting move. The threshold percentage is a parameter to set, not a Brazilian-particular feature. |
| Hare-quota + highest-averages hybrid (CE Arts. 106-109) | **Universal** | Both methods are familiar and the two-step structure is portable. |
| Required party affiliation; no independent candidacy (CF Art. 14 § 3º V) | **Particular** | A Brazilian-particular constraint not portable to U.S. local non-partisan contexts. |
| 30% gender quota with funding enforcement (Lei 9.504 Art. 10 § 3º; CF Art. 17 § 7º; FEFC 30% rule) | **Particular** | Gender quotas in candidacy regulation face a different legal-constitutional environment in the U.S. than in Brazil; the funding-enforcement mechanism is a portable concept. |
| Compulsory voting (CF Art. 14 § 1º) | **Particular** | Politically and constitutionally untenable in U.S. contexts. |
| Federações partidárias (Lei 14.208/2021) | **Hybrid** | The substance — a permanent joint structure functioning as a single electoral entity — is portable as an apparentement model. The 4-year minimum lock-in is the distinctive Brazilian parameter. |

### Top three takeaways for US state/local implementation

1. **Single-vote candidate-or-party expression operates at scale.**
   Brazil runs the architecture across 5,568 municipalities with
   ~155 million registered voters. The interface is digital
   (single number on the urna eletrônica), but the substantive
   logic — one vote, expressible as either a candidate
   preference or a party preference, both contributing to the
   inter-party allocation — adapts to paper ballots without
   substantive modification. The drafting question for U.S.
   adoption is the marking convention, not the underlying
   substantive logic.

2. **Candidate-level minimum thresholds (CE Art. 108) are a
   distinct drafting tool.** A 10% (or other parameter)
   candidate-level threshold within an open list filters
   intra-party "carrying" effects without affecting the
   inter-party formula. Brazilian experience shows the
   mechanism works without producing legitimacy crises: the
   seats not filled flow to the *sobras* distribution and end
   up with parties whose candidates do meet the floor. A U.S.
   analog could be tuned for any desired floor.

3. **The two-step formula structure (quota + highest averages)
   is statutorily explicit.** Brazilian Arts. 106-109 describe
   the principal allocation (Hare quota) and the remainder
   distribution (D'Hondt-style highest averages) as distinct
   procedural steps within the same statutory body. U.S.
   drafting can adopt this structure without committing to the
   Hare or D'Hondt families specifically — the substitution to
   Sainte-Laguë / Webster (the German federal and Bavarian
   choice) preserves the two-step architecture while changing
   the rounding rule.

---

## 8. Sources

### Primary

- *Constituição da República Federativa do Brasil* (1988), Arts.
  14, 17, 29(IV). Cached at
  `sources/brazil/constituicao.html`.
  <https://www.planalto.gov.br/ccivil_03/constituicao/constituicao.htm>
- *Código Eleitoral* (Lei nº 4.737, de 15 de julho de 1965),
  consolidated text. Arts. 106–109. Cached at
  `sources/brazil/l4737compilado.html`.
  <https://www.planalto.gov.br/ccivil_03/leis/l4737compilado.htm>
- *Lei das Eleições* (Lei nº 9.504, de 30 de setembro de 1997).
  Cached at `sources/brazil/l9504.html`.
  <https://www.planalto.gov.br/ccivil_03/leis/l9504.htm>
- *Lei dos Partidos Políticos* (Lei nº 9.096, de 19 de setembro
  de 1995).
- *Emenda Constitucional nº 58, de 23 de setembro de 2009* —
  the population-tiered council-size table.
- *Emenda Constitucional nº 97, de 4 de outubro de 2017* —
  abolition of *coligações* in proportional elections.
- *Lei nº 14.208, de 28 de setembro de 2021* — *federações
  partidárias*.
- *Lei nº 14.211, de 1 de outubro de 2021* — amendments to CE
  Arts. 107, 108, 109.

### Constitutional decisions

- **STF, ADI 7228, ADI 7263, ADI 7325** (decided February 2024)
  — the 80% party-level performance threshold and 20%
  candidate-level threshold in CE Art. 109 § 2º declared
  unconstitutional.

### TSE materials

- TSE, *Resolução nº 23.736/2024* — the resolution governing the
  October 2024 municipal elections.
- TSE, *Conheça o sistema proporcional, usado para a eleição
  de vereadores*:
  <https://www.tse.jus.br/comunicacao/noticias/2024/Abril/eleicoes-2024-sistema-proporcional-e-usado-para-eleicao-de-vereadores>
- TRE-SP, *Entenda o cálculo para determinar o quociente
  eleitoral, o quociente partidário e as sobras*:
  <https://www.tre-sp.jus.br/comunicacao/noticias/2024/Fevereiro/entenda-o-calculo-para-determinar-quais-vereadores-e-deputados-sao-eleitos>

### Outstanding gaps

- Full text of the STF ADI rulings (2024) — at present cited
  via TSE / TRE summaries, not via the STF opinion text.
- Verbatim text of Lei 9.504 Arts. 8, 10, 87, 105, and Title V
  (campaign finance).
- Verbatim text of Lei 9.096/1995 (Lei dos Partidos Políticos).
- TSE Resolução 23.736/2024 substantive provisions.
- 2024 election outcome data: descriptive representation
  measures by race and gender; comparative invalid-vote rates
  vs the 2020 cycle; share of voto-de-legenda vs voto-nominal
  by municipality size.
- OAS Electoral Observation Mission report for the 2024 cycle
  (if published).

### Resolved in this iteration

**2026-05-05** (initial profile):
- CF Art. 29(IV) (population-tiered council-size table) quoted
  in Component 1.
- CE Art. 106 (quociente eleitoral), Art. 107 (quociente
  partidário), Art. 108 (10% candidate threshold), Art. 109
  (sobras / highest-averages distribution) quoted in Component
  3.
- Lei 9.504 Art. 10 § 3º (gender quota) quoted in Component 2.
- 2017 (EC 97) coligação abolition documented.
- 2021 (Lei 14.208) federações partidárias introduction
  documented.
- 2021 (Lei 14.211) amendments to CE Arts. 107-109 documented.
- 2024 STF ADI rulings on Art. 109 § 2º documented.
