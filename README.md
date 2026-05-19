# OTML Practical 6: Constrained Optimization and Lagrange Multipliers

## 1. Aim

The aim of this practical is to understand constrained optimization and the use of Lagrange multipliers for solving optimization problems with equality constraints.

In this practical, students solve a simple constrained optimization problem by constructing the Lagrangian function, computing partial derivatives, solving simultaneous equations, and verifying the optimal solution.

---

## 2. Course and Module Mapping

**Course:** A8751 – Optimization Techniques in Machine Learning  
**Module:** Module 1 – Model Fitting and Error Measurement  
**Practical Topic:** Constrained Optimization and Lagrange Multipliers

This practical is mapped with Module 1 of OTML, where students study optimization foundations, model fitting, constraints, objective functions, and mathematical techniques used in machine learning optimization.

---

## 3. Theory Background

In many optimization problems, we cannot choose any value freely. Some restrictions must be satisfied. These restrictions are called **constraints**.

A constrained optimization problem contains two main parts:

| Component | Meaning |
|---|---|
| Objective function | Function to be minimized or maximized |
| Constraint | Condition that must be satisfied |

A general equality-constrained optimization problem can be written as:

```text
Minimize or Maximize: f(x, y)

Subject to: g(x, y) = 0
