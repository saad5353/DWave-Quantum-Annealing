# Quantum Annealing & D-Wave Optimization 🌀⚛️

An educational, hands-on repository demonstrating how to solve combinatorial optimization problems using **Quantum Annealing** and **QUBO (Quadratic Unconstrained Binary Optimization)** formulations. 

This project provides end-to-end Python notebooks, visual explanations, and simulated annealing code using D-Wave's open-source tools to bridge the gap between abstract quantum physics and practical computer science.

---

## 📌 Conceptual Overview

### What is Quantum Annealing?

**Quantum Annealing** is a specialized paradigm of quantum computing engineered exclusively for solving complex combinatorial optimization problems (finding the best choice among an astronomical number of possibilities).

Unlike gate-based quantum devices that run sequential logic gates, a quantum annealer uses continuous physical evolution governed by the **Adiabatic Theorem**:
1. **Initial State:** The processor starts in a strong transverse magnetic field where all qubits exist in a uniform superposition of all possible $0$ and $1$ states simultaneously.
2. **The Anneal:** The driver field is slowly turned down while your problem's energy landscape (QUBO matrix) is turned up.
3. **Quantum Tunneling:** As the system evolves, qubits exploit **quantum tunneling** to pass directly *through* tall energy barriers rather than climbing over them like classical thermal solvers.
4. **Ground State:** The system settles into its absolute lowest energy configuration—the **Ground State**—which directly encodes the optimal solution to your problem.

---

## ⚙️ The Mathematical Engine: QUBO

To run a problem on a D-Wave quantum annealer, business constraints and objective functions must be mapped into a **QUBO (Quadratic Unconstrained Binary Optimization)** matrix:

$$E(x) = \sum_{i} Q_{ii} x_i + \sum_{i < j} Q_{ij} x_i x_j$$

Where:
* $x_i \in \{0, 1\}$ are binary decision variables.
* $Q_{ii}$ (Diagonal terms) represent linear biases assigned to individual variables.
* $Q_{ij}$ (Off-diagonal terms) represent interaction penalties or rewards when variables $x_i$ and $x_j$ are active simultaneously.

---

## 💻 Repository Contents & Visualizations

The featured notebook translates the NP-complete **Max-Cut Problem** into a QUBO matrix and solves it using D-Wave's `neal` simulated annealing engine.

### Key Visualizations Included:
* **Interactive Network Graphs:** Clear, color-coded node partitions (**Group 0 vs. Group 1**) with distinct edge rendering to easily identify **Cut Edges** (successful connections) versus **Uncut Edges**.
* **Energy Distribution Histograms:** Plots of all sample reads across the energy landscape to demonstrate how the annealer reliably converges on the ground state.

---

## 🚀 Use Cases for Quantum Annealing

Quantum annealing is currently used across industry sectors for large-scale combinatorial challenges:
* **Logistics & Fleet Routing:** Solving advanced variants of the Traveling Salesperson Problem (TSP) and Vehicle Routing.
* **Financial Portfolio Optimization:** Balancing risk vs. return across correlated asset classes.
* **Telecommunications:** Frequency allocation and antenna coverage layout.
* **Drug Discovery & Molecular Folding:** Identifying low-energy molecular configurations and protein structures.

---
