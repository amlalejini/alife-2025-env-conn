# Compilation instructions

Instructions for compiling and running the software used in this study on your local machine.
All experiments were run on Mac or Linux-based operating systems.

You will need a C++ compiler that supports at least C++17.
We used g++13 for all local compilations.

You will also need Python to run graph generation and analysis.
Python dependencies are listed in the `requirements.txt` at the root of this repository.

Statistical analyses and data visualizations were conducted using R.

Experiments in our simplified model used the MABE2 software, and experiments with digital organisms (self-replicating computer programs) used a modified version of the Avida software platform.

## Instructions

First, clone the `alife-2025-env-conn` repository (<https://github.com/amlalejini/alife-2025-env-conn.git>) to your machine.
Then, initialize and update git submodule inside the repository.
From inside the repository on your machine, run:

```
git submodule update --init --recursive
```

This will download and update the following dependencies:

- `avida-empirical` (commit hash: `266f95f8fcb452655330dab55caa9f1408b49ffa`): A modified implementation of the Avida software that supports the capacity to configure environmental connectivity.
- `evo_spatial_discoveries` (commit hash: `2c384e93df231125bae83fc6c38d8dc8c64eb6ee`): Contains configurations for MABE2 experiments.
- `MABE2` (commit hash: `4f8eb86f997ee89f6d0e0b1144c5be162f4d8d1b`): MABE = "Modular agent-based evolver", which is a software platform deigned to empower developers to easily build and customize software for evolutionary computation or artificial life. We used this platform to implement our non-avida experiments.
- `network_correlation` (commit hash: `9d9a07f7436c3569d10eb3b03c6b30e1238c74ef`): Third-party python implementations of various graph statistics and analyses.

To compile Avida, navigate into the `third-party/avida-empirical/` directory and run `./build_avida/`.
The compiled executable will be created in the `third-party/avida-empirical/cbuild/work/` directory.

To compile MABE2, navigate into the `third-party/MABE2/build` directory and run `make native`.
The compiled executable will be created in the `third-party/MABE2/build` directory.

Configuration files used Avida experiments can be found in the `experiments/` directory (within the `hpc/config` subdirectory for any given experiment).
Configuration files used for MABE2 experiments can be found in `third-party/evo_spatial_discoveries/experiments/`.

