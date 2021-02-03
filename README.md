# Structack: Structure-based adversarial attacks on GNNs



DeepRobust library [https://github.com/DSE-MSU/DeepRobust/] is needed for the scripts to run.
Please clone that repo, and run `python setup.py install`.
This library contains the datasets as well as the implementations of informed baseline approaches.

Additionally, `torch-scatter` is needed. Please see [https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html]


The script `structack/compare_to_baselines.py` evaluates the accuracy and running time of GCN on
* A clean graph when run with option `--approach_type clean`
* Perturbed graph with Structack with different combinations when run with option `--approach_type structack`
* Perturbed graph with baseline approaches when run with option `--approach_type baseline`

The script `structack/memory_test.py` evaluates the memory consumption of Structack and baselines.

The script `structack/calc_unnoticeability_baselines.py` evaluates the unnoticeability of Structack and baselines.

It stores results in a `.csv` file in path `reports/eval/`
