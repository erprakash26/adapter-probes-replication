# Adapter Probes for Self-Interpretation — Small-Scale Replication

A small-scale replication of ["Learning Self-Interpretation from Interpretability Artifacts: Training Lightweight Adapters on Vector-Label Pairs"](https://arxiv.org/abs/2602.10352) (Pepper, McKenzie, Pop et al., AE Studio / AIAF), run on GPT-2-small with a 769-parameter adapter and 60 labeled SAE features.

The original paper shows that a tiny adapter trained on a frozen LM can learn to generate accurate natural-language self-descriptions from internal activation vectors, with self-interpretation quality improving from 7B to 72B scale. This notebook tests the opposite end of the spectrum — very small model, very small adapter, very little data — and specifically probes whether the adapter generalizes to features whose labels it never saw during training, versus falling back on a small set of generic completions. Full write-up: [LessWrong post link].

**To run:** open `adapter_probes_experiment.ipynb` in [Google Colab](https://colab.research.google.com/), set the runtime to a T4 GPU (Runtime → Change runtime type), and run top to bottom. You'll need a free [Hugging Face account/token](https://huggingface.co/settings/tokens) for the login step (GPT-2 itself is open, no gated access required).
