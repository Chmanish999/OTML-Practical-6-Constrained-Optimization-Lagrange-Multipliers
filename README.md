# OTML Practical 6: Constrained Optimization and Lagrange Multipliers

## Project Title

**Constrained Optimization and Lagrange Multipliers in Optimization Techniques for Machine Learning**

## Repository Name

`OTML-Practical-6-Constrained-Optimization-Lagrange-Multipliers`

## Subject

**Optimization Techniques for Machine Learning (OTML)**

## Practical Number

**Practical 6**

## Objective

The objective of this practical is to understand the concept of constrained optimization and the use of Lagrange multipliers for solving optimization problems with equality constraints.

After completing this practical, students will be able to:

- Understand constrained optimization problems.
- Identify objective functions and constraints.
- Construct a Lagrangian function.
- Compute partial derivatives.
- Solve simultaneous equations to obtain the optimal solution.
- Relate Lagrange multipliers with machine learning optimization problems.

## Theory

In many optimization problems, we are not allowed to choose any value freely. Some restrictions must be satisfied. These restrictions are called **constraints**.

A general constrained optimization problem can be written as:

```text
Minimize or Maximize: f(x, y)

Subject to: g(x, y) = 0
```

Here:

| Symbol | Meaning |
|---|---|
| `f(x, y)` | Objective function |
| `g(x, y)` | Constraint function |

## What are Lagrange Multipliers?

Lagrange multipliers are used to solve optimization problems subject to constraints.

Instead of solving the objective function and constraint separately, we combine both into a single function called the **Lagrangian function**.

For example:

```text
Objective function:
f(x, y) = x² + y²

Constraint:
x + y = 10
```

The constraint can be written as:

```text
g(x, y) = x + y - 10 = 0
```

The Lagrangian function is:

```text
L(x, y, λ) = f(x, y) + λg(x, y)
```

Therefore:

```text
L(x, y, λ) = x² + y² + λ(x + y - 10)
```

## Practical Workflow

```text
Objective Function
        ↓
Constraint
        ↓
Construct Lagrangian Function
        ↓
Differentiate Partially
        ↓
Solve Simultaneous Equations
        ↓
Obtain Optimal Solution
```

## Python Libraries Used

This practical uses the following Python library:

```python
import sympy as sp
```

## Code Explanation

### Step 1: Import the SymPy Library

```python
import sympy as sp
```

### Step 2: Define Symbols

```python
x, y, lam = sp.symbols('x y lam')
```

Here:

| Symbol | Meaning |
|---|---|
| `x, y` | Optimization variables |
| `lam` | Lagrange multiplier |

### Step 3: Define Objective Function and Constraint

```python
f = x**2 + y**2
constraint = x + y - 10
```

### Step 4: Construct the Lagrangian Function

```python
L = f + lam * constraint

print("Lagrangian Function:")
print(L)
```

### Step 5: Compute Partial Derivatives

```python
dL_dx = sp.diff(L, x)
dL_dy = sp.diff(L, y)
dL_dlam = sp.diff(L, lam)

print(dL_dx)
print(dL_dy)
print(dL_dlam)
```

### Step 6: Solve the System of Equations

```python
solution = sp.solve(
    [dL_dx, dL_dy, dL_dlam],
    (x, y, lam)
)

print(solution)
```

## Output

The solution obtained is:

```text
x = 5
y = 5
λ = -10
```

Now checking the constraint:

```text
x + y = 10
5 + 5 = 10
```

The constraint is satisfied.

The value of the objective function is:

```text
f(x, y) = x² + y²
f(5, 5) = 25 + 25 = 50
```

Hence, the optimal solution is:

```text
x = 5, y = 5
```

## Relevance in Machine Learning

Lagrange multipliers are widely used in machine learning and optimization.

| Machine Learning Area | Use of Lagrange Multipliers |
|---|---|
| Support Vector Machines | Margin optimization |
| Deep Learning | Constrained optimization |
| Resource Allocation | CPU, memory, and cloud resource constraints |
| Probability Models | Normalization constraints |
| Regularization | Penalty-based optimization |

## Learning Outcome

By completing this practical, students understand that:

- Lagrange multipliers help solve optimization problems under constraints.
- Objective functions and constraints can be combined into a Lagrangian function.
- The optimal solution must satisfy both the objective condition and the constraint condition.
- This topic forms the foundation for convex optimization and Support Vector Machines.

## Files Included

| File Name | Description |
|---|---|
| `OTML_Practical_6_Lagrange_Multipliers.ipynb` | Main Jupyter Notebook |
| `README.md` | Project documentation |
| `requirements.txt` | Required Python libraries |

## Requirements

Create a `requirements.txt` file with the following content:

```text
sympy
jupyter
```

## How to Run This Practical

### Step 1: Clone the Repository

```bash
git clone https://github.com/Chmanish999/OTML-Practical-6-Constrained-Optimization-Lagrange-Multipliers.git
```

### Step 2: Move into the Project Folder

```bash
cd OTML-Practical-6-Constrained-Optimization-Lagrange-Multipliers
```

### Step 3: Install Required Libraries

```bash
pip install -r requirements.txt
```

### Step 4: Open Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
OTML_Practical_6_Lagrange_Multipliers.ipynb
```

## Conclusion

This practical demonstrates how constrained optimization problems can be solved using Lagrange multipliers. The example helps students understand the mathematical foundation of optimization used in machine learning models such as Support Vector Machines, probabilistic models, regularization, and resource allocation problems.
