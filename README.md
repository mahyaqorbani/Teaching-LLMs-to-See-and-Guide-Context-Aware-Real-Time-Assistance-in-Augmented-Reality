# What Context Matters for LLM-Based AR Task Guidance? A Controlled Empirical Study

Code and sample data for the paper:

> Mahya Qorbani, Kamran Paynabar, and Mohsen Moghaddam. **What Context Matters for LLM-Based AR Task Guidance? A Controlled Empirical Study.** *ACM Transactions on Interactive Intelligent Systems (TiiS)*, 2026. DOI: _to be added_

An earlier preprint version is available on arXiv: [2511.00730](https://arxiv.org/abs/2511.00730).

## Overview

Large language models (LLMs) lack situational awareness in physical environments: without knowing what a user is doing or where they are in a task, they produce generic guidance. This study examines **which types of contextual information matter most** for LLM-generated task guidance in augmented reality (AR).

Using the [HoloAssist dataset](https://holoassist.github.io) (Microsoft Research), four model configurations receive progressively richer context through structured prompt-based context injection:

| Model | Context added |
|---|---|
| Model 1 (baseline) | Task type, approximate duration, conversation history |
| Model 2 | + Common task steps |
| Model 3 | + Current task step at question time |
| Model 4 | + Temporally aligned hand-action annotations (verb–noun pairs) |

All configurations operate under an **online information constraint**: each response uses only information available up to the moment the question is asked. Contextual signals come from temporally aligned dataset annotations rather than a deployed perception pipeline, which isolates the effect of each context type.

Responses are evaluated with lexical metrics (BERTScore, embedding similarity), LLM-as-a-judge scoring, and human evaluation. All-Except-One and Only-One ablations quantify each signal's contribution.

## Key findings

- Response quality improves monotonically from Model 1 to Model 4 (LLM-judge mean 2.69 → 4.41), consistently across GPT-4o, GPT-4.1, and GPT-5 backbones.
- Dynamic signals (current step, hand actions) give the largest gains; hand-action data is the most informative single signal, and task duration the least.
- Human and LLM-judge evaluations agree closely (71.5% winner overlap, Pearson r ≈ 0.74).

## Repository contents

- `Incremental Prompting Framework.ipynb`: Prompt templates for the four model configurations and API calls to generate responses. Requires your own Azure OpenAI (or OpenAI) endpoint and API key.
- `Evaluation Methods.ipynb`: Lexical metrics and LLM-as-a-judge evaluation. Run after responses for all four models have been generated.
- `Sample Data.csv`: Sample of the processed data for reproducing the workflow and adapting it to other tasks.

The full HoloAssist dataset must be obtained from its [official source](https://holoassist.github.io) under its license.

## Citation

```bibtex
@article{qorbani2026whatcontext,
  author  = {Qorbani, Mahya and Paynabar, Kamran and Moghaddam, Mohsen},
  title   = {What Context Matters for {LLM}-Based {AR} Task Guidance? A Controlled Empirical Study},
  journal = {ACM Transactions on Interactive Intelligent Systems},
  year    = {2026},
  doi     = {TBD}
}
```

## Contact

- Mahya Qorbani – mqorbani@gatech.edu
- Mohsen Moghaddam – mohsen.moghaddam@gatech.edu

## Acknowledgments

This work was supported by the National Science Foundation (NSF) under Grant No. 2128743.
