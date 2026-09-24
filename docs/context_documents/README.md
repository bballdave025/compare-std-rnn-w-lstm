# Context Documents

This directory contains **continuation-ready context documents** (Lab Notebook / LN files) for **compare-std-rnn-w-lstm**. The short project marker is `rnncmp`.

These are working checkpoints, not polished project documentation. They preserve decisions, architecture, constraints, what code actually ran, observed outputs, open questions, and the next executable step. In particular, distinguish a proposal in an old conversation from a cell that ran successfully.

## Purpose

Each document should answer:

> If I resumed this project in a fresh chat, on another machine, or months later, what would I need to know to write the next notebook cell?

Keep the established goal: **write the LSTM; do not design the LSTM**. The main implementation belongs in `notebooks/01_rnn_lstm_comparison.ipynb`, with explicit vanilla RNN updates and LSTM gates. PyTorch autograd and optimizers are allowed. Ratings are a supervised target, not necessarily a direct measure of linguistic sentiment.

## Documentation hierarchy

```text
../../README.md                 Project overview
../source-reconstruction/       Historical project charter and plans
LN_rnncmp_*.md                 Continuation-ready state snapshots
LAB_NOTEBOOK.md                Running record of actions and observations
../dev_notes/                  Focused implementation or experiment notes
```

The September 23 reconstructed context document is a starting snapshot. Its references to the August `jupy_log` timelines are retrieval anchors. As code and data are added, the actual repository and recorded execution results become the source for implementation status. The four `RCN_Part_*` files belong in `../source-reconstruction/` and retain their reconstruction notices.

`LAB_NOTEBOOK.md` may stay in this directory as the running log. Give a new `LN_rnncmp_*` document a self-contained current-state account when a fresh-chat handoff is needed. The log alone need not carry every fact needed for a restart.

## Context Document header template

Use double-brace placeholders (`{{...}}`). Fill the fields with current facts; do not copy a historical timestamp or completed-status claim forward unchanged.

```text
*BEGIN: Context Document Header*

# CONTEXT DOCUMENT — Continuation

## Project

**Name:**
RNN/LSTM Implementation — Bring-Your-Own Amazon Reviews Project

**Short marker:**
`rnncmp`

**Description:**
{{1–3 sentences describing the current project and intended result}}

---

## Continuation Metadata

**Prepared at:**
{{ssssssssss_YYYY-mm-ddTHH:MM:SS±ZZZZ}}

Generated in Boston time with:
`TZ=America/New_York date +'%s_%Y-%m-%dT%H:%M:%S%z'`

**Continued from chat:**
{{Exact chat title}}

**Also involving:**
- {{Relevant notebook, source timeline, or related topic}}
- {{Other relevant source, or omit this line}}

---

## Author / Source

**User (GitHub):**
@bballdave025

**User (ChatGPT):**
{{Optional}}

---

## Intent for This Context

{{1–2 sentences saying what the next session should be able to do}}

---

## Usage Instructions

- Treat this document as the authoritative reconstructed project state at its preparation time.
- Continue with minimal re-derivation.
- Separate decisions, observed execution, exploratory code, proposals, and unfinished work.
- Prefer newer verified repo contents and user corrections where they supersede this snapshot.

*ENDOF: Context Document Header*
```

After the header, include the current research question and target definition, data provenance and split status, notebook cells that ran and their outputs, model implementation status, active constraints, open questions, and **Immediate Next Steps**. Include paths, commands, small snippets, and timeline anchors when they save future reconstruction effort.

## Pre-Context-Document Prompt (PCDP) template

Send this short prompt before an LN document when starting a fresh chat. The historical `PCDP_rnncmp_2026-09-23_go-pers.md` is an example, not a substitute for updating the immediate focus.

```text
## Current Work

Project:
Manual vanilla RNN versus LSTM on Amazon Reviews 2023, in a notebook-first PyTorch repository.

Starting with:
- {{What is confirmed to exist and run}}
- {{Smallest next action}}
- {{Constraint or decision that must be carried forward}}

---

## Upcoming Context Document

The next message will be a CONTEXT DOCUMENT for:

RNN/LSTM Implementation — Bring-Your-Own Amazon Reviews Project

This continues discussion begun in:
"{{Exact previous chat title}}"

---

## Timing

Preparation:
{{YYYY-MM-DDTHH:MM:SS±ZZ:ZZ}}

(Optional) New chat:
{{YYYY-MM-DDTHH:MM:SS±ZZ:ZZ}}

---

## Instructions for Next Message

- Do not summarize, reformat, critique, or optimize the context document.
- Treat it as the authoritative snapshot, subject to newer verified evidence and my corrections.
- Confirm receipt and readiness; propose one small next action if requested.

---

## Immediate Focus

Help me:
{{Concrete, task-oriented next step}}

*End of PCDP*
```

For a chat that is *creating* a context document, the “Instructions for Next Message” section can be omitted. It is most useful when addressed to the new chat receiving the document.

## Naming convention

```text
LN_rnncmp_YYYY-MM-DD_{{optional-tag}}_-_{{short-slug}}.md
```

`LN` means Lab Notebook. Omit the optional tag unless it helps, such as `ctx01`, `parked`, or `submitted-addenda`. Choose a slug for the main engineering topic. An existing continuation file may retain its historical name; future files should be dated and specific.

## What belongs in a context document?

Capture the **current engineering state**, not merely a change log:

- Repository and notebook layout, including any `src/` extraction.
- Dataset source/revision, sampling method, cleaning, labels, and split definitions.
- Code that ran, observed outputs, and what remains unverified.
- Manual RNN and LSTM equations/shape conventions once implemented.
- Comparison protocol, results by review length, limitations, and open questions.
- A short, executable next action.

## Retrieval tip

1. Sort `LN_rnncmp_*` by filename and open the newest applicable snapshot.
2. Check `LAB_NOTEBOOK.md` for later runs or decisions.
3. Reconcile the snapshot against the current notebook and files.
4. Resume from **Immediate Next Steps**.

*End of README*
