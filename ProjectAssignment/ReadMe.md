# Read Me

## Version and Packages 
- Python 3.12
- pandas 3.1.0, numpy 2.5.4, scikit-learn 1.9.1

## Data
Download each dataset and save it in the same folder as `run.py`, using these filenames:
(datasets are )

| Dataset | Source | Saved as               |
|---|---|------------------------|
| PhiUSIIL Phishing URL Dataset | https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset (paper: https://doi.org/10.1016/j.cose.2023.103545) | `PhiUSIIL_result.csv`  |
| UCI Phishing Websites Dataset | https://doi.org/10.24432/C51W2X | `[UCILL_result.csv]`   |
| Phishing Dataset for Machine Learning Feature Evaluation (Mendeley) | https://data.mendeley.com/datasets/h3cgnj8hft/1 | `Mendeley_dataset.csv` |


## Seed
4371 (used for the splits and the random forest).

## Run
Primary (baseline) dataset: PhiUSIIL.

```bash
python run.py PhiUSIIL
python check.py --split split_PhiUSIIL.csv --scores scores_PhiUSIIL.csv --threshold <value>
```

`run.py` prints the exact `--threshold` value at the end of the run.
`python run.py` with no argument also trains on the UCI and Mendeley datasets and writes the matching files
`split_<dataset>.csv` and `scores_<dataset>.csv`.

## Outputs 
`split_PhiUSIIL.csv`, `scores_PhiUSIIL.csv` [and the UCI and Mendeley pairs, if run]