# Component 3 — Allocation Formula

The third of the three primary components from the Guinier Project
primer (*Getting from Votes to Seats*, pp. 14–16). Allocation
formulas convert votes into seats. They are the final mathematical
step and, especially at low district magnitudes (Component 1), they
substantially shape who wins representation.

The primer organizes formulas into two families and names them with
both their **American constitutional designations** and their
**European designations**:

## Family 1: Largest Remainder methods

Compute a *quota* (the "cost" of a seat) and award seats by filling
whole quotas first, then distributing remaining seats by largest
leftover.

### Hamilton method (Hare quota)
- **Quota = Total Votes / Total Seats**
- After whole-quota allocations, remaining seats go to the largest
  remainders.
- **More favorable to minority coalitions** (primer p. 15): a group
  can win a seat on the strength of a remainder even without hitting
  a full quota.

### Droop quota (largest remainder)
- **Quota = Total Votes / (Total Seats + 1)**
- Smaller divisor produces a smaller quota, but the (s+1)
  qualification slightly advantages larger groups.
- **Less favorable to minorities** than Hamilton, but more so than
  divisor methods.

## Family 2: Highest Average (Divisor) methods

Divide each group's vote total by a sequence of divisors and award
seats to the highest resulting averages.

### Jefferson method (D'Hondt)
- **Divisor sequence = (seats won + 1)**, i.e., 1, 2, 3, 4 …
- Mathematically **favors larger groups**: each additional seat is
  "cheaper" to win after the first.
- The most common formula in continental Europe; familiar from
  Spain, Belgium municipal, Netherlands, Brazil, Chile, and
  others.

### Webster method (Sainte-Laguë)
- **Divisor sequence = (2 × seats won + 1)**, i.e., 1, 3, 5, 7 …
- Faster-shrinking divisor treats large and small groups more
  symmetrically.
- **Least biased** of the standard formulas; used in Norway,
  Denmark (with modified first divisor of 1.4), New Zealand
  party-list tier.

### Modified Sainte-Laguë
- Same as Webster but the first divisor is 1.4 (instead of 1),
  imposing a slight "first-seat tax" that filters very small
  parties at low magnitudes. Used by NO, SE, DE Bundestag.

### Imperiali (largest average)
- Divisor = (seats won + 2), i.e., 2, 3, 4, 5 …
- Strongly favors large parties. Used by **Belgian municipal
  elections** — relevant to the project. Has been criticized as
  disproportional and is used elsewhere primarily in deal-making
  contexts.

## Why formula matters most at low magnitude

The primer's p. 16 illustration: in a 3-seat district where a
majority bloc wins 80% and a minority 20%:

- **Jefferson awards all three seats to the majority.** Computed
  averages: 80, 40, 27 (for seats 1, 2, 3) vs. the minority's 20.
- **Webster awards the third seat to the minority.** Computed
  averages: 80, 27, 16 vs. the minority's 20.

The primer's gloss (p. 16):

> "Most formulas converge on proportionality at larger sizes (higher
> magnitude), but in 3–7 seat districts, different formulas … can
> have a profound impact on representation, determining whether a
> group wins no representation or has more representation than they
> would under an alternative formula."

The implication for US implementation: at the low magnitudes that
US local charters typically can accommodate (3–9 seats per district),
**formula choice is decisive**, and the choice should be a
substantive drafting decision, not a default.

## Statutory minimum thresholds

Separate from the threshold of exclusion (Component 1, structural)
and the formula-implied threshold, many systems impose a **legal
threshold** below which a list receives no seats:

- **Germany** (national): 5% threshold for *Bundestag*.
- **Many German municipalities**: no threshold beyond natural.
- **Spain** (Congress): 3%; varies for municipalities.
- **Netherlands** (national): no threshold (single 150-seat
  district produces natural threshold ≈ 0.67%).
- **South Africa local PR tier**: no threshold beyond 1/seat.
- **Belgium municipal**: no formal threshold.

Threshold design is a key US drafting question because it directly
controls how restrictive an otherwise permissive system can be.
Constitutional ballot-access law (*Williams v. Rhodes*, *Anderson v.
Celebrezze*) constrains how high a threshold can be set without
raising equal-protection concerns.

## Apparentement / list cartels

Some systems allow lists to declare **joint allocation pools** before
the count, so that small groups can pool votes for the formula step
and then divide the resulting seats internally. Forms include:

- *Listeforbund* / *valgforbund* (Denmark): three-tier nested
  cartels.
- *Yhteislista* and *vaaliliitto* (Finland): joint lists and
  electoral alliances.
- Pre-2017 *coligações* in Brazil municipal elections (now
  abolished for proportional contests).
- *Lijstverbinding* (Netherlands): formerly permitted, abolished.

Apparentement is a way for small groups to capture the benefits of a
larger denominator without merging organizationally. It is
useful for non-partisan lists that may share an
ideological direction but want separate ballot identities.

## Statutory questions for case studies

- Which formula is in force, and where codified (statute, charter,
  regulation)?
- How is the formula written: by name (e.g. "D'Hondt"), by
  mathematical formula, by procedural description, or by worked
  example in the statute?
- Are tied seats handled? How (random draw, age, vote totals at
  prior round)?
- Is a legal threshold imposed? At what level (district / regional
  / national)? With what exemptions (minority-protective
  carve-outs)?
- **Apparentement / list cartels**: are lists permitted to declare
  joint allocation pools? Under what rules?
- For tiered systems: which formula at which tier, and how are
  surplus / leveling seats allocated?

## Connections

- **Component 1 (Seat Product)**: at low M, formula choice is
  decisive; at high M, formulas converge on proportionality.
- **Component 2 (Ballot)**: open-list systems require an additional
  intra-list allocation mechanism (preference votes vs. list
  order). The inter-list formula (this component) and the intra-
  list rule (Component 2 / connected) are distinct.
- **Connected — vote count administration**: counting authority,
  recount rules, audit trails, certification timelines all bear
  here.

## US-specific considerations

### Statutory clarity

Existing US use of cumulative and limited vote relies on plurality-
style counting; formulas like D'Hondt and Sainte-Laguë are
unfamiliar in US ballot law. The implementation guide should
recommend that any US PR statute specify the allocation formula in
**plain language** with **a worked example embedded in the statute
itself**, to forestall litigation over interpretation and to give
EMBs a clear procedural map.

### Naming and constitutional grounding

Using "Hamilton / Jefferson / Webster" alongside Hare / D'Hondt /
Sainte-Laguë is more than cosmetic: these are the names already used
for House apportionment among states and so ground unfamiliar
formulas in American constitutional history. The primer adopts this
practice (pp. 15–16) and the implementation guide should follow.

### Threshold drafting

Federal and state constitutional law on ballot access constrains
how high a threshold can be set without raising equal-protection
concerns. Recommended drafting practice:

- Set the legal threshold at or below the natural threshold of
  exclusion at typical district magnitude, so that the legal
  threshold is non-binding in normal operation.
- If a higher threshold is imposed for systemic reasons (avoiding
  splinter representation), it should be defended on a record of
  legitimate state interest.

### Cumulative-vote and limited-vote precedents

Existing US case law on cumulative and limited voting relies on
plurality-style counting and does not directly involve quotas or
divisors. The implementation guide should note this gap: introducing
quota or divisor methods at the local level will require fresh
statutory language and may invite litigation, but does not
straightforwardly conflict with existing precedent.

## Cross-cutting research questions for the project

When all twelve cases are documented:

1. What is the comparative incidence of each formula at the local
   level, and what considerations drove the choice?
2. Where apparentement is permitted, what is the practical incidence
   and effect on small / non-partisan list outcomes?
3. How do statutes actually express the formula — by name, by math,
   by worked example — and what does that suggest for US drafting
   clarity?

---

**Reference**: primer pp. 14–16.
