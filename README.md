# 🐍 NumPy Mastery: Complete Hands-On Tutorial & Reference

[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Executed Cells](https://img.shields.io/badge/Executed%20Cells-340%2B-brightgreen.svg)](#whats-covered)
[![Author](https://img.shields.io/badge/Author-Preetham%20V%20R-purple.svg)](https://github.com/preetamvr1595)

A comprehensive, production-grade **NumPy Mastery Series** — featuring **340+ executed code cells** across 5 structured Jupyter Notebooks. Built for data science, machine learning engineers, and Python developers who want deep conceptual clarity and practical fluency with numerical computing in Python.

Unlike basic tutorials with simple `[1, 2, 3]` arrays, this series covers real-world multi-dimensional arrays, memory layouts, strides, broadcasting mechanics, structured/record arrays, vectorization, indexing traps, and linear algebra pipelines.

---

## 📌 Table of Contents

- [Overview & Key Features](#-overview--key-features)
- [Notebook Navigation](#-notebook-navigation)
- [Detailed Topic Breakdown](#-detailed-topic-breakdown)
  - [Notebook 1: Basics, Broadcasting & Ufuncs](#notebook-1-numpy-basics--memory)
  - [Notebook 2: Array Creation & I/O](#notebook-2-array-creation--io)
  - [Notebook 3: Indexing, Slicing & Views](#notebook-3-indexing--slicing)
  - [Notebook 4: Reshaping, Axis Manipulation & Stacking](#notebook-4-reshaping--stacking)
  - [Notebook 5: Searching, Sorting & Statistics](#notebook-5-searching-sorting--statistics)
- [Requirements & Quick Start](#-requirements--quick-start)
- [Why Learn NumPy?](#-why-learn-numpy)
- [Author & Connect](#-author--connect)
- [License](#-license)

---

## 🌟 Overview & Key Features

- **340+ Executed Notebook Cells**: Fully runnable code blocks with inline outputs, visualizations, and detailed explanations.
- **Deep Memory Mechanics**: Strides, memory contiguity, C-order vs Fortran-order, itemsize, flags, and `np.info()`.
- **View vs Copy Demystified**: Clear rules on when NumPy creates memory views versus full copies to prevent silent data mutation bugs.
- **Advanced Vectorization**: `ufuncs`, `np.vectorize()`, `np.select()`, `np.where()`, and multi-condition boolean indexing.
- **Real-World Pipelines**: Mini-projects including sales data analysis, image channel assembly, and polynomial curve fitting (`np.polyfit`).

---

## 📚 Notebook Navigation

Direct links to interactive Jupyter notebooks:

| Notebook | File Link | Core Focus | Executed Cells | Key Functions Covered |
| :--- | :--- | :--- | :---: | :--- |
| **01** | [`01_numpy_basics.ipynb`](01_numpy_basics.ipynb) | Basics, Memory & Ufuncs | 60+ | `dtype`, `strides`, `ufuncs`, `vectorize`, `broadcast`, `issubdtype`, `errstate` |
| **02** | [`02_array_creation.ipynb`](02_array_creation.ipynb) | Creation Routines & I/O | 70+ | `arange`, `linspace`, `logspace`, `structured arrays`, `default_rng`, `savetxt`, `char` |
| **03** | [`03_indexing_slicing.ipynb`](03_indexing_slicing.ipynb) | Indexing, Slicing & Views | 70+ | `boolean mask`, `fancy indexing`, `newaxis`, `Ellipsis`, `take`, `put`, `select` |
| **04** | [`04_reshaping_stacking.ipynb`](04_reshaping_stacking.ipynb) | Reshaping & Axis Ops | 75+ | `reshape`, `moveaxis`, `vstack`, `hstack`, `dstack`, `kron`, `outer`, `pad` |
| **05** | [`05_searching_sorting_filtering.ipynb`](05_searching_sorting_filtering.ipynb) | Searching, Sorting & Stats | 70+ | `where`, `searchsorted`, `argsort`, `partition`, `linalg`, `polyfit`, `unique` |

---

## 📖 Detailed Topic Breakdown

### Notebook 1: NumPy Basics & Memory
- **Array Fundamentals**: `ndim`, `shape`, `size`, `dtype`, `itemsize`, `nbytes`.
- **Data Types & Precision**: Complex numbers, floating-point gotchas, integer overflow edge cases.
- **Memory Layout**: Strides, C-contiguous vs F-contiguous memory blocks, checking array flags.
- **Vectorized Operations**: `ufuncs`, building custom ufuncs with `np.vectorize()`.
- **Broadcasting Rules**: Dimensions alignment, expansion mechanics, memory efficiency.
- **Reductions & Aggregations**: `sum`, `mean`, `std`, `var`, `min`, `max`, `median` along axes.
- **Safety & Debugging**: Controlling warnings with `np.errstate()`, type hierarchy inspection with `np.issubdtype()`.

### Notebook 2: Array Creation & I/O
- **Creation Routines**: `zeros`, `ones`, `full`, `empty`, `eye`, `identity`, `diag`.
- **Sequence Generators**: `arange`, `linspace`, `logspace`, `geomspace`, `vander`.
- **Coordinate Grids**: `meshgrid`, `mgrid`, `ogrid`, `indices`.
- **Structured & Record Arrays**: Defining custom tuple dtypes, attribute-style access, mixed types.
- **Modern Random API**: `np.random.default_rng()`, normal/uniform sampling, seed control.
- **Data Persistence**: Binary format (`.npy`, `.npz`), text format (`loadtxt`, `savetxt`).
- **Specialized Arrays**: `datetime64`, `timedelta64`, Masked Arrays (`numpy.ma`), String methods (`np.char`).

### Notebook 3: Indexing & Slicing
- **Basic & Multi-Dimensional Slicing**: `[start:end:step]` across 1D, 2D, and 3D arrays.
- **Advanced Selection**: Boolean masking, Fancy indexing, combined boolean + fancy selection.
- **Dimensionality Manipulation**: `np.newaxis` (`None`), `Ellipsis (...)` automatic expansion.
- **Functional Indexing**: `np.take()`, `np.put()`, `np.take_along_axis()`, `np.ix_()`.
- **Vectorized Conditionals**: Multi-branch selection with `np.select()`, `np.where()`.
- **View vs Copy Safety**: Detecting implicit memory copies, avoiding chained indexing traps (`df[a][b]` style bugs).

### Notebook 4: Reshaping & Axis Stacking
- **Shape Transformation**: `reshape()` with `-1` inferencing, `order='C'` vs `order='F'`.
- **Flattening**: `ravel()` (view) vs `flatten()` (copy).
- **Axis Relocation**: `transpose()`, `.T`, `swapaxes()`, `moveaxis()`, `rollaxis()`.
- **Array Combining & Splitting**: `concatenate`, `stack`, `vstack`, `hstack`, `dstack`, `block`, `split`, `array_split`.
- **Array Flipping & Rotation**: `flip`, `fliplr`, `flipud`, `roll`, `pad`.
- **Matrix Products**: Kronecker product (`np.kron`), Outer product (`np.outer`).
- **Real Mini-Project**: Rebuilding damaged multi-channel image grid layouts.

### Notebook 5: Searching, Sorting & Statistics
- **Searching Routines**: `np.where()`, `np.searchsorted()` (binary search), `np.nonzero()`, `np.flatnonzero()`.
- **Sorting Methods**: `sort()`, `argsort()`, multi-key sorting with `lexsort()`, field-based structured sorting.
- **Top-K & Quick Selection**: `np.partition()`, `np.argpartition()`.
- **Set Operations**: `unique()`, `intersect1d()`, `union1d()`, `setdiff1d()`, `isin()`.
- **Statistical Operations**: `percentile`, `quantile`, `histogram`, `bincount`, `digitize`, `cumsum`, `gradient`.
- **Linear Algebra (`np.linalg`)**: Matrix multiplication, determinants, inverses, eigenvalues/eigenvectors, linear system solvers (`np.linalg.solve`).
- **Polynomial & Signal Fitting**: Curve fitting with `np.polyfit()` & `np.polyval()`, convolutions with `np.convolve()`.
- **Real Mini-Project**: Full sales analysis pipeline with data cleaning, filtering, and metric calculation.

---

## ⚡ Requirements & Quick Start

### 1. Prerequisites
Ensure you have Python 3.8+ installed.

### 2. Clone the Repository
```bash
git clone https://github.com/preetamvr1595/numpy-mastery.git
cd numpy-mastery
```

### 3. Install Dependencies
```bash
pip install numpy jupyter matplotlib
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```
Or open the `.ipynb` files directly in **VS Code** with the Python & Jupyter extensions.

---

## 💡 Why Learn NumPy?

NumPy is the foundational building block of the entire Python Scientific and Data Science stack:
- **Pandas**: Series and DataFrames are built directly on top of NumPy ndarrays.
- **Scikit-Learn**: Machine learning algorithms operate on NumPy matrices.
- **PyTorch & TensorFlow**: Tensor data structures share memory layouts and syntax patterns with NumPy.
- **SciPy & OpenCV**: Image processing and scientific computing rely on vectorized NumPy arrays.

Mastering NumPy enables you to write clean, vectorized code that runs **10x–100x faster** than standard Python loops by leveraging compiled C-C++ implementations.

---

## 👨‍💻 Author & Connect

**Preetham V R**  
*MCA Student | Data Science & Machine Learning Educator*

- 🌐 GitHub: [@preetamvr1595](https://github.com/preetamvr1595)
- 💡 Project Link: [https://github.com/preetamvr1595/numpy-mastery](https://github.com/preetamvr1595/numpy-mastery)

---

## 📄 License

This repository is licensed under the [MIT License](LICENSE) — free to use, share, and adapt for learning or teaching.

---

⭐ **If you find this tutorial helpful, please star the repository on GitHub!**

