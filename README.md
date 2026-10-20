# Stationary-String Framework (P1) — Publication Package

> **Türkçe:** [README_TR.md](./README_TR.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**P1: The Stationary-String Framework — A Unified FENE-P Model for Galactic, Hadronic and Laboratory Phenomenology (A Degrees-of-Freedom Ledger, a Fragility Map, and a Forensic Audit of Its Own Errors)**

Author: Fahri Meral · Date: October 20, 2026 · Version: v1 (P1)

> **Status:** Unpublished preprint (v1). Not peer-reviewed. *Zenodo DOI pending deposit.*

## What this paper is (and is not)

This is a **methods paper**: it lets the framework score its own claims.
It is **not** a claim that the Yang–Mills mass gap is solved or that dark
matter is replaced — those are explicitly out of scope and are stated as such
in Section 1 of the paper.

## Contents

| File | Description |
|---|---|
| `paper/stationary_strings_framework_p1.tex` | Main paper, Turkish (Table 1, 7 sections) |
| `paper/stationary_strings_framework_p1_EN.tex` | English version |
| `paper/ledger.json` | Machine-readable degrees-of-freedom ledger (17 rows) |
| `CITATION.cff` | Citation record |
| `LICENSE` | CC BY 4.0 |

## Key findings

- **Degrees-of-freedom ledger (Table 1):** 17 published comparisons, each with
  observable, literature value, model value, the free parameters entering,
  whether they were fitted to that datum, and a fragility measure.
  Class distribution: **2 fit, 2 fit-like, 10 transfer, 2 genuine, 1
  structural**. Grouping correlated rows gives **8 independent observable
  groups against 9 free degrees of freedom → evidence ratio 0.889**.
- **Fragility map:** the glueball mean (T33) moves by **27.8 %** for a 1 %
  shift of `C_univ`; the 1.56 % agreement is therefore **not robust**.
  Charmonium (0.05 %) and Vela (0.17 %) are practically stable.
- **Only two genuine predictions** exist (T22 Ps band budget, T37 Na-22 band
  ratio), both on the laboratory side; the other fifteen rows are fits or
  transfers. The table exposes the strongest and weakest parts of the
  series simultaneously.
- **Forensic audit:** eight error classes found and fixed inside this work
  (wrong self-adjoint extension, tautological Temple–Kato lower bound,
  transposed source formulas, a literature band that was a *ghost
  parameter*, `H_0` dependence, post-hoc multiplicative factors, a model
  contradicting its own source, hard-coded "independent" checks).

## Numerical reproduction

The ledger is a program, not a table: it recomputes every row, cross-checks
against the solver, and verifies the table in the paper.

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T37 (38/38 PASS)
python duran_sicimler_sim/ledger.py          # ledger + solver cross-check (1e-9) + table check
python duran_sicimler_sim/mini_check_audit.py # independent series audit (9/9 PASS)
```

`ledger.py` exits with a non-empty mismatch list if the table in the paper
drifts from the recomputed values.

## Citation

```bibtex
@misc{meral2026stationarystringsP1,
  author = {Fahri Meral},
  title  = {The Stationary-String Framework: A Unified FENE-P Model for Galactic, Hadronic and Laboratory Phenomenology},
  year   = {2026},
  url    = {https://github.com/fahrim/grand-proof-p1}
}
```

See also `CITATION.cff`.

## Related work

- `stationary-strings-i` … `stationary-strings-x` — Theorems I–X (the parent series).
- `grand-proof-i` / `grand-proof-ii` / `grand-proof-iii` — the three application
  papers, each of which is audited by the ledger of the present work.

## License

CC BY 4.0 — see `LICENSE`. Content is not peer-reviewed.
