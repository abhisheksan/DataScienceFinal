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

See [data/README.md](data/README.md) for dataset sources, download links, and schema.

## Requirements

```
pandas
numpy
scipy
scikit-learn
xgboost
matplotlib
seaborn
jupyter
ipykernel
```

Install all at once:

```bash
pip install pandas numpy scipy scikit-learn xgboost matplotlib seaborn jupyter ipykernel
```

> **Apple Silicon note:** XGBoost requires OpenMP. If you hit an import error, run `brew install libomp`.

## How to Reproduce

1. Clone the repo: `git clone https://github.com/abhisheksan/DataScienceFinal`
2. Download `pbp2026.csv` from [Kaggle](https://www.kaggle.com/datasets/szymonjwiak/nba-play-by-play-data-1997-2023) and place it in `data/`
3. Install requirements (see above)
4. Open and run `notebooks/analysis.ipynb` top to bottom (Kernel → Restart & Run All)

The notebook writes two figures to `paper/figures/` automatically. All other data files are already in the repo.
