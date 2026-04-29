# Scalar–Tensor Cosmology with Time-Scaling Modification

This repository contains the code used in the analysis presented in:

**"Scalar–Tensor Cosmology with Time-Scaling Modification: Observational Constraints from H(z) and Pantheon+"**  
Josip Zenčić (2026)

---

## 🔬 Overview

This project explores a minimal extension of ΛCDM cosmology based on a time-scaling modification motivated by scalar-field dynamics.

The model introduces a redshift-dependent factor:

T(z) = 1 + C * z / (1 + z)

which modifies the expansion rate:

H(z) = H_LCDM(z) * T(z)

The goal is to test whether such a minimal dynamical correction can improve agreement with observational data.

---

## 📊 Data Used

The analysis includes:

- **Cosmic chronometer H(z) data**
- **Pantheon+ Type Ia supernova sample (N = 1701)**
- Full covariance matrix for supernova data

Data sources:
- Pantheon+: https://github.com/PantheonPlusSH0ES/DataRelease

---

## ⚙️ Methodology

- Joint χ² minimization:
  
  χ² = χ²_H(z) + χ²_SN

- Parameters fitted:
  - H₀ (Hubble constant)
  - C (time-scaling parameter)
  - M (supernova magnitude offset)

- Optimization:
  - SciPy `minimize` (Nelder-Mead)

---

## 📈 Key Results

- ΛCDM:
  - χ² ≈ 1778.14

- Minimal model:
  - χ² ≈ 1765.47

- Improvement:
  - Δχ² ≈ -12.67
  - ΔAIC ≈ -10.67

➡️ The minimal model is statistically preferred over ΛCDM under current data.

---

## 📌 Interpretation

- The improvement is driven primarily by the supernova dataset.
- The model remains consistent with H(z) constraints.
- Best-fit value:
  
  C ≈ 0.12

This suggests a stronger effective modification of the expansion rate at higher redshift.

---

## 🌌 Effective Cosmology

From the reconstructed expansion history:

- w₀ ≈ -0.88  
- Transition redshift: z ≈ 0.55  

These values are consistent with a late-time accelerating universe.

---

## 🧪 Stability

The solution is highly stable across different initial conditions:

σ_C ~ 10⁻⁶

This indicates a well-defined global minimum.

---

## ⚠️ Limitations

- No MCMC or posterior analysis yet
- No BAO or CMB constraints included
- Phenomenological parametrization

Results should be considered **preliminary**.

---

## ▶️ How to Run

Install dependencies:

```bash
pip install numpy pandas scipy matplotlib




Run:

python psi_time_model_fit_v2.py
📁 Files
psi_time_model_fit_v2.py – main analysis script
📜 License

This project is provided for research and educational purposes.

🔗 Related Work

Zenodo record:

👉 https://zenodo.org/records/19672877

👤 Author

Josip Zenčić
Makarska, Croatia

💡 Note

This work represents an ongoing research direction.
Further validation with additional datasets (BAO, CMB) and full statistical analysis is planned.
