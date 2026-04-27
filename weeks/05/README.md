# Week 5: Optimization Improvements + PyTorch

## Contents

- **Week_05_Optimization_Improvements_PyTorch.ipynb** - Canonical notebook for this week.

## Running

- **Local (uv):** From repo root run `uv sync`, then `uv run jupyter notebook weeks/05/Week_05_Optimization_Improvements_PyTorch.ipynb`.
- **Colab:** Use the "Open in Colab" badge at the top of the notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`. CPU is enough. `torchvision` is not used in this notebook.

The notebook intentionally does not install or upgrade PyTorch during normal execution. It includes a commented-out optional update cell for later use if a runtime is stale; students should restart the runtime/kernel after package upgrades.

## Learning Path

1. **Quick recap** - learning rate and momentum on a 1D quadratic.
2. **Momentum refined** - velocity vs gradient; sensible beta values.
3. **PyTorch transition** - manual training loop mapped to `loss.backward()` and `optimizer.step()`.
4. **Coding block 1** - compare SGD and momentum by editing learning rate and beta.
5. **Adaptive optimizers** - RMSprop and Adam intuition.
6. **Optimizer comparison** - SGD, momentum, RMSprop, Adam on the same toy regression task.
7. **Coding block 2** - optimizer and learning-rate exploration.
8. **Early stopping** - validation monitoring with patience.
9. **Homework / Post-class Extensions** - optional TODO scaffolds for schedules and hyperparameter search.

## Interactivity

- TODOs in Sections 1, 4, and 7.
- Optional extension cells at the end.
- Loss plots use log scale where useful.
- The central pattern is: change one thing -> run -> observe -> explain.
