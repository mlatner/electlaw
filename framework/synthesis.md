# Synthesis: framework for the implementation guide

## Mission

This project produces an analytical document and user's guide for
**US lawyers and administrators** on the *statutory and
administrative implementation* of proportional representation at
**all levels of US government — federal, state, and local — and
in both partisan and non-partisan contexts**.

It is conceived as a much larger and more detailed follow-up to the
Charles Hamilton Houston Institute / Guinier Project primer
**[Getting from Votes to Seats](../sources/pdfs/Guinier_Project_Getting_from_Votes_to_Seats.pdf)**,
which establishes the conceptual foundation. Where the primer
answers *what* the components of an electoral system are, this
project answers *how* to codify and administer them in the US legal
context.

The deliverable is a practitioner-oriented reference — not an
academic monograph, not a research index, not a comparative legal
treatise. Non-partisan local elections appear as one important
subsection of the guide because that is where the most active US
reform is happening and where comparative lessons on
list-without-parties administration most directly apply, but the
guide's full scope spans every level and partisan posture.

## The three primary components — the spine

From the primer (pp. 2–16), the spine of the project. Each gets a
deep framework document and will eventually become a full chapter (or
chapter cluster) of the guide:

1. **`components/01_seat_product.md`** — Assembly Size × District
   Magnitude. Threshold of Exclusion = 1 / (M + 1).
2. **`components/02_ballot_structure.md`** — How voters express
   preferences; coordination problems Level A (candidate-side) and
   Level B (voter-side); spectrum from candidate-centered to
   coalition-centered.
3. **`components/03_allocation.md`** — Formulas converting votes to
   seats. American + European naming: Hamilton/Hare, Droop,
   Jefferson/D'Hondt, Webster/Sainte-Laguë, etc.

These three are **the mechanics of PR**. The deliverable's primary
substance is organized around them, in the primer's order.

## Connected areas

`connected_areas.md` covers the surrounding statutory and
administrative environment that affects the mechanics:

- A. Voter eligibility and registration
- B. **Candidate / party / list registration** (the most important
  for US local applicability — non-partisan list administration is
  the central drafting problem)
- C. Campaign finance and disclosure
- D. Election administration and EMB structure
- E. Vote counting, certification, recounts
- F. Election dispute resolution
- G. Media access
- H. Districting law

Each is treated only at the depth required to explain how it bears
on the three primary components.

## Diagnostic and reference tools

These are not the spine of the project — they are tools applied to
each provision under study and to the eventual model statute.

- **`performance.md`** — James (2020) PROSeS framework adapted as a
  diagnostic for any provision: process design, resource investment,
  service output quality, service outcomes, stakeholder satisfaction.
- **`electoral_cycle.md`** — Norris / Electoral Integrity Project's
  eleven-stage electoral cycle. Used as a checklist for which
  connected-area provisions exist in a given case.
- **Venice Commission Code of Good Practice** (2002) — used as a
  *normative floor*: any provision we draft or recommend must pass
  the Venice principles (universal, equal, free, secret, direct
  suffrage; periodicity; respect for fundamental rights;
  regulatory stability; procedural safeguards).
- **Gardner (ed.), *Comparative Election Law*** (Edward Elgar 2022)
  — used as the *portability test*: each foreign provision is
  classified universal vs. particular, which disciplines what we
  recommend for US adoption.

## Comparative cases as empirical bedrock

Thirteen cases (`cases/`) provide the comparative evidence. Each is
documented using the case template (`case_template.md`), organized
around the three primary components.

Cases are selected to maximize coverage of the design space:

- **Germany (Bavaria especially)** — rich non-partisan list ecosystem;
  open list with cumulation/panachage.
- **Netherlands** — *lokale partijen* as a working non-party list
  system; preference votes; abolished apparentement.
- **Spain** — *agrupación de electores* under LOREG.
- **Finland** — pure open list; *valitsijayhdistys* voter
  associations.
- **Denmark** — list-cartel mechanics (*listeforbund* / *valgforbund*);
  flexible list / parallel-ordered list choice.
- **Belgium** — three regional regimes; flexible list; Imperiali
  formula at municipal level.
- **Brazil** — party-list system with strongly candidate-centered
  intra-list dynamics (personal-vote totals govern seat assignment
  within each list); recent abolition of *coligações* for
  proportional contests; *federações partidárias* as a partial
  replacement.
- **Chile** — post-2015 reform; independent-list mechanics;
  Constitutional Convention experience.
- **South Africa** — local mixed (ward + PR); independents on PR
  list since 2023.
- **New Zealand** — canonical MMP at the national level since 1996;
  Sainte-Laguë leveling; 5%-or-one-electorate threshold; reserved
  Māori seats. Strongest comparator for any US state-legislature-
  level MMP design.
- **Scotland** — STV at local level. Included for the
  *administrative scaffolding* lessons (candidate descriptions in
  lieu of party labels), even though STV-as-vote-conversion is out
  of scope.
- **Australia** (NSW local + Senate) — above-the-line group voting
  as a list-shaped administrative interface.
- **United Kingdom** (London Assembly only) — mostly a negative
  case; minimal list-PR exposure.

## How a case is documented

For each country case, the analyst:

1. Fills in case metadata.
2. Walks **Component 1** (Seat Product), capturing statutory
   provisions on assembly size, district magnitude, tiered
   structure, and threshold of exclusion.
3. Walks **Component 2** (Ballot Structure), capturing ballot type,
   list-bearing entities, non-partisan list labeling, ballot
   design authority.
4. Walks **Component 3** (Allocation Formula), capturing the
   formula, threshold, apparentement rules, intra-list assignment.
5. Notes **connected areas** at supporting depth.
6. Applies the **PROSeS** lens.
7. Checks **Venice Commission** compliance.
8. Concludes with a **Gardner-style portability assessment** for US
   implementation.

## How comparisons are produced

Cross-case `comparisons/` documents aggregate along whichever axis
is analytically interesting. A given comparison cuts horizontally
across the twelve cases on a single dimension — e.g., "thresholds
across the project's twelve cases", "non-partisan list labeling
rules", "apparentement mechanics". These comparisons feed directly
into the eventual guide's component chapters.

## What this is not

- **Not a quantitative cross-national index.** Following James, we
  treat assessment as case-based and small-n.
- **Not a comparative legal treatise.** We are not surveying
  election law generally — only the mechanics of PR and what bears
  on them.
- **Not the primer.** The primer establishes the conceptual frame
  and the audience-facing language. This project is its
  implementation companion.
- **Not a model statute draft (yet).** The `models/` directory is
  reserved for that work, which begins after the comparative phase
  is substantially complete.
