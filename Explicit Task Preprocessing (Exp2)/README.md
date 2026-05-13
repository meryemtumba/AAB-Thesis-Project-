# Explicit Task Preprocessing (Experiment 2)

This folder contains the preprocessing pipeline for Explicit Task (Exp2) and the preprocessing was implemented in Python.

## Files in This Folder

* `Behavioral/Eye-Tracking Preprocessing.ipynb`: Main preprocessing script for Experiment 1.  
The script loads the partially preprocessed behavioural and eye-tracking data, merges participant sessions, cleans RT and TFF measures, constructs analysis variables, and generates the final datasets used for statistical analyses.

* `Explicit_Task_Data_Experiment2.rtf`: Original preprocessing instructions and data description document provided by Aitana Grasso-Cladera.

# Input Data

The preprocessing pipeline combines several behavioural and eye-tracking files.

Typical input files include:

```text id="3yplwz"
reactionTime.csv
timeFirstFixation.csv
actualReaction.csv
frameColor.csv
frameSide.csv
valence.csv
blockOrder.csv
subjectsToRemove.csv
````

# Preprocessing Workflow

The preprocessing pipeline includes the following steps:

## 1. Participant Exclusion

Participants were excluded based on predefined quality criteria, including:

* missing or incomplete sessions,
* excessive invalid trials,
* participants listed in `subjectsToRemove.csv`.

## 2. Session Merging

Participants completed two experimental sessions.

The preprocessing script:

* loads both sessions,
* merges them into a single participant-level dataset,
* preserves trial order across sessions.

Participants completed 176 trials in total across both sessions.

## 3. Behavioural Data Cleaning

Reaction time (RT) preprocessing included:

* removal of RT < 150 ms,
* exclusion of incorrect responses,
* RT winsorising ±2 SD,
* conversion of invalid trials to missing values (`NaN`).

Correct responses were determined by comparing:

* instructed joystick movement (`frameColor`)
* actual response (`actualReaction`)

### Response Coding

| Frame Colour | Required Action |
| ------------ | --------------- |
| Blue         | Pull            |
| Orange       | Push            |

## 4. Eye-Tracking Data Cleaning

Time to First Fixation (TFF) preprocessing included:

* removal of TFF values < 100 ms,
* trimming of extreme values using ±2 SD filtering,
* marking invalid trials as missing.

## 5. Variable Construction

The preprocessing pipeline generates several derived variables used in later analyses.

### Main Variables

| Variable    | Description                    |
| ----------- | ------------------------------ |
| `RT_ms`     | Reaction time in milliseconds  |
| `logRT`     | Log10-transformed RT           |
| `TFF_ms`    | Time to First Fixation         |
| `TFF_c`     | Within-participant centred TFF |
| `trial_z`   | Standardised trial order       |
| `condition` | Congruent vs incongruent       |
| `valence`   | Positive vs negative           |
| `side`      | Left vs right stimulus side    |

## 6. Effect Coding

Categorical variables were effect coded for mixed-effects modelling.

| Variable  | Coding                           
| --------- | -------------------------------- |
| Valence   | Negative = -1, Positive = +1     |
| Side      | Left = -1, Right = +1            |
| Condition | Incongruent = -1, Congruent = +1 |


# How to Run

1. Place the raw experimental files into the appropriate directories.
2. Update file paths in the preprocessing scripts if necessary. 

# Note

The repository does not contain raw experimental data due to ethical and privacy restrictions.
