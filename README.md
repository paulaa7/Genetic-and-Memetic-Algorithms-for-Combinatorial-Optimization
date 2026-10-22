# Genetic and Memetic Algorithms for Combinatorial Optimization

C++ implementations of genetic and memetic algorithms for combinatorial optimization, developed as part of the Metaheuristics coursework in the Computer Engineering degree at the University of Granada.

The project explores different evolutionary search strategies and compares their performance using fitness and execution-time measurements across benchmark instances.

## Overview

The implementation includes seven algorithm variants:

- **Generational Genetic Algorithms (GGA):** position-based and uniform crossover variants.
- **Steady-State Genetic Algorithms (SSGA):** position-based and uniform crossover variants.
- **Memetic Algorithms:** three variants with different local-search configurations.

The algorithms share a common optimization interface, allowing different strategies to be evaluated on the same problem under a consistent evaluation budget.

## Key Features

- Modular C++ implementation separating the optimization problem from the search algorithms.
- Multiple genetic and memetic search strategies.
- Fitness evaluation and best-solution tracking.
- Reproducible runs using configurable random seeds.
- Automated execution across 50 benchmark instances.
- CSV output for fitness and execution-time analysis.

## Tech Stack

- **Language:** C++
- **Build system:** CMake
- **Automation:** Bash
- **Analysis:** Jupyter Notebook, CSV

## Project Structure

- `main.cpp` — initializes the problem and runs the algorithm variants.
- `inc/` — algorithm and problem interfaces.
- `src/` — algorithm and problem implementations.
- `common/` — shared metaheuristics framework components.
- `datos_MDD/` — benchmark instance files.
- `P2.ipynb` — notebook for analysis and experimentation.
- `ejecucion.sh` — batch execution script.
- `solo_fitness.csv` and `solo_tiempo.csv` — collected performance measurements.

## Building and Running

The project uses CMake and a C++ compiler.

```bash
cmake -S . -B build
cmake --build build
```

Run the executable from the project root with a random seed and a benchmark instance name:

```bash
./build/main 15 GKD-b_1_n25_m2
```

The exact executable path may depend on your build configuration.

The batch script `ejecucion.sh` automates experiments across the included benchmark instances and collects fitness and runtime measurements. Review the script before running it, as it deletes existing output CSV files.

## Experimental Analysis

The project records fitness and execution time to support comparisons between algorithm variants and benchmark instances. The accompanying notebook and CSV files provide a starting point for analysing search performance.

No universal performance ranking is claimed: results depend on the benchmark instance, algorithm configuration, and experimental setup.

## Context

Developed as an academic project for the Metaheuristics course at the University of Granada. The repository is intended to demonstrate algorithm design, modular C++ implementation, and experimental comparison of optimization strategies.
