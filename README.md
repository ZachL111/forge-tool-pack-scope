# forge-tool-pack-scope

`forge-tool-pack-scope` is a compact Python repository for cli tools, centered on this goal: Package a Python local lab for pack analysis with transition tables, invalid-transition tests, and documented operating limits.

## Reason For The Project

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Forge Tool Pack Scope Review Notes

Start with `report density` and `file span`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## What It Does

- `fixtures/domain_review.csv` adds cases for file span and terminal width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/forge-tool-pack-walkthrough.md` walks through the case spread.
- The Python code includes a review path for `report density` and `file span`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## How It Is Put Together

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `file span`, `terminal width`, `argument risk`, and `report density`.

The added Python path is deliberately direct, with fixtures doing most of the explaining.

## Run It

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Check It

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Boundaries

The fixture set is small enough to audit by hand. The next useful expansion is malformed input coverage, not extra surface area.
