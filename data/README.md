# Data

Input files for `Gene42.ipynb`:

- `log(CPM_Matrix) DATA - Biotrack.xlsx` — log2(CPM + 1) gene-expression matrix.
- `ADOMICS Metadata_Kh.csv.xlsx` — sample metadata and diagnosis labels.

The notebook cleans gene identifiers, checks the inputs, and performs all label-dependent selection inside each training split. Do not add restricted patient data or credentials to this directory.
