# Molecular-Dynamics Electrode-Charge Dataset



## Overview

This repository contains the molecular-dynamics electrode-charge time-series data used in the master's thesis

> **DATA-DRIVEN FORECASTING OF SUPERCAPACITOR CHARGING PROFILES WITH LSTM APPROACH**

The dataset consists of the electrode-charge trajectories obtained from molecular-dynamics simulations of electrochemical double-layer capacitors (EDLCs) with different pore sizes, solvent dipole moments, and applied potentials.

These trajectories were used for data preprocessing, LSTM training, recursive forecasting, and transmission-line-model (TLM) analysis presented in the thesis.



# Authors

The dataset obtained by Ayşe Hafsa Doğan, Yağız Efe Korkmaz, Assoc. Prof. Betül Uralcan Kılavuz.


---

# Repository Structure

```text
edlc-md-charge-data/
│
├── README.md
└── data/
    ├── PS620_DM091_1V.zip
    ├── PS620_DM207_1V.zip
    ├── ...
    └── PS1475_DM618_2V.zip
```

---

# Data Format

Each ZIP archive contains a single molecular-dynamics charge trajectory stored as a plain-text file.

Each extracted file contains three comma-separated columns:

```text
time_ns,positive_charge_e,negative_charge_e
```

where

- **time_ns** : simulation time in nanoseconds (ns)
- **positive_charge_e** : instantaneous total charge of the positive electrode in units of the elementary charge (e)
- **negative_charge_e** : instantaneous total charge of the negative electrode in units of the elementary charge (e)

---

# File Naming Convention

Each filename follows

```text
PS[pore size]_DM[dipole moment]_[voltage].zip
```

where

- **PS** : pore size (Å)
- **DM** : solvent dipole moment (D)
- **V** : applied potential difference (V)

For example,

```text
PS1475_DM288_2V.zip
```

corresponds to

- pore size = 14.75 Å
- solvent dipole moment = 2.88 D
- applied potential = 2 V




