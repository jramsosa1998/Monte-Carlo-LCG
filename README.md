# Rebuilding a Linear Congruential Generator in Python

## Overview
This project rebuilds a pseudo-random number generator from an older ROOT/C++ implementation using Python. 

The notebook implements a linear congruential generator (LCG), evaluates the statistical properties of the generated sequence, and extends the analysis into a Monte Carlo simulation to estimate π.

---

## Mathematical Formulation

The generator follows the recurrence relation:

$$
x_{n+1} = (a x_n + c) \bmod M
$$

The sequence is normalized to the interval $[0,1]$:

$$
u_n = \frac{x_n}{M - 1}
$$

**Parameters used:**
- $a = 16807$
- $c = 0$
- $M = 2147483647$
- $x_0 = 3$

---

## Methodology

The project proceeds in three stages:

1. **Generator Implementation**
   - Custom LCG built from first principles

2. **Statistical Evaluation**
   - Histogram to assess uniformity
   - Lag plot to detect short-range correlation

3. **Monte Carlo Simulation**
   - Random sampling in the unit square
   - Estimation of π based on point inclusion

---

## Results

Using 10,000 sampled points:

- Estimated π: **3.14**
- True π: **3.141592653589793**
- Absolute error: **~0.00159**

---

## Why This Project Matters

This project demonstrates:

- Translating legacy scientific code into modern Python
- Understanding pseudo-random number generation
- Applying simulation techniques (Monte Carlo methods)
- Communicating technical work clearly through structured notebooks

---

## Repository Structure

- `MonteCarlo.ipynb` — main notebook containing implementation and analysis