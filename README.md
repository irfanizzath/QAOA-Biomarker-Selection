# Gene42: Quantum-Optimised Biomarker Selection

Gene42 selects compact gene panels that distinguish lung adenocarcinoma (LUAD) from non-cancerous samples. The notebook combines leakage-free patient-level validation, an mRMR-inspired QUBO, QAOA, classical optimisers, and feature-selection baselines.

The study uses 26 patients and selects four genes. QAOA is evaluated with Qiskit Aer and, for a feasibility check, on IBM Quantum's `ibm_marrakesh` backend. Hardware logs and summary tables are included in the repository.

## Repository contents

| Path | Description |
|---|---|
| `Gene42.ipynb` | Complete preparation, shortlist, QUBO, solver, validation, hardware, and reporting pipeline |
| `data/` | Input expression matrix and sample metadata |
| `results/` | Cross-validation, compute-budget, panel, and hardware summaries |
| `seeds/` | Logs for the recorded IBM Quantum runs |
| `requirements.txt` | Pinned Python dependencies |

## Run

Use Python 3.11, install the dependencies, and open `Gene42.ipynb` in Jupyter or Colab:

```bash
pip install -r requirements.txt
```

The notebook can reproduce the analysis and saved hardware summaries without an IBM account. Running new hardware jobs requires IBM Quantum credentials and access to the configured backend; keep credentials outside the notebook.

## Reported panel

The saved final panel is:

`FGFRL1`, `CLCA4`, `DPY19L1`, `DNASE1L3`

This is an experimental research result, not a clinically validated diagnostic signature. The hardware experiment demonstrates feasibility only; it does not establish quantum advantage.

## Team

Mohamed Irfan · Bogdan Egorov · Jayanth Venkatesan · Hasmik Chilingaryan — University of Birmingham Dubai
