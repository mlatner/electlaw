# electlaw — Claude instructions

Model PR legislation drawn from comparative non-partisan list administration
in 12 countries.

## Documentation discipline (mandatory)

Two append-only logs in `docs/`:

- **`docs/sources_log.md`** — statutory sources, code citations, comparative
  jurisdiction references
- **`docs/decisions_log.md`** — drafting choices, comparative trade-offs

Read both at session start. Append at session end.

## Project-specific notes

- **Use actual code text and precise citations.** Never popular accounts of
  what a statute says. (memory: `feedback_statutory_primary_sources.md`)
- **Diagnostic language only.** No emotive terms. (memory:
  `feedback_diagnostic_language.md`)
- **Voter-error review** is the evidence base for RQ#2 — already integrated
  at `sources/literature/`. (memory: `reference_voter_error_review.md`)
- **PR not RCV.** (memory: `feedback_pr_not_rcv.md`)
