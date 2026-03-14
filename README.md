# In Vivo Electrophysiology Analysis Pipelines

> **Context:** The code in this repository was developed as part of my Ph.D. thesis in Neuroscience at Université de Rouen Normandie (France). It contains custom analytical pipelines used to investigate post-stroke cortical plasticity and network reorganization following Vagus Nerve Stimulation (VNS). 
> 
> *Note: This repository serves as a methodological portfolio. To protect intellectual property prior to publication, the raw datasets (`.dat`, `.mat`, `.nix`) have been omitted.*

## Overview

This repository is divided into two main analytical pipelines, covering both macro-scale network dynamics (LFP) and micro-scale single-unit activity (Spikes).

### 1. [Superlet_Burst_Detection](./Superlet-Burst-Detection)
A custom Python pipeline designed to detect and analyze high-frequency oscillatory bursts in Local Field Potentials (LFP). It leverages the **Superlet transform** to achieve high-resolution time-frequency representations, overcoming the limitations of standard Morlet wavelets.

* **Key Features:**
    * Time-frequency analysis using Superlets.
    * Custom modification of existing burst detection algorithms to fit specific experimental constraints.
    * Advanced statistical modeling of burst features using Generalized Estimating Equations (GEE) via `statsmodels`.

### 2. [SpikeInterface_Pipeline](./SpikeInterface-Pipeline)
A comprehensive, production-ready Jupyter Notebook pipeline for *in vivo* spike sorting and post-processing, utilizing the **SpikeInterface** framework. 

* **Key Features:**
    * Automated preprocessing (filtering, referencing, stimulation artifact removal via chunking).
    * Integration with state-of-the-art sorters (e.g., Kilosort 4).
    * Waveform extraction, quality metrics computation, and semi-automated curation preparation for SpikeInterface GUI or Phy.

### Pipeline Visualizations

<p align="center">
  <img src="SpikeInterface-Pipeline/Exports_examples/SpikeInterface GUI.jpeg" alt="SpikeInterface GUI" width="700">
</p>

<p align="center">
  <img src="SpikeInterface-Pipeline/Exports_examples/Multi-unit template metrics display.jpg" alt="Template Metrics" width="700">
</p>

<p align="center">
  <img src="SpikeInterface-Pipeline/Exports_examples/Rasterplot of curated good units.png" alt="Rasterplot" width="700">
</p>