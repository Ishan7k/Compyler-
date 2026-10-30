# Compyler: Compass Your Coding Journey

[![Academic Track](https://img.shields.io/badge/Academic-SPPU%20Final%20Year%20Project-blue.svg)](https://github.com)
[![Architecture](https://img.shields.io/badge/Architecture-Dual--Pipeline%20Judge-orange.svg)](https://github.com)

> An adaptive online judge pairing containerized sandboxed execution with deterministic Abstract Syntax Tree (AST) pattern recognition to deliver prerequisite-aware Data Structures and Algorithms tutoring.

---

## 📌 Problem Overview
Traditional online judges evaluate submissions purely via black-box input/output matching. An optimal $O(n)$ two-pointer solution and a suboptimal $O(n^2)$ brute-force loop receive identical "Accepted" verdicts if test cases are loose.

**Compyler** decouples code evaluation into two simultaneous pathways:
1. **Functional Correctness Pipeline:** Ephemeral sandboxed execution (cgroups capped: 1.0 vCPU, 256 MB RAM, 2.0s timeout) returning AC, WA, TLE, MLE.
2. **Structural Pattern Pipeline:** Compiler-based AST analysis deterministically classifying algorithmic techniques (Brute Force, Two-Pointer, Recursion) invariant to variable naming or formatting.

---

## 📁 Repository Structure
```text
compyler/
├── frontend/    # React + Monaco Code Editor 
├── backend/     # Express API + Judge0 Runner + MongoDB 
├── analyzer/    # Java AST Pattern Parser + Prerequisite DAG 
└── docs/        # SRS, Review PPTs, Technical Specifications