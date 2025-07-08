README — gamma_gain.hoc
========================================
Purpose
-------
Reproduces the calibration used in Supplementary Table S55 (main manuscript).
The script sweeps AMPA conductance on a passive CA1‑like soma and reports
the resulting peak EPSP amplitude, establishing the scaling factor
(~0.032 mV per % dendritic gain) cited in the paper.

How to run
----------
1. Install NEURON 8.x (www.neuron.yale.edu).
2. Copy `gamma_gain.hoc` into your working directory.
3. Launch with:

       nrngui gamma_gain.hoc

   or, from Python:

       import neuron
       h = neuron.h
       h.load_file('gamma_gain.hoc')

Outputs
-------
* Console printout of two vectors:
    - Synaptic weights (µS)
    - Corresponding EPSP amplitudes (mV)
* An XY plot (amplitude vs. weight) for immediate inspection.

Expected outcome
----------------
Linear regression of amplitude (mV) vs. % change in conductance
yields a slope ≈ 0.032 mV per % — the value used in Table S55 to map
a –35 % reduction in γ‑burst to a +1 mV expansion of V_margin.

Contact
-------
Questions: <rosapatryk55@gmail.com>
Licence:   CC‑BY 4.0
