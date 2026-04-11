# Music Recommender

This project explores a personality-to-music recommender using the Young People Survey dataset. The current notebook focuses on a baseline model that predicts genre preferences from Big Five personality proxy features.

## Current Progress

- Loaded and validated the survey dataset from `dataset/responses.csv`.
- Identified the available music preference columns and checked basic data quality.
- Built Big Five proxy features from related survey questions.
- Trained baseline multi-output regressors:
	- `RandomForestRegressor`
	- `RidgeCV`
- Evaluated the models with MAE and RMSE.
- Kept mood and Spotify integration separate for the next phase.

## What We Still Need To Do

- Improve feature engineering for the Big Five proxies.
- Compare the baseline against stronger models and cross-validation.
- Add top-K genre recommendation logic from predicted preference scores.
- Integrate Spotify recommendations.
- Map mood to Spotify audio features such as `target_valence`, `energy`, and `tempo`.
- Add fallback behavior when the profile is sparse or model confidence is low.

## Dataset

- Young People Survey

## Baseline Model

- `MultiOutputRegressor` as the current baseline wrapper
- `RandomForestRegressor` and `RidgeCV` as the main regressors tested so far
