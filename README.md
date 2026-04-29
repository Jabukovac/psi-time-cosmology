# Scalar–Tensor Cosmology with Time-Scaling Modification

This repository contains the analysis code for:

**Scalar–Tensor Cosmology with Time-Scaling Modification: Observational Constraints from H(z) and Pantheon+**  
Josip Zenčić, 2026

## Overview

This project explores a minimal phenomenological extension of ΛCDM cosmology based on a redshift-dependent time-scaling modification motivated by scalar-field dynamics.

The model introduces:

```text
T(z) = 1 + C z / (1 + z)

which modifies the expansion rate:

H(z) = H_LCDM(z) · T(z)
Data Used

The analysis uses:

Cosmic chronometer H(z) measurements
Pantheon+ Type Ia supernova sample, N = 1701
Full Pantheon+ covariance matrix

Pantheon+ data source:
https://github.com/PantheonPlusSH0ES/DataRelease

Methodology

The model is tested through a joint chi-square fit:

χ² = χ²_H(z) + χ²_SN

Fitted parameters:

H₀ — Hubble constant
C — time-scaling parameter
M — supernova magnitude offset

Optimization is performed using scipy.optimize.minimize.

Key Results

ΛCDM:

χ² ≈ 1778.14
AIC ≈ 1782.14

Minimal Ψ/time model:

χ² ≈ 1765.47
AIC ≈ 1771.47

Improvement:

Δχ² ≈ -12.67
ΔAIC ≈ -10.67

The improvement is driven primarily by the Pantheon+ supernova sector, while the model remains comparable to ΛCDM for H(z) data.

Effective Cosmology

The reconstructed expansion history gives approximately:

w₀ ≈ -0.88
w(z=1) ≈ -0.60
q₀ ≈ -0.42
z(q=0) ≈ 0.55

These values are consistent with a late-time accelerating universe.

Stability

The best-fit solution was tested across multiple initial conditions and converges to a stable minimum:

C ≈ 0.12146
σ_C ~ 10⁻⁶
Limitations

This is a preliminary observational test. Current limitations include:

No MCMC or posterior analysis yet
No BAO or CMB constraints included
Phenomenological parametrization
Further validation required
How to Run

Install dependencies:

pip install numpy pandas scipy matplotlib

Run the analysis:

python code/psi_time_model_fit_v2.py
Repository Structure
psi-time-cosmology/
├── README.md
└── code/
    └── psi_time_model_fit_v2.py
Related Work

Zenodo record:
https://zenodo.org/records/19672877

Citation

If you use this code or results, please cite the Zenodo record above.

Author

Josip Zenčić
Makarska, Croatia

Note

This work is part of an ongoing research direction. Future versions should include BAO/CMB constraints, uncertainty estimates, and full posterior exploration.
