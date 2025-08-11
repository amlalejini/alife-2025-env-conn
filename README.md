# Environmental connectivity influences long-term evolutionary outcomes

[![DOI](https://zenodo.org/badge/1036101318.svg)](https://doi.org/10.5281/zenodo.16795777)
[![OSF](https://img.shields.io/badge/data%20%40%20OSF-10.17605%2FOSF.IO%2FAHS6M-blue)](https://osf.io/ahs6m/)

This repository is associated with our 2025 Artificial Life Conference paper, "Environmental connectivity influences long-term evolutionary outcomes".

## Overview

### Abstract

> Evolutionary graph theory uses mathematical representations of networks to model population spatial structure, providing a tractable framework to study how environmental connectivity influences evolution.
  However, evolutionary graph theory often uses simple genetic representations with limited fitness landscapes and focus on short-term evolutionary outcomes, such as the probability of fixation and average fixation time for new mutations.
  In this work, we bridge evolutionary graph theory and artificial life approaches to investigate how different patterns of connectivity affect long-term evolutionary adaptation.
  To do so, we developed an extended evolutionary graph theory platform that supports fully configurable, large fitness landscapes, and we compared evolutionary adaptation on different spatial structures across three fitness landscapes crafted to isolate different aspects of evolution.
  We found that, in general, more constrained spatial structures slow evolutionary adaptation on smooth fitness gradients but can facilitate improved fitness landscape exploration and valley crossing.
  Next, we compared the evolution of complex adaptive traits in populations of self-replicating computer programs (digital organisms) evolving on different spatial structures.
  In populations of digital organisms, we found variation in the number of complex traits and reproductive strategies evolved across different patterns of connectivity.
  For example, some structures favored organisms with smaller genomes capable of faster self-replication, while others favored more complex organisms.
  More broadly, this work demonstrates a path forward for extending evolutionary graph theory to study long-term evolutionary outcomes and poses critical considerations for how we study the effects of spatial structure in artificial life systems.

## Repository guide

- `bookdown/` - contains configuration for bookdown build of supplemental material
- `docs/` - contains supplemental documentation of our methods, including data availability, guides for compiling experiment software, etc.
- `experiments/` - contains HPC job submission scripts, configuration files, and data analyses for experiments
- `hpc-env/` - contains SLURM environments (e.g., loaded software modules) for HPC systems used to conduct experiments
- `local/` - contains files specific to local setup on authors' machines
- `scripts/` - contains Python scripts used to run experiments, perform some analyses, etc.
- `third-party/` - contains dependencies as git submodules
- `web-supplement/` - contains the compiled web-based supplement
- `requirements.txt` - contains Python dependencies