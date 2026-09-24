<!--
RECONSTRUCTION NOTICE
Source: jupy_log_wjupy_lab_3_build_your_own_2__timeline.pdf, with
jupy_log_wjupy_lab_3_build_your_own_1__timeline.pdf used as a cross-check.

This file was reconstructed from rendered `%load` output preserved in the
timeline PDFs. Text that was clearly visible has been restored as written,
apart from ordinary Markdown whitespace/list normalization.

Any content whose placement or wording had to be inferred is explicitly
marked with "RECONSTRUCTION UNCERTAINTY".
-->
# RCN Part 1 --- Philosophy, Constraints, and Project Charter

## Philosophy

> Write the LSTM. Don't design the LSTM.

This project is about understanding sequence models while staying within
the assignment scope.

## Guiding Principles

- Reduce decisions before coding.
- Understand every tensor.
- Use AI to accelerate implementation, not replace understanding.
- Finish before optimizing.

## Constraints

- Time budget: a few focused sessions.
- Dataset: manageable subset of Amazon Reviews 2023.
- Framework: PyTorch.
- Training: use autograd and optimizers.
- Do not implement custom autograd.

## Definition of Done

- Manual RNN cell.
- Manual LSTM cell.
- Three EDA visualizations.
- Clear comparison.
- Polished notebook export.

## Decisions Already Made

- RNN vs. LSTM comparison.
- Manual gate implementation.
- No transformers.
- No attention.
- No architecture redesign.

## Project Charter

Research goal: Understand how hidden state and cell state affect
sentiment classification while satisfying the course rubric.
