# Group31 — ML Systems Optimization Assignment 2

## Parallel and Distributed SGD: Systems-Level Performance Analysis

This repository contains Assignment 2 for the ML Systems Optimization course.

The project investigates how different execution strategies influence the system-level performance of stochastic gradient descent (SGD) without modifying the underlying learning algorithm.

### Contents

- Jupyter Notebook implementing:
  - Serial SGD baseline
  - Shared-memory parallel SGD (lock-free / HOGWILD-style)
  - Distributed data-parallel SGD (model averaging)
  - Extended analysis experiments (scaling, synchronization frequency, workload analysis)

- Experimental report (PDF)

### Objective

The study focuses on execution efficiency, scalability behaviour, synchronization overhead, and practical runtime constraints from a systems engineering perspective.

### How to Run

1. Open the Jupyter notebook.
2. Restart the kernel.
3. Select **Run All** to execute the complete workflow.
4. All experiments, analysis sections, and visualizations will be generated automatically.

### Note on Reproducibility

Due to system-level factors such as CPU load, thread scheduling, runtime environment behaviour, and lock-free asynchronous execution, exact timing values may vary slightly across runs. While numerical results (e.g., training time) may differ, overall performance trends and system-level insights discussed in the report are expected to remain consistent.
