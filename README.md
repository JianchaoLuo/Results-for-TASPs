# Results-for-TASPs

This repository contains experimental results for TASPs (Task Assignment / Scheduling Problems).

## Overview
- **Results for small scale TASPs**: contains TASPs with n = 6–10.
- **Results for large scale TASPs**: contains TASPs with n = 30, 50, 80, 120.

Each results folder contains CSV files with output from experiments. Filenames encode experiment variants and parameter values (see notes below).

## Folder contents (high level)
- `Results for small scale TASPs/` — CSVs from small instance experiments (n = 6..10).
- `Results for large scale TASPs/` — CSVs from larger instance experiments (n = 30,50,80,120).
- `Results of B&BA1 and B&BA2 for large scale TASPs/` — results for B&BA variants run on large-scale instances.

Typical file name examples found in the repository:
- `Result0.csv`, `Result05.csv`, `Result10.csv` — result summaries for different parameter values (e.g., 0.0, 0.5, 1.0).
- `Sequence0.csv`, `Sequence05.csv`, `Sequence10.csv` — solution sequences or orderings for corresponding parameter values.
- `TAFSPs0.csv`, `TAFSPs05.csv`, `TAFSPs10.csv` — per-instance TAFSP outputs.
- `ResultB&BA0.csv`, `SequenceB&BA0.csv` — B&BA variant outputs (note `&` may be inconvenient for some tools; see suggestions).

## Notes and suggestions
- File naming: Numeric suffixes such as `0`, `05`, `10` are used to represent parameter values (commonly 0.0, 0.5, 1.0). Consider adopting an explicit, machine-safe naming convention such as `result_scale-0.0.csv`, `result_scale-0.5.csv`, `result_scale-1.0.csv` and avoiding special characters like `&` in filenames.
- Metadata: Each results folder should ideally include a small `metadata.json` or `params.yaml` recording how files were generated (script name and version, parameters, random seeds, and generation date) to improve reproducibility.
- Encoding & delimiters: Ensure CSV files are UTF-8 encoded and use a consistent delimiter (commas). Add a short example for loading files with Python/pandas if useful.

## Quick example (Python)
```python
import pandas as pd

# load a results file
df = pd.read_csv('Results for large scale TASPs/Result05.csv', encoding='utf-8')
print(df.head())
```

If you want, I can:
- Add a `DATA_DESCRIPTION.md` with a data dictionary for each CSV's columns.
- Normalize file names and add a mapping file showing old → new names.
- Create a small `notebooks/overview.ipynb` to demonstrate loading and visualizing key metrics.

Please tell me which of the above you'd like me to add next.
