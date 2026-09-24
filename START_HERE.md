# Start here

This is a notebook-first continuation of Dave's RNN/LSTM comparison. The initial notebook contains local inventory and an optional dataset preview. No cleaned data or trained model is claimed.

## Set up

From the repository directory, on Linux or macOS:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

On Windows, activate with `.venv\Scripts\activate` instead of `source .venv/bin/activate`.

Open `notebooks/01_rnn_lstm_comparison.ipynb` and run the environment and local inventory cells. These do not fetch data. The remote preview starts with `RUN_REMOTE_PREVIEW = False`; set it to `True` when ready to inspect five records from the dataset host. It does not create the final sample.

## Decide before making the dataset

1. The binary rating mapping, including 3-star reviews.
2. Category selection and approximate quotas.
3. Sampling within categories, a random seed, and exact dataset revision.
4. Duplicate and missing-text rules and train/validation/test splits.

The working defaults are about 10,000 reviews and binary classification. The first 10,000 records in stream order are not a random sample. Keep datasets in `data/raw/` or `data/processed/`; their contents are ignored by Git.

Record what actually ran, its output, decisions, and the next small action in `docs/LAB_NOTEBOOK.md`. Build the explicit RNN and LSTM in the main notebook with shapes beside each operation. Move code into `src/std_rnn_vs_lstm_write_not_design/` only if the notebook becomes unwieldy.

The MIT license is a proposed default and can be changed before publication. It does not license Amazon review data.
