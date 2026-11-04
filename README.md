# Learning to Predict Cybersickness in 3D Games from Gameplay Video

*ITE351 AI & Applications, Hanyang University, Fall 2026. Group G14 project blog.*

## Task 1: Group Members

| Name | Organization | Email |
|---|---|---|
| Hyeonmin Choi | Department of Information Systems, Hanyang University | daniel794@hanyang.ac.kr |
| Togtokhbayar Bilegt | Department of Data Science, Hanyang University | TBD |

## Task 3: Research Idea

**Title:** Learning to Predict Cybersickness in 3D Games from Gameplay Video

**Proposal (Option B):**
Many players feel dizzy or nauseous in first-person 3D games, but they cannot tell in advance which scenes will cause it. Our prototype, a Windows window recorder, already extracts per-frame visual features with OpenCV optical flow: camera translation, rotation, shake, brightness change, and input/screen lag. It currently combines them into a risk score with hand-tuned weights. We will replace these weights with a learned model. Participants will play short 3D game sessions while we record the screen and their input timing, and they will rate discomfort on a 0–10 scale at fixed intervals. Each 10-second window becomes one sample with aggregated motion features and a discomfort label. We will train logistic regression, random forest, and gradient boosting with scikit-learn, plus a small GRU over feature sequences, and compare them with the rule-based baseline using MAE and F1 for high-risk windows. Train and test sets will be split by participant to avoid leakage. The best model will drive a comfort filter that adjusts screen colors when risk rises. This is not a medical diagnosis tool.

## Starting Point

| Component | What it does now |
|---|---|
| Window recorder | Records a selected game window to MP4 and logs input timing |
| Video analyzer | Optical-flow features per frame and a hand-tuned risk score (baseline) |
| Comfort filter | Overlay that adjusts screen brightness and color in real time |

## Plan

1. Collect recordings and discomfort ratings, and export features to CSV.
2. Explore the data: feature distributions, correlations, class balance.
3. Train and compare models against the rule-based baseline.
4. Connect the best model to the comfort filter and report results and limits.

## Progress Log

- **2026-11-04**: Group registered (G14), blog created, research idea proposed.
