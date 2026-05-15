# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**temp_corrections_mw** is a working repository for analyzing and applying corrections to the MW (Monier-Williams Sanskrit-English Dictionary) digitization.

## Architecture

| File | Purpose |
|---|---|
| `mw.txt` | MW entries flagged for review |
| `mw_error.txt` | English spelling errors identified in MW entries |
| `suggest_changes.txt` | Suggested correction text for reviewed errors |

## Workflow

1. Start from `mw_error.txt` (from CORRECTIONS repo's English spell-check pipeline)
2. Review each candidate — distinguish genuine errors from intentional usage (Latin, technical terms, proper names)
3. Write confirmed changes to `suggest_changes.txt`
4. Apply corrections via `updateByLine.py` to `csl-orig/v02/mw/mw.txt`

## Dependencies

- **Python 3**
- **CORRECTIONS** sibling repo — source of the error lists
- **mw.txt** — in `$BASE/cologne/csl-orig/v02/mw/mw.txt`
