# NBA Back-to-Back Fatigue Analysis (2025-26 Season)

CS439 Data Science — Final Project, Spring 2026

**Abhishek Sancheti & Aravind Saravu**

## Overview

This project analyzes the impact of back-to-back scheduling on NBA player and team performance during the 2025-26 regular season. Using play-by-play event data and the official league schedule, we identify which teams and players were most adversely affected by schedule fatigue.

## Repository Structure

```
├── data/               # Datasets (see data/README.md for sources)
├── notebooks/          # Analysis and modeling notebooks
├── paper/              # LaTeX source for the final paper
└── README.md
```

## Approach

1. **Data pipeline** — Join PBP game stats with schedule to flag back-to-back games
2. **Feature engineering** — Per-player per-game metrics (FG%, shot volume, turnovers, fouls)
3. **EDA** — Compare performance on B2B vs. rested games; identify most-affected players/teams
4. **Clustering (K-Means)** — Group players by fatigue response pattern
5. **Supervised model (XGBoost)** — Predict performance drop from schedule context

## Data

See [data/README.md](data/README.md) for dataset sources and schema.

## Requirements

```
pandas
numpy
scikit-learn
xgboost
matplotlib
seaborn
jupyter
```
