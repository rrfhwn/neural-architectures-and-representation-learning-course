# Week 4: Training Dynamics and Failure Modes

## Contents

- **Week_04_Training_Dynamics_Failure_Modes.ipynb** — Canonical notebook for this week.

## Running

- **Local (uv):** From repo root run `uv sync`, then `uv run jupyter notebook weeks/04/Week_04_Training_Dynamics_Failure_Modes.ipynb`.
- **Colab:** Use the "Open in Colab" badge at the top of the notebook (update the URL to your public course repo).

## Dependencies

`numpy`, `matplotlib` only. No PyTorch in this notebook.

## Learning path

1. **Fast recap** — one-line update rule; 1D toy; change `learning_rate` and re-run.
2. **Shared setup** — same NumPy MLP helpers (`forward` / `backward` / `train_sgd`) as Week 3.
3. **Learning rate** — two-panel demo (small/moderate vs large `lr`); optional 1D loss-vs-`w` overshoot plot. Loss-vs-epoch plots use **log scale** for readability.
4. **Initialization** — effect of init scale on training curves (log-scale plots).
5. **Coding block 1** — sweep learning rates (`learning_rates` list); same `seed` for fair comparison (TODO: edit list).
6. **Momentum** — velocity update vs plain SGD (same learning rate).
7. **Train vs validation** — synthetic split; train vs val MSE per epoch (overfitting intuition).
8. **Coding block 2** — SGD vs momentum at two learning rates (`lr_a`, `lr_b`; TODO: edit).
9. **Wrap-up** — takeaway bullets.
10. **Homework / Post-class Extensions** — optional TODO scaffolds only (`NotImplementedError` / `pass`); see Week 3 notebook for worked examples to adapt.

## Interactivity

- TODOs in Sections 1, 4, and 7 (edit hyperparameters and re-run).
- Optional extension cells at the end (students implement bodies; not pre-filled solutions).
