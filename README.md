# temp_corrections_mw

_Created: 14-06-2026 · Last updated: 11-07-2026_

Working repository for analyzing and applying English spell-check corrections to the
**MW** (Monier-Williams Sanskrit–English Dictionary) digitization. Part of the
[sanskrit-lexicon](https://github.com/sanskrit-lexicon) project (Cologne Digital
Sanskrit Dictionaries).

> This is a **staging / analysis workspace**, not a delivery repo. Candidate errors
> are reviewed here and confirmed changes recorded in
> [`suggest_changes.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/suggest_changes.txt);
> they are applied to the canonical `csl-orig` MW source through the standard
> correction workflow, not committed back into these `.txt` exports.

## Status

Active as of July 2026. The error list is drawn from the
[sanskrit-lexicon/CORRECTIONS](https://github.com/sanskrit-lexicon/CORRECTIONS)
English spell-check pipeline. Two issues have been filed against this repo — one
still open (a `question`/`trivial` query on botanical names: typo vs scan error,
June 2026), one closed (SCH/Scholiast markup change). A suggested-changes list has
been accumulated but not yet promoted into `csl-orig` via a committed change file.

## Contents

| File | Purpose |
|---|---|
| [`mw.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/mw.txt) | MW dictionary text (source under review, ~50 MB) |
| [`mw_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/mw_error.txt) | English spelling errors flagged in MW entries (234 lines), from the CORRECTIONS pipeline |
| [`suggest_changes.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/suggest_changes.txt) | Suggested correction text for reviewed errors (1,745 lines) |

## Workflow

1. Start from [`mw_error.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/mw_error.txt)
   (the CORRECTIONS repo's English spell-check output).
2. Review each candidate — distinguish genuine errors from intentional usage
   (Latin, technical terms, proper names).
3. Record confirmed changes in
   [`suggest_changes.txt`](https://github.com/sanskrit-lexicon/temp_corrections_mw/blob/main/suggest_changes.txt).
4. Apply corrections to the canonical `csl-orig` MW source (`v02/mw/mw.txt`) through
   the Cologne correction workflow (`updateByLine.py` change files), documented in
   [csl-corrections/docs/correction-workflow.md](https://github.com/sanskrit-lexicon/csl-corrections/blob/main/docs/correction-workflow.md).
   Corrections are **never** made directly to source files — they are expressed as
   change files applied by scripts.

## Dependencies

- **Python 3**.
- [sanskrit-lexicon/CORRECTIONS](https://github.com/sanskrit-lexicon/CORRECTIONS) —
  upstream source of the error lists.
- The canonical MW source `mw.txt` lives in the `csl-orig` tree at
  `csl-orig/v02/mw/mw.txt`.

_Dr. Mārcis Gasūns_
