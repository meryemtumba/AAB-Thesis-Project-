# Statistical Analysis

This folder contains the statistical analysis and plotting scripts for the thesis project.  
All analyses were implemented in Python using behavioural and eye-tracking data generated from the preprocessing pipelines.

The analyses were conducted separately for:

- **Experiment 1 — Implicit Task**
- **Experiment 2 — Explicit Task**

The analysis scripts include the following steps:

## 1. Loading Preprocessed Data

The scripts load cleaned datasets generated during preprocessing.

Typical input files include:

```text id="34vzmt"
Exp1_RT_TFF_clean.csv
Exp2_RT_TFF_clean.csv
Exp1_ready_TFF.csv
Exp2_ready_TFF.csv
```
## 2. Descriptive Statistics

The scripts compute descriptive statistics for:

* reaction time (RT),
* time to first fixation (TFF),
* task conditions,
* participant-level summaries.

## 3. Linear Mixed Models

Linear mixed models (LMMs) were used to examine the relationship between attentional orienting and behavioural responding.

The main analyses included:

* within-participant models,
* task-adjusted models,
* time-on-task models,
* between-participant models.

All models included random intercepts for participants.

## 4. Variables Used in Analyses

### Main Variables

| Variable    | Description                     |
| ----------- | ------------------------------- |
| `logRT`     | Log10-transformed reaction time |
| `TFF_c`     | Within-participant centred TFF  |
| `trial_z`   | Standardised trial order        |
| `mean_TFF`  | Participant mean TFF            |
| `condition` | Congruent vs incongruent        |
| `valence`   | Positive vs negative            |
| `side`      | Left vs right stimulus side     |


## 5. Effect Coding

Categorical predictors were effect coded.

| Variable  | Coding                           |
| --------- | -------------------------------- |
| Valence   | Negative = -1, Positive = +1     |
| Side      | Left = -1, Right = +1            |
| Condition | Incongruent = -1, Congruent = +1 |

## 6. Plotting

The plotting scripts generate figures used in the thesis, including:

* RT distributions,
* TFF distributions,
* within-participant TFF–RT relationships,
* task effects,
* time-on-task effects,
* between-participant associations.

# How to Run

1. Ensure preprocessing has been completed.
2. Confirm that the paths to the cleaned datasets are correct.
3. Run the analysis scripts in Python.

# Note

The repository does not contain raw experimental data due to ethical and privacy restrictions.

