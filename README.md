# PS-Q1 Variational Quantum Classifier

Phase 1 submission for Qiskit Fall Fest 2026. This project classifies a synthetic binary dataset with a 4-qubit variational quantum classifier and compares the same logical circuit on participant-defined Processor A (5 qubits) and Processor B (9 qubits).

## Scope

- Problem statement: PS-Q1 Variational Quantum Classifier.
- Dataset: `sklearn.datasets.make_classification(n_samples=200, n_features=4, n_informative=3, random_state=42)`.
- Train/test split: 80/20, deterministic seed 42.
- Primary comparison: circuit depth, CX count, SWAP/routing overhead, and classification metrics.
- Phase 1 scope: Processor A and Processor B only. Processor C and D are not benchmarked.

## Setup

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook main.ipynb
```

Run all notebook cells from top to bottom. Results are written to `results/tables/` and `results/figures/`.

## Repository map

See `main.ipynb` for the end-to-end experiment, `src/` for implementation, `processors/` for the two coupling graphs, and `report.md` for the architectural analysis.

## Reproducibility

All random seeds, split settings, transpilation settings, and shot counts are recorded in the notebook. Do not report numbers until the notebook has been run successfully and the generated files have been inspected.
