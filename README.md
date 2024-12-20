# Functional analysis within latent states: A novel framework for analysing functional time series data

Code repository accompanying the manuscript "Functional analysis within latent states: A novel framework for analysing functional time series data" by Owen Forbes, Edgar Santos-Fernandez, Paul Pao-Yen Wu, and Kerrie Mengersen.

## Description

This repository contains R code implementing a novel framework for analysing functional time series data using functional hidden Markov models (FHMM) and functional principal components analysis (FPCA). The code demonstrates the application of this framework to EEG data, specifically analysing power spectra during eyes-closed resting state recordings.

The analysis pipeline includes:
- Preprocessing of EEG spectral data using FOOOF (Fitting Oscillations & One Over F)
- Application of functional hidden Markov models to identify latent states
- Functional principal components analysis within identified states
- Statistical analysis relating latent states and functional principal components to behavioural and demographic variables

## Required Software and Packages

### R Packages

The following R packages are required for running the analyses:

Part 1 requirements:
- rmatio (v0.19.0): For importing .mat files containing EEG data
- ForeCA (v0.2.7): For spectral entropy calculations
- tidyverse (v2.0.0): For data manipulation and visualization
- fdapace (v0.6.0): For functional data analysis
- hmmhdd (v1.0): For functional hidden Markov models
  - Requires dependencies: gmfd (v1.0.1) and roahd (v1.4.3)
- reticulate (v1.36.1): For FOOOF integration

Part 2 requirements:
- tidyverse (v2.0.0): For data manipulation and visualization
- ggplot2 (v3.5.1): For plotting
- fda (v6.2.0): For functional data analysis
- viridis (v0.6.5): For color palettes
- ggvenn (v0.1.10): For Venn diagrams
- gtsummary (v2.0.4): For summary tables
- gt (v0.11.1): For table formatting
- brms (v2.22.0): For Bayesian regression models
- modelsummary (v2.2.0): For model summaries

### Python Requirements

FOOOF (v1.0.0) and matplotlib are required for spectral parameterisation. These can be installed in a conda environment named "FOOOF_env".

## Code Files

The analysis is split into two main R markdown files:

1. `flawless_code_public_part1.Rmd`: 
   - Data preprocessing
   - FOOOF analysis of power spectra
   - Implementation of functional hidden Markov models
   - Cross-validation through subset analysis

2. `flawless_code_public_part2.Rmd`:
   - Functional principal components analysis within states
   - Statistical analysis of relationships with behavioural measures
   - Generation of figures and tables
   - Results visualization

## License

MIT License

Copyright (c) 2023 Owen Forbes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
