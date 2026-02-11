# Group31 — ML Systems Optimization Assignment 2

## Parallel and Distributed SGD: Systems-Level Performance Analysis

This repository contains Assignment 2 for the ML Systems Optimization course.  
The project investigates how different execution strategies influence the system-level performance of stochastic gradient descent (SGD) without modifying the underlying learning algorithm.

The focus is on execution efficiency, scalability behaviour, synchronization overhead, and practical runtime constraints from a systems engineering perspective.

---

## Project Overview

Rather than improving model accuracy, this study examines how execution architecture affects training performance.

Three execution models are evaluated:

- Serial SGD baseline
- Shared-memory parallel SGD (lock-free / HOGWILD-style)
- Distributed data-parallel SGD (model averaging)

Additional experiments extend analysis to explore:

- Parallel scaling behaviour
- Synchronization frequency trade-offs
- Workload scalability characteristics

The goal is to understand how theoretical parallelism compares with practical system performance.

---

## Repository Structure

- `MLSysOptimization-Assignment2.ipynb`  
  Main notebook containing all experiments, analysis, and visualizations.

- `Assignment2_Report.pdf`  
  Final written report with structured discussion and system-level insights.

- `README.md`  
  Repository overview and execution instructions.

---

## Experimental Focus

The experiments isolate execution effects by keeping:

- Dataset
- Model architecture
- Optimization procedure
- Hyperparameters

constant across implementations.

Performance is evaluated using:

- Training time (wall-clock execution)
- Prediction accuracy
- Relative speedup vs serial baseline

---

## Key Systems Insights

- Serial execution can outperform parallel approaches when workload size is small.
- Shared-memory parallelism introduces coordination overhead and Python runtime constraints.
- Distributed training introduces synchronization and communication trade-offs.
- Practical scalability depends on workload size, execution environment, and system architecture.

---

## How to Run

1. Open the Jupyter notebook.
2. Restart the kernel.
3. Select **Run All** to execute the complete workflow.
4. All experiments, analysis sections, and visualizations will be generated automatically.

### Note on Reproducibility

Due to system-level factors such as CPU load, thread scheduling, runtime environment behaviour, and lock-free asynchronous execution, exact timing values may vary slightly across runs. While numerical results (e.g., training time) may differ, overall performance trends and system-level insights discussed in the report are expected to remain consistent.

---

## Technologies Used

- Python
- NumPy
- Scikit-learn
- Matplotlib
- Multithreading (Python threading module)

---

## References

Key references include work on parallel SGD, distributed training, and lock-free optimization methods such as HOGWILD-style updates.

---

## Author / Group

Group31 — ML Systems Optimization Course
