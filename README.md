# Subcellular model building and calibration

We develop tools for data-driven building of subcellular biochemical signaling pathway models. This includes interoperable modules for: model building, calibration (parameter estimation) and model analysis. All information needed to perform these tasks are stored in a structured, human- and machine-readable file format based on SBtab (Lubitz et al. 2016). The information contained in the SBtab files includes: models, experimental calibration data and prior assumptions on parameter distributions. The toolset enables simulations of the same model in simulators with different characteristics, e.g. STEPS, NEURON, MATLAB’s Simbiology and R via automatic code generation. The parameter estimation is done by optimization or Bayesian approaches. Model analysis includes global sensitivity analysis and functionality for analyzing thermodynamic constraints and conserved moieties.

The documentation for the SBtab format are here: https://github.com/tlubitz/SBtab

The documentation of each respective module (tool) from our group can be found in the READ ME file of that repository, i.e.:
- Uncertainty Quantification and Global Sensistivity Analyses (UQSA) https://github.com/icpm-kth/uqsa
- etc

[1] Lubitz, T., Hahn, J., Bergmann, F.T., Noor, E.,. Klipp, E, Liebermeister, W. (2016). SBtab: A flexible table format for data exchange in systems biology. Bioinformatics, 15;32(16), 2559-61

<p>
![Organizational Flowchart](ToolsetFlowchart-fix.svg)
<div align="justify" width="80%" style="font-size: 90%"> This is a
high level flowchart of common tasks in systems biology (and modelling
in neuroscience). We require a storage format that is robust enough to
survive being moved to other platforms and must be easy to parse by
common tools, on various platforms and in many programming
languages. The SBtab format can be read using such tools as `awk` and
`sed` but is also easy to represent as a _data frame_ in *R* or an
array of structs (matlab and GNU Octave have _structarrays_). We need
to easily communicate with other groups and send them models and
data. Another important task is simulation and parameter
estimation. Both of these tasks require the translation of the
biological model into a computational model (right hand side vector
field of an ordinary differential equation or propensities for a
stochastic algorithm such as the Gillespie Algorithm). Calibration and
Analysis includes copmmon tasks such as *parameter estimation*,
*global sensitivity analysis*, *prediction*; we are working on methods
and implementations for these tasks.
</div> </p>

