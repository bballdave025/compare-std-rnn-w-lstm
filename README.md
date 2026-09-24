# Standard RNN vs. LSTM: write, do not design

A notebook-first PyTorch comparison of a manually written vanilla RNN and a manually written LSTM on a manageable sample of [Amazon Reviews 2023](https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023).

**Main goal:** understand every embedding, recurrent-state update, LSTM gate, and tensor shape by writing the recurrent cells explicitly. PyTorch autograd and optimizers can handle differentiation and training.

**Secondary goal:** use star ratings as a supervised proxy for evaluative polarity, compare the two models overall and across review lengths, and discuss where they disagree. A star rating is not identical to linguistic sentiment.

The working plan is approximately 10,000 reviews and binary classification. The precise label mapping, category allocation, and sampling strategy remain decisions to settle after inspecting real data. Five-class rating prediction remains a possible later extension. Both models should use the same splits and comparable preprocessing.

Start with [START_HERE.md](START_HERE.md), then open [the notebook](notebooks/01_rnn_lstm_comparison.ipynb).

## Scope

- Explicit vanilla RNN hidden-state update and LSTM forget, input, candidate, and output gates.
- Explain tensor shapes and recurrent-state changes alongside the code.
- EDA: missingness, duplicates, review length, vocabulary, rating balance, and length-versus-label plots.
- Reproducible train/validation/test splits and evaluation by review length.
- No `nn.RNN`, `nn.LSTM`, transformers, attention, custom autograd, or architecture redesign for the central models.

## Provenance and status

The reconstructed planning documents in `docs/source-reconstruction/` derive from the August 2026 Jupyter timeline. The earlier one-category streaming snippet was a proposed acquisition route, not evidence of a completed 10K sample. No cleaned dataset, trained model, or result is claimed by this starter repository.

Dataset credit: McAuley Lab, *Amazon Reviews 2023*. The dataset is obtained separately under its own terms; this repository's code license does not license review content.
