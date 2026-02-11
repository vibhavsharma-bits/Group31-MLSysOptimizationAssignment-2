# Group31 — ML Systems Optimization Assignment 2

## Parallel and Distributed SGD: Systems-Level Performance Analysis

This repository contains Assignment 2 for the ML Systems Optimization course. The project investigates how different execution strategies influence the system-level performance of stochastic gradient descent (SGD). The study focuses on execution behaviour rather than improving model accuracy.

The analysis compares serial execution, shared-memory parallelism using lock-free updates, and distributed data-parallel training with periodic model averaging. Additional experiments explore scalability behaviour, synchronization trade-offs, and workload sensitivity to understand practical system constraints affecting machine learning performance.

---

## Repository Contents

- Jupyter Notebook containing full implementation and experimental analysis.
- Final report describing design evolution, results, and systems-level insights.
- Visualizations generated from experimental evaluation.

---

## Execution Environment

Experiments were executed using:

- Google Colab (CPU runtime)
- Python 3 environment
- Jupyter Notebook workflow

Google Colab was used to ensure reproducibility and consistent execution environment.

---

## Technologies Used

- Python 3
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Python threading (shared-memory parallel execution)
- Jupyter Notebook
- Google Colab

---

## Experimental Overview

The notebook follows an iterative experimental workflow:

1. **Serial SGD Baseline**
   - Sequential training used as reference performance benchmark.

2. **Shared-Memory Parallel SGD**
   - Multithreaded execution using lock-free asynchronous updates (HOGWILD-style).

3. **Distributed Data-Parallel SGD**
   - Independent workers with periodic synchronization via model averaging.

4. **Extended Analysis**
   - Parallel scaling behaviour
   - Synchronization frequency analysis
   - Workload scalability experiments

The objective is to analyse system-level trade-offs including execution overhead, coordination cost, and practical scalability limitations.

---

## Key Systems Insights

- Increasing parallelism does not automatically improve performance.
- Python runtime constraints (e.g., GIL) significantly influence shared-memory parallel execution.
- Distributed training introduces communication overhead that impacts efficiency.
- Effective scalability depends on workload size relative to coordination overhead.

---

## How to Run

1. Open the Jupyter notebook.
2. Restart the kernel/runtime.
3. Select **Run All** to execute all experiments sequentially.
4. All results and visualizations will be generated automatically.

### Note on Reproducibility

Due to system-level factors such as CPU load, thread scheduling, runtime environment behaviour, and lock-free asynchronous execution, exact timing values may vary slightly across runs.

While numerical results (e.g., training time) may differ, overall trends and system-level insights discussed in the report are expected to remain consistent.

---

## Deliverables

- Notebook implementation (.ipynb / PDF)
- Final report (PDF)
- GitHub repository submission

---

## References

[1] S. H. Haji and A. M. Abdulazeez, Comparison of Optimization Techniques Based on Gradient Descent Algorithm: A Review, PJAEE, 2021.  
[2] M. Zinkevich et al., Parallelized Stochastic Gradient Descent, NIPS, 2010.  
[3] J. Dean et al., Large Scale Distributed Deep Networks, NIPS, 2012.  
[4] M. Li et al., Communication Efficient Distributed Machine Learning with the Parameter Server, NIPS, 2014.  
[5] F. Niu et al., HOGWILD!: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent, NIPS, 2011.  
[6] Y. Lin et al., Deep Gradient Compression, ICLR, 2018.  
[7] P. Goyal et al., Accurate Large Minibatch SGD, arXiv, 2017.  
[8] X. Lian et al., Asynchronous Decentralized Parallel SGD, ICML, 2018.  
[9] J. Jiang et al., Bagua: Scaling Distributed Learning with System Relaxations, arXiv, 2021.

---

## Authors

Group 31 — ML Systems Optimization Assignment 2
