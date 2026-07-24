# Ballot-Error Crosswalk — 12 Jurisdictions × Review Evidence

Maps each case profile in `cases/` to the row of the Latner systematic
review (`sources/literature/Consolidated_Systematic_Review_Voter_Error_Electoral_Design.docx`)
that empirically characterizes that ballot architecture's error
behavior. Use this as a quick reference when a case profile asks
"what does the empirical literature say about this ballot type."

Rate estimates below are drawn from **published literature only**;
none come from electlaw or list_methods modeling. Where a review-row
citation was revised after this crosswalk was first drafted (2026-07-22–23
fact-check pass in `~/error/docs/decisions_log.md`), the current row
reflects the revised citation and the change is documented in
`../docs/sources_log.md`.

**Design-space frame** (from `~/error/CLAUDE.md`, the companion blog
series): each case sits on two independent axes —
- **Axis 1 (Inclusive ↔ Exclusive)**: district magnitude / threshold
  of exclusion. This is component-1 territory (`01_seat_product.md`).
- **Axis 2 (Candidate-centered ↔ Party-centered)**: ballot structure.
  This is the axis component 2 (this document's parent) is about.

The rows below characterize Axis-2 position; Axis-1 position is noted
in each profile.

Columns:
- **Case (jurisdiction)** — directory under `cases/`.
- **Ballot architecture** — short structural description (primer
  Level-A / Level-B framing where applicable).
- **Review row** — corresponding row in Table 1 of the review's
  *Electoral System Comparison Matrix*.
- **Observed invalid / mismark rate** — empirical estimate(s) from
  the literature most directly applicable to this architecture.
- **Key citation(s)** — the studies the review uses for this row.
- **Minority-representation note** — review evidence on
  disparate-impact patterns for this architecture.

---

| Case (jurisdiction) | Ballot architecture | Review row | Observed rate | Key citation(s) | Minority-rep. note |
|---|---|---|---|---|---|
| **Germany — Federal Bundestag** (`cases/germany/federal_profile.md`) | Two-vote MMP: constituency vote + closed-list compensatory (Erststimme / Zweitstimme) | Closed-list party vote + FPTP | <1–2% invalid on list vote; ~1.5–2% on constituency vote | Kouba & Lysek 2019; Fatke & Heinsohn 2017 | Low-error reference baseline; PR boost + low complexity → strong descriptive representation via list ordering |
| **Germany — Bavaria** (`cases/germany/bavaria_profile.md`) | Multi-vote MMP with cumulation: voter has as many votes as seats, may cumulate or distribute (*Listenkreuz* vs candidate votes per GLKrWG Art. 34) | Multi-vote (D21+) (flexible maximum) | ~1.5% invalid (exp.) | Jarabinský et al. 2025; Haase Formánková et al. 2026 | Flexible-maximum: fewer than max marks remains valid — minimizes disparate disqualification |
| **Germany — NRW** (`cases/germany/nrw_profile.md`) | One-vote MMP (KWahlG § 25, § 31) — single mark covering both tiers | Closed-list party vote (with mixed allocation) | <1–2% invalid expected | Inferred from closed-list row (Kouba & Lysek 2019) | One-vote design collapses the dual-vote coordination task voters face under standard MMP; expected reduction in the split-ticket confusion channel, though the direct empirical test of NRW-style single-vote MMP vs standard two-vote MMP has not been published. |
| **Australia — NSW local** (`cases/australia/nsw_local_profile.md`) | STV / optional preferential, with above-the-line group voting (NSW LG Act 1993 Ch 10 Pt 6 Div 1) | RCV/IRV (optional) — STV variant | ~4–5% improper; exhaustion variable | Pettigrew & Radley 2026 (overvotes / overranks / skips); Endersby & Towle 2014 (generic Irish STV context) | Above-the-line group voting *reduces* error sharply — voters who pick a group bypass the within-group ranking burden. Key precedent for the user's preferred design. |
| **Brazil — federal** (`cases/brazil/profile.md`) | Mandatory open-list PR with compulsory voting; electronic ballot since 1996 | Open-list PR (mandatory) + Compulsory voting | Up to 30%+ pre-electronic; ~12.9% "PR blow" estimate | Power & Roberts 1995 (pre-electronic rates); Flis & Kaminski 2025 (PR-blow magnitude). *Cheibub & Sin 2020 speaks to intra-party competition dynamics, not to invalid-vote rates — see Chile row.* | **The cautionary case.** Compulsory voting + complex ballots in earlier elections produced very high invalid rates, with the error gradient across education documented but not uniformly monotonic across studies (Kouba & Lysek 2019 meta: 11 hypothesized-direction tests, 4 opposite, 8 null across 23 total; overall meta effect r=0.42 p<0.05, significant negative). Electronic ballot has reduced but not eliminated. Parallel to Colombia: ballot redesign *within* an open-list system reduced invalid rates (Pachón et al. on the 2006/2010 redesigned ballot). Physical layout is an independent lever separate from allocation choice. |
| **Spain — federal** (`cases/spain/profile.md`) | Closed-list PR (D'Hondt at provincial level) | Closed-list party vote | <1–2% invalid | Kouba & Lysek 2019 | Lowest-error reference; descriptive rep depends entirely on internal party list ordering (Krook & O'Brien 2010 quota dynamics) |
| **Netherlands — federal** (`cases/netherlands/profile.md`) | Open-list PR with optional *voorkeurstem* (preference vote); 25%-of-quota threshold for reordering | Flexible-list PR | ~2–4% mismark (est.) | Flis & Kaminski 2025; Söderlund et al. 2021 | Optional preference vote = low error floor (party vote default) with high-expressiveness ceiling. **Best-practice ballot-error compromise the review identifies.** |
| **Belgium — federal** (`cases/belgium/federal_profile.md`) | Semi-open list (preference vote affects ordering only if threshold met); D'Hondt | Flexible-list PR | ~2–4% mismark (est.) | Flis & Kaminski 2025 | Similar to NL; preference vote is participation-side option, list defaults preserve closed-list error floor |
| **Belgium — Flanders local** (`cases/belgium/flanders_local_profile.md`) | Semi-open list at municipal level; preference vote with cumulation | Flexible-list PR | ~2–4% mismark (est.) | — (extrapolation from federal-Belgium row) | Local-level analog of federal Belgium; same ballot-error profile expected |
| **France — Paris-Lyon-Marseille** (`cases/france/profile.md`) | Closed-list PR with sectoral divisions; majoritarian top-up bonus | Closed-list party vote (with majority bonus) | <1–2% invalid expected | Kouba & Lysek 2019 (closed-list baseline) | Bonus seats are an allocation issue, not a ballot-structure issue; ballot-error remains closed-list-floor |
| **Chile — federal** (`cases/chile/profile.md`) | Open-list PR (D'Hondt) since 2015 reform | Open-list PR | ~3–5% mismark (est., extrapolated); 12.9% "PR blow" upper bound | Flis & Kaminski 2025 (invalid-rate); Power & Garand 2007 (Latin American residual votes); Cheibub & Sin 2020 (intra-party competition dynamics, not invalid-vote rates) | Chile's post-2015 open list invites the same intra-party-competition complexity that Cheibub & Sin (2020) document for Brazil — a candidate-cognitive-load channel that is analytically distinct from the invalid-vote channel. |
| **South Africa — national + provincial** (`cases/south-africa/profile.md`) | Closed-list PR at national level; mixed (constituency + closed-list compensatory) at provincial after 2023 reform | Closed-list party vote | <1–2% invalid | Kouba & Lysek 2019 | Low error; descriptive rep relies on party list construction. New mixed system at provincial level is structural-reform-watch item. |
| **New Zealand — federal** (`cases/new-zealand/profile.md`) | Two-vote MMP (canonical comparator) | Closed-list + FPTP | ~1–2% invalid each side | Norris 2004; Kouba & Lysek 2019 | Canonical MMP — low error, strong descriptive representation, demonstrated minority-list dynamics (Māori electoral roll) |
| **Scotland — Holyrood / local** (`cases/scotland/profile.md`) | MMP (parliament) + STV (local govt) | Two architectures: Closed-list MMP + STV (full rank) | MMP: ~1–2%; STV: 8.4% (exp.) | Carman, Mitchell & Johns 2008 ("unfortunate natural experiment"); Haase Formánková et al. 2026 | The 2007 Scottish parliament ballot redesign produced a major spike in invalid voting — a primary case study for ballot-layout testing. **Key precedent: physical ballot design is independent error source.** |
| **Denmark — federal** (`cases/denmark/profile.md`) | Personalized PR / flexible-list with strong personal-vote tradition | Flexible-list PR | ~2–4% mismark (est.) | Söderlund et al. 2021 | Long-running flex-list with very high preference-vote rates; the case where Level-B coordination is heavily voter-driven |

---

## How to use this crosswalk

When drafting any case profile that touches ballot-error empirical
claims, cite from this crosswalk's "Key citation(s)" column. When
the model-statute drafting addresses ballot complexity (`framework/components/02_ballot_structure.md`),
this table is the evidence base for choosing between architectures.

The user's working baseline (**one-vote MMP with party-or-candidate
options**, see `project_electlaw.md`) draws from:
- The closed-list / two-vote MMP baseline (Germany federal, NZ) for
  the party-vote pathway's low-error floor.
- NRW's one-vote architecture (KWahlG § 25, § 31).
- NSW above-the-line option for the visual interface.
- Netherlands' optional-preference threshold logic for any
  candidate-vote reordering effect.

The empirical case for that design is that it (a) preserves the
low-error closed-list floor for voters who use the party-vote
option, and (b) allows expressive candidate voting without
triggering the "PR blow" that pure mandatory open-list (Brazil,
pre-electronic; Poland) produces.

## Cross-reference: the diagnostic blog post

The parallel diagnostic treatment of the same evidence base is
`~/error/posts/2026-07-22-ballot-error-diagnostic/` (part of Latner's
*Election Administration and Electoral Bias* blog series). That post
went through a systematic fact-check pass on 2026-07-22–23 which
produced ten citation-level corrections that have been propagated
back into this crosswalk. See `../docs/sources_log.md` for the
correction ledger. Notable divergences from earlier drafts:

- The blog post organizes evidence by *findings* (distributional
  invariance, coordination-task drivers, invalidation-rule strictness,
  error-consequence rule), not by ballot type or by author. This
  crosswalk retains the by-jurisdiction organization because its
  purpose is different — mapping each case profile to its evidence —
  but any Axis-2 taxonomic prose in `02_ballot_structure.md` should
  match the blog's findings-keyed structure.
- The blog post retired the "cancels the PR boost" framing as too
  advocacy-adjacent; this crosswalk carries only the diagnostic
  finding ("PR blow" magnitude), not the trade-off framing.

## Gaps in the current evidence to flag in case profiles

The review identifies several gaps that case profiles should
acknowledge:

- **Limited direct data** on free-list / panachage error rates
  (Switzerland, some German Länder local).
- **Limited direct data** on partisan-vs-nonpartisan list error
  differences — particularly relevant to the project's interest
  in non-partisan local charters.
- **Online vs paper voting** findings (Haase Formánková et al.
  2026: 1.48× higher mismark odds online) need replication.
- **Conditional voting rules** (D21−, score voting with veto)
  produce high errors but are understudied in real elections.

These gaps mark places where the project's model statute should
choose conservatively (closed-list-like defaults) rather than rely
on architectures with thin evidence.
