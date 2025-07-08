# vCA1-margin-model

**Narrowing of the vCA1 excitability margin – stress, magnetite, CREB-high hot-spots and Schumann resonance as a common mechanism in SZ / MDD / PTSD**

[![License: CC-BY-4.0](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)](LICENSE)  
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

This repository provides the **minimal code and data needed to reproduce the calibration**  
“γ-burst ↓  ⇒  EPSP ↑ ≈ 0.032 mV per %” (Supplementary Table S55 in the manuscript).

---

## Contents

| File / folder           | Purpose                                                                    |
|-------------------------|----------------------------------------------------------------------------|
| `gamma_gain.hoc`        | **NEURON** script – sweeps AMPA conductance (0.1–3 µS) and records EPSP    |
| `README_gamma_gain.txt` | One-page CLI guide for running the script without the GUI                  |
| `LICENSE`               | Full text of the **Creative Commons Attribution 4.0** licence              |

---

## Requirements

* **NEURON ≥ 8.0** – <https://neuron.yale.edu>  
  `conda install -c conda-forge neuron` &nbsp;or&nbsp; `pip install neuron`
* Python ≥ 3.8 (only if you run the script head-less)
* Linux / macOS (Windows via WSL also works)

---

## Quick start

```bash
# with GUI
nrngui gamma_gain.hoc

# head-less (pure Python)
python - <<'PY'
import neuron
neuron.h.load_file('gamma_gain.hoc')
PY
