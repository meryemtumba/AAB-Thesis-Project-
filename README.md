# AAB - Master Thesis Project

# Investigating the Temporal Relationship Between Fixation Timing and Reaction Time

## A Dual Picture Approach–Avoidance Task

This repository contains the preprocessing and statistical analysis code used for my Master’s thesis:

> **“Investigating the Temporal Relationship Between Fixation Timing and Reaction Time in the Approach–Avoidance Task”**

The project examines the relationship between early attentional orienting and behavioural responding in a Dual Picture Approach–Avoidance Task (AAT) using behavioural and eye-tracking measures. In particular, the thesis investigates whether earlier fixation onset, indexed by **Time to First Fixation (TFF)**, is associated with faster behavioural **reaction times (RTs)**.

The repository includes workflows for two experimental task variants:

- **Experiment 1 — Implicit Task**
- **Experiment 2 — Explicit Task**

---

# Repository Structure

The repository is organised into the following folders:

```text
├─ Analysis/
│  Contains scripts for statistical analyses and plotting.
│
├─ Explicit Preprocessing/
│  Contains preprocessing scripts and documentation
│  for Experiment 2 (Explicit Task).
│
├─ Implicit Preprocessing/
│  Contains preprocessing scripts and documentation
│  for Experiment 1 (Implicit Task).
│
├─ README.md
└─ .gitignore
````markdown

Each preprocessing folder contains:

* preprocessing scripts,
* workflow documentation,
* and a dedicated README explaining the corresponding pipeline.

---

# Requirements

This repository requires:

* Python (≥ 3.10)

Main packages used in the project:

```python
pandas
numpy
matplotlib
seaborn
statsmodels
scipy
```

Additional dependencies are listed at the beginning of each script.

---

# Acknowledgements

This thesis was conducted at the Neurobiopsychology Research Group, Institute of Cognitive Science, University of Osnabrück and all the data were provided by Aitana Grasso Cladera.


