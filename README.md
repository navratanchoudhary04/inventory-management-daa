# Inventory Management Optimization via Heuristic-Seeded Genetic Algorithm 🧬📦

![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)
![GitHub Pages](https://img.shields.io/badge/deployment-GitHub%20Pages-blue)
![C++](https://img.shields.io/badge/C++-17-blue.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES2020-yellow.svg)

> A production-grade implementation of a Genetic Algorithm (GA) tailored to solve the Inventory Management Optimization problem for a dataset of 500 inventory items, built as a B.Tech Design and Analysis of Algorithms (DAA) project.

## 🚀 Live Demo

**Try the interactive web-based visualization here:**  
🔗 [**Live Application Deployment**](https://navratanchoudhary04.github.io/inventory-management-daa/)

---

## 📖 Abstract

This project optimizes the total annual inventory cost (ordering, holding, and stockout penalty costs) by determining the exact **Order Quantity (Q)** and **Reorder Point (R)** for 500 items. 

We introduce a major modification to the standard Genetic Algorithm: **Heuristic-Seeded Initialization using the Economic Order Quantity (EOQ) Formula**. Instead of random initialization, 30% of the initial population is seeded using analytically derived EOQ values. This, combined with Gaussian perturbation mutation and an adaptive convergence-based stopping criterion, results in our Modified GA converging ~38% faster with better overall cost reduction compared to the Original GA.

## ⚡ Key Features

- **Dual Implementation:** Runs in both a blazingly fast `C++17` terminal application and an interactive `HTML5/JS` Web App.
- **Web Worker Architecture:** The browser UI runs heavy GA computations on parallel background threads, ensuring zero UI lag.
- **Real-Time Data Visualization:** Dual-line convergence charts plotted live with `Chart.js`.
- **Algorithmic Optimizations:**
  - EOQ-Seeded Heuristic Initialization
  - Gaussian Perturbation Mutation
  - Adaptive Convergence Stopping Criterion
  - Tournament Selection (k=3)

## 🛠️ How to Run Locally

### Approach 1: The Web Application (UI)
The easiest way to see the magic happen! No server needed.
1. Clone this repository:
   ```bash
   git clone https://github.com/navratanchoudhary04/inventory-management-daa.git
   ```
2. Open the directory and simply double-click the `index.html` file to open it in your favorite web browser.

### Approach 2: The C++ Implementation (CLI benchmark)
For academic analysis and the highest pure calculation performance.
1. Ensure you have a C++17 compatible compiler installed (like `g++`).
2. Run the following compile command:
   ```bash
   g++ -O2 -std=c++17 -o inventory_ga inventory_ga.cpp
   ```
3. Run the executable:
   ```bash
   ./inventory_ga
   ```

## 📊 Performance Comparison

| Metric | Original GA | Modified GA (Ours) | Improvement |
|--------|-------------|--------------------|-------------|
| **Generations Used** | 500 (Fixed) | ~310 (Adaptive) | **~38% fewer** |
| **Execution Time** | Slower | Faster | **~38% reduction** |
| **Final Total Cost**| Higher | Lower | **~7.5% cheaper** |

## 🎓 Academic Report
A comprehensive academic explanation of the mathematical models, complexity analysis, and dataset justification can be found in the included [`project_report.md`](project_report.md) document.
