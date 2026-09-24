# A_02 · Python NumPy Tutorial

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.x-013243?logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-VS%20Code-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-success)

## Student Information

| Field | Details |
|---|---|
| **Name** | Nabonita Das |
| **Email** | nabonita@umich.edu |
| **Student ID** | 35226076 (UMich ID) |
| **Course** | ECE 5831-001 / ECE 5831-002 (Fall 2026) |
| **Assignment** | HW#2 (A_02): Python NumPy Tutorial |
| **GSI** | Elahe Delavari ([@ElaheDlv](https://github.com/ElaheDlv)) |
| **Due Date** | Tuesday, September 29, 2026, 11:59 PM |
| **Environment** | Jupyter Notebook in Visual Studio Code |

---

## Overview

This assignment completes the NumPy section of the
[CS231n Python NumPy Tutorial](https://cs231n.github.io/python-numpy-tutorial/).
Every example from the tutorial is reproduced and run. Each topic also has
**"Going further"** experiments and ends with **mini challenges** that are
vectorized and checked with `assert` statements.

## Repository Structure

```
ece-5831-2026-assignments/
└── A_02/
    ├── numpy-tutorials.ipynb   # Completed NumPy tutorial (exercises + examples)
    └── README.md               # This file
```

## Files

| File | Description |
|---|---|
| `numpy-tutorials.ipynb` | The main notebook. It has a Markdown explanation for each topic, all CS231n tutorial examples with saved outputs, extra experiments, performance benchmarks, and three self-checking mini challenges. |
| `README.md` | Describes the assignment, the files, and the work completed. |

## Work Completed

| # | Section | What was done |
|---|---|---|
| 0 | **Setup** | Printed the environment versions and used a seeded `np.random.default_rng` for reproducible results. |
| 1 | **NumPy** | Explained why `ndarray` is fast (contiguous memory, compiled loops) and **benchmarked** a Python list against a NumPy array (about 40x faster). |
| 2 | **Arrays** | Covered rank, shape, and the constructors `zeros`, `ones`, `full`, `eye`, `random`, `arange`, `linspace`. Inspected `ndim`, `size`, `itemsize`, `nbytes` and practiced `reshape` / `np.newaxis`. |
| 3 | **Array indexing** | Covered slicing, mixing integer indexes with slices (effect on rank), integer array indexing, the one-element-per-row trick, and boolean masks. Used `np.shares_memory` to check **view vs. copy**, and practiced `np.where` and compound masks. |
| 4 | **Data types** | Covered `dtype` inference and explicit types, upcasting rules, `astype` truncation vs. rounding, **integer overflow** (`uint8` wrap-around), float precision (`finfo`), and why to use `np.isclose`. |
| 5 | **Array math** | Covered elementwise operators and their ufunc equivalents, `dot` / `@`, `sum` along axes, and transpose. Also used `mean`, `max`, `argmax`, `std`, `keepdims`, and numerically checked the identity (AB)ᵀ = BᵀAᵀ. |
| 6 | **Broadcasting** | Compared the loop, `np.tile`, and broadcasting approaches with a **benchmark**. Stated the four broadcasting rules and tested them with `np.broadcast_shapes`. Reproduced all tutorial applications: outer product, adding to rows and columns, scalar scaling. |
| 7 | **Mini challenges** | (1) Z-score feature standardization, (2) numerically stable row-wise softmax, (3) loop-free pairwise Euclidean distances. Each is checked against a reference with `assert`. |
| 8 | **Summary** | A key-takeaways table and references. |

## Key Takeaways

- **Vectorize.** Replacing Python loops with array operations gave a 10–50x speed-up in this notebook.
- **Slices are views.** Changing a slice changes the original array. Integer array and boolean indexing return copies.
- **Watch your dtypes.** Fixed-width integers overflow silently, and float comparisons need a tolerance.
- **Think in shapes.** Broadcasting aligns shapes from the right. Dimensions must match or be 1.

## How to Run

1. Clone the repository and open it in **VS Code**.
2. Install the **Python** and **Jupyter** extensions.
3. Install the dependency:
   ```bash
   pip install numpy
   ```
4. Open `A_02/numpy-tutorials.ipynb`, select a Python 3 kernel, and click **Run All**.

The benchmark timings will differ from machine to machine. Every other output is deterministic because the random generator is seeded.

## References

1. CS231n: *Python NumPy Tutorial*. https://cs231n.github.io/python-numpy-tutorial/
2. NumPy Documentation: *Broadcasting*. https://numpy.org/doc/stable/user/basics.broadcasting.html
3. NumPy Documentation: *Indexing on ndarrays*. https://numpy.org/doc/stable/user/basics.indexing.html
4. NumPy Documentation: *Data types*. https://numpy.org/doc/stable/user/basics.types.html
