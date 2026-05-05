# Case study template

Copy this file into a country folder as `profile.md` and fill in.
The template is organized around the three primary components from
the primer, with connected areas treated more briefly.

For each substantive section, capture (a) statutory citations,
(b) operationalized variable values, and (c) prose narrative.

Square-bracketed `[...]` fields are placeholders. `N/A` is acceptable
when a provision does not exist — but flag whether the absence is
*silent* (no rule) or *explicit* (rule says no). Both are findings.

---

## 0. Case metadata

```
country:
sub-jurisdiction:                # e.g. "Bavaria", "Wallonia", "NSW"
level_of_government:             # local | regional | national
electoral_system_family:         # list_PR | MMP | mixed_local | other
governing_statute_primary:
governing_statute_citation:
governing_statute_url:
governing_statute_year:
governing_statute_language:
constitutional_anchor:
last_major_reform_year:
analyst:
date_completed:
```

**Why this case is in the project** (2–4 sentences):

[free-text]

---

## 1. Component 1 — Seat Product (Assembly Size × District Magnitude)

### Assembly Size
```
total_seats:
codification_instrument:         # statute | charter | constitution
amendment_authority:
amendment_threshold:
last_change_year:
```

### District Magnitude
```
magnitude_uniform:               # yes | no
magnitude_typical:
magnitude_range:                 # min - max
districts_count:
districting_authority:
districting_frequency_years:
districting_criteria_in_statute:
```

### Tiered structure
```
tiered:                          # yes | no
tier_count:
tier_magnitudes:                 # list per tier
tier_compensatory:               # yes (leveling) | no (parallel)
```

### Threshold of exclusion (computed)
```
threshold_of_exclusion_pct:      # 1 / (M + 1)
```

**Notes** (VRA-equivalent context, historical changes, charter
politics, varying-magnitude rationale):

[free-text]

---

## 2. Component 2 — Ballot Structure

### Ballot type
```
ballot_type:                     # closed_list | open_list | flexible_list |
                                 #   limited_vote | cumulative | block_vote |
                                 #   stv | sntv | mmp_two_vote | mixed | other
preference_votes_per_voter:
panachage_allowed:               # yes | no
cumulation_allowed:              # yes | no
cumulation_max:
above_the_line_option:           # yes | no
```

### List-bearing entities (where applicable)
```
party_lists_allowed:             # yes | no
voter_grouping_lists_allowed:    # yes | no
voter_grouping_legal_term:       # native term
citizen_committee_lists_allowed: # yes | no
independents_on_lists_allowed:   # yes | no
```

### Non-partisan list labeling rules (where applicable)
```
non_party_label_allowed:         # yes | no
non_party_label_categories:      # geographic | professional | advocacy |
                                 #   ethnic | generic_letter | other
non_party_label_restrictions:
label_validation_authority:
```

### Ballot design authority and standards
```
ballot_design_authority:
overvote_rule:
undervote_rule:
write_in_treatment:
ballot_languages:
```

**Notes** (ballot complexity, simplicity considerations, voter-error
data if available):

[free-text]

---

## 3. Component 3 — Allocation Formula

### Inter-list allocation
```
allocation_formula:              # hamilton_hare | droop_lr |
                                 #   jefferson_dhondt | webster_sainte_lague |
                                 #   modified_sainte_lague | imperiali | other
formula_codified_as:             # named | mathematical | procedural | example
formula_statutory_citation:
ties_rule:
```

### Statutory threshold
```
legal_threshold_pct:
threshold_level:                 # district | regional | national
threshold_exemption_rules:
threshold_backdoor:              # e.g. NZ "one electorate seat"
```

### Apparentement / list cartels
```
apparentement_allowed:           # yes | no
apparentement_form:              # listeforbund | yhteislista | vaaliliitto |
                                 #   coligacao | other
apparentement_rules:
```

### Intra-list seat assignment (open / flexible lists)
```
intra_list_rule:                 # list_order | pure_preference |
                                 #   hybrid_threshold
preference_threshold_pct:
intra_list_ties_rule:
```

### Counting administration
```
counting_authority:
recount_trigger:
audit_requirements:
allocation_computation_authority:
```

**Notes** (worked example showing how an actual contest's seats were
allocated, where data is accessible):

[free-text]

---

## 4. Connected areas (brief)

### A. Voter eligibility and registration

[brief narrative + key citations]

### B. Candidate / list registration — *full subsection*

This is the most important connected area for the project.

```
list_registration_authority:
signatures_required_min:
signature_scaling:
signature_geographic_distribution:
deposit_amount:
deposit_currency:
deposit_refund_threshold:
filing_deadline_days_before:
party_v_nonparty_equal_treatment:    # yes | partial | no
list_size_min:
list_size_max:
list_ordering_rule:                  # submitter | alphabetical | random
gender_quota:                        # none | parity | zipper | percentage
gender_quota_pct:
residency_required:
multiple_candidacy_restrictions:
```

[free-text]

### C. Campaign finance

[brief]

### D. Election administration / EMB

[brief]

### E. Vote count, certification, recounts, dispute resolution

[brief]

### F. Media access

[brief]

### G. (Districting law — already captured under Component 1)

---

## 5. PROSeS performance diagnostic

For each cluster, note where evidence exists and where silence is
itself a finding (cite Elections-Commission-equivalent data,
academic studies, EIP / PEI scores).

- **Process Design** (public participation, probity, accountability):
  [...]
- **Resource Investment** (transparency, sustainability, legitimacy,
  contingency): [...]
- **Service Output Quality** (convenience, accuracy, enforcement,
  efficiency): [...]
- **Service Outcomes** (turnout, register accuracy/completeness,
  fraud, rejected ballots, service denial, violence; equity by
  group; diffuse impact): [...]
- **Stakeholder Satisfaction** (citizen, staff, parties / civil
  society): [...]

---

## 6. Venice Commission compliance check

```
universal_suffrage:              # compliant | partial | divergent
equal_suffrage:
free_suffrage:
secret_suffrage:
direct_suffrage:
periodic_elections:
fundamental_rights:
regulatory_stability:
procedural_safeguards:
```

**Notes on any divergence**:

[free-text]

---

## 7. Gardner portability assessment for US implementation

For each notable provision, classify the design problem it solves:

- **Universal**: portable; every democracy faces this problem.
- **Particular**: not directly portable; rooted in this country's
  constitutional / political history.
- **Hybrid**: substantively universal, procedurally embedded.

```
provision_1: [ name | universal/particular/hybrid | rationale ]
provision_2: ...
```

### Top three takeaways for US state/local implementation

1. [...]
2. [...]
3. [...]

---

## 8. Sources

[Primary statutes (with citations), case law, secondary sources.
Cross-reference local PDFs in `sources/<country>/`.]
