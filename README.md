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
