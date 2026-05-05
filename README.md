# electlaw

A practitioner-oriented analytical document and user's guide for US
lawyers and administrators on the **statutory and administrative
implementation of proportional representation** at the state and
local level.

This project is conceived as a much larger and more detailed
follow-up to the Charles Hamilton Houston Institute / Guinier
Project primer
**[*Getting from Votes to Seats*](sources/pdfs/Guinier_Project_Getting_from_Votes_to_Seats.pdf)**,
which establishes the conceptual foundation. Where the primer
answers *what* the components of an electoral system are, this
project answers *how* to codify and administer them in the US.

## The three primary components (the spine)

From the primer (pp. 2–16):

1. **Seat Product** = Assembly Size × District Magnitude.
   Threshold of Exclusion = 1/(M+1).
2. **Ballot Structure** — how voters express preferences;
   coordination problems Level A (candidate-side) and Level B
   (voter-side); spectrum from candidate-centered to coalition-
   centered.
3. **Allocation Formula** — Hamilton/Hare, Droop,
   Jefferson/D'Hondt, Webster/Sainte-Laguë.

Connected statutory areas (voter eligibility, list / candidate
registration, campaign finance, election administration,
certification, dispute resolution, media access) are treated at
the depth needed to show how they affect the three components.

## Scope

- **System types**: List PR and MMP. STV is out of scope as a
  vote-conversion rule, but STV jurisdictions with list-like
  administrative scaffolding (Scotland, NSW Australia above-the-
  line) are included for the lessons they offer on administering
  grouped candidacies.
- **Levels of government**: All of them. The guide addresses how
  US lawyers and administrators write and enforce PR statutes at
  the **federal, state, and local** levels, in both **partisan and
  non-partisan** contexts. Non-partisan local elections are an
  important *subsection* because most US local charters run
  formally non-partisan elections, but they are not the project's
  center.
- **Cross-cutting drafting problems** the guide addresses:
  constitutional and preemption constraints; statutory clarity
  (especially for unfamiliar formulas); ballot uniformity; ballot
  access for non-party lists; administrative implementation by
  EMBs; certification and dispute resolution.

## Comparative cases (13)

Germany · United Kingdom · Spain · Netherlands · Belgium · Finland
· Denmark · Brazil · Chile · South Africa · New Zealand · Scotland
· Australia

## Diagnostic and reference tools

- **PROSeS** (James 2020) — performance evaluation lens.
- **PEI 11-stage electoral cycle** (Norris et al.) — connected-area
  checklist.
- **Venice Commission Code of Good Practice** (2002) — normative
  floor.
- **Gardner (ed.), *Comparative Election Law*** — portability test.

## Repository layout

```
framework/
  synthesis.md              master framework; read first
  components/               one document per primary component
    01_seat_product.md
    02_ballot_structure.md
    03_allocation.md
  connected_areas.md        supporting statutory areas
  performance.md            PROSeS diagnostic
  electoral_cycle.md        PEI cycle cross-reference
  case_template.md          fill-in template per case
  README.md                 reading order
cases/                      one folder per country (13 cases)
comparisons/                cross-case write-ups
models/                     draft model US statutes (later phase)
sources/                    statutes, secondary materials, source
                            ledger, local PDF cache
```

## Status

Project started 2026-05-04. Framework v2 (organized around the
primer's three components) finalized 2026-05-04. Currently building
case-study scaffolding. Comparative case studies populate next; US
target jurisdictions and model statutory drafts are downstream of
the comparative phase.
