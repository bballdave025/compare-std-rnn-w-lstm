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
# RCN Part 3 --- Implementation Roadmap

## Manual RNN

Implement:

- Embedding
- Hidden state update
- Output layer

Track tensor shapes throughout.

## Manual LSTM

Implement manually:

- Forget gate
- Input gate
- Candidate state
- Cell update
- Output gate
- Hidden state

Use ordinary tensor operations.

Use PyTorch autograd for training.

## Amazon Q Prompts

- Explain every tensor.
- Show tensor dimensions.
- Rewrite explicitly.
- Do not use nn.LSTM.
- Help me implement the gates manually.
- Visualize hidden and cell states.
- Simplify if too abstract.

## Too Simple?

If I cannot explain every gate, simplify.

## Too Complex?

If Q introduces transformers, CUDA, custom autograd, or graph internals,
reject and restate scope.
