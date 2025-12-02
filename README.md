# Results-for-TASPs

This repository collects results and tools for solving Traveling Salesman-like Assignment Problems (TASPs). It includes datasets, solver implementations, utility scripts, and experiment logs for both small-scale and large-scale instances.

## Summary
- Small-scale TASPs: instances with n = 6–10.
- Large-scale TASPs: examples with n = 30, 50, 80, 120.

## Core modules
- data/  
  Contains problem instances, generators, and input parsers. Use these to reproduce or extend tested instances.
- solvers/  
  Implementations of exact and heuristic algorithms for TASPs (e.g., branch-and-bound, greedy, local search). Each solver includes a simple CLI wrapper for batch runs.
- utils/  
  Helper scripts for common tasks: result formatting, logging, timing, and evaluation metrics.
- experiments/  
  Experiment configurations, run scripts, and parameter sweeps used to produce the results in this repository.
- results/  
  Collected output files, summaries, and plots generated from experiments.

## Quick start
1. Prepare Python (or other) environment as required by each module.
2. Place or generate problem instances in data/.
3. Run a solver from solvers/ and store outputs in results/.

Feel free to open issues or contribute new instances and solver variants.
