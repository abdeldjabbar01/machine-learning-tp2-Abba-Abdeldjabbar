# ML TP2 – Standardized PCA

Implementation of standardized PCA from scratch (NumPy/Pandas), compared with Scikit-learn's `PCA`.

- **Data:** grades of 6 students in 4 subjects (Mathematics, Statistics, Programming, Algorithms)
- **Notebook:** `TP-02-ABBA-Abdeldjabbar.ipynb` (run cells in order)

---

## Part A – PCA from Scratch

| Step | Description |
|------|-------------|
| 01 | Load dataset into DataFrame |
| 02 | Dimensions & descriptive statistics |
| 03 | Standardization (z-score) |
| 04 | Correlation matrix |
| 05 | Eigenvalues/eigenvectors of covariance matrix |
| 06 | Sort eigenvalues & reorder eigenvectors |
| 07 | Select top 2 eigenvectors (PC1, PC2) |
| 08 | Project standardized data onto PC1, PC2 |
| 09 | Explained variance ratio & cumulative |

**Result (Part A):** PC1 ≈ 93.5%, PC2 ≈ 6.0% → **99.5% variance retained** with 2 components.

---

## Part B – Analysis & Visualization

| Step | Description |
|------|-------------|
| 10 | Scatter plot: students in PC1–PC2 space |
| 11 | Feature loadings (variable contributions) |
| 12 | Reconstruction from 2 PCs (inverse transform) |
| 13 | Reconstruction error (Frobenius norm) |
| 14 | Scree plot (eigenvalues) |
| 15 | Verify with `sklearn.decomposition.PCA` |
| 16 | Correlation circle (loadings on unit circle) |
| 17 | Compare manual vs sklearn — explain sign differences |
| 18 | Summary & interpretation |

---

## Key Findings

- **PC1 (Learning Level):** Overall academic mastery — all subjects load positively
- **PC2 (Learning Profile):** Theoretical (Math/Algorithms) vs Applied (Statistics/Programming)
- **2D representation** captures 99.5% of variance with low reconstruction error
- **Manual PCA = sklearn** (up to arbitrary sign flips — subspace identical)

---

## Requirements

- Python 3
- `numpy`, `pandas`, `scikit-learn`, `matplotlib`

```bash
pip install numpy pandas scikit-learn matplotlib