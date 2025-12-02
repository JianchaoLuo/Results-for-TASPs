# Results-for-TASPs
Results for small scale TASPs contains TASPs with n = 6-10
Results for large scale TASPs contains TASPS with n = 30,50,80,120
# Results-for-TASPs

This repository stores experimental results and related data for Task Assignment and Scheduling Problems (TASPs). It provides organized results for both small-scale and large-scale instances, reproduction scripts, and evaluation tools.

## Overview
- Small-scale TASPs: instances with `n = 6, 7, 8, 9, 10`.
- Large-scale TASPs: instances with `n = 30, 50, 80, 120`.
- Contents include raw results, instance files, execution scripts, and documentation.

## Repository Structure
- `results/` — Experiment outputs (CSV, JSON, logs).
- `instances/` — Problem instance files.
- `scripts/` — Scripts to run experiments, evaluate results, and plot figures.
- `docs/` — Additional documentation and visualizations.
- `README.md` — This file.

## File Naming Conventions
- Instance files: `instance_n{n}_id{m}.json` (e.g. `instance_n30_id2.json`).
- Result files: `result_n{n}_id{m}_{method}.csv` (e.g. `result_n50_id1_greedy.csv`).
- Logs: `results/logs/run_YYYYMMDD_HHMMSS.log`.

## Reproducing Experiments (example)
1. Prepare environment (use virtualenv or container)
   - Install dependencies according to `scripts` instructions.
2. Run a single instance (example)
   - `python scripts/run_instance.py --input instances/instance_n30_id1.json --output results/result_n30_id1_methodA.csv`
3. Run batch experiments (example)
   - `python scripts/run_batch.py --instances instances/ --outdir results/`
4. Evaluate and plot (example)
   - `python scripts/evaluate.py --results results/ --out plots/`

## Result Format
Each result file should include key metrics such as:
- `total_time` — total computation time
- `objective` — objective value or cost
- `task_completion_rate` — fraction of completed tasks
- `resource_utilization` — utilization metrics
- `method` and parameter fields to identify algorithm and settings

Adjust fields according to the actual `scripts/evaluate.py` and result headers.

## Dataset & Instance Notes
- Small instances are intended for quick testing and algorithm debugging.
- Large instances are for scalability and performance evaluation.
- Instance generation scripts (if any) should be placed in `scripts/` and documented.

## Citation & License
- If using data or results from this repository, cite the repository in publications and include a link.
- Add a `LICENSE` file to specify the license for data and code.

## Contact
- For questions or contributions, use the repository Issues page or contact the maintainers listed on the repository.