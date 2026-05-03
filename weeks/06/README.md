# Week 6: Fixing Models - Generalization and Stability

## Contents

- **Week_06_Fixing_Models_Generalization_Stability.ipynb** - Canonical notebook for this week.
- **Assignment_01_Model_Repair.ipynb** - Controlled graded assignment notebook.

## Running

- **Local (uv):** From repo root run `uv sync`, then open either notebook, for example:
  - `uv run jupyter notebook weeks/06/Week_06_Fixing_Models_Generalization_Stability.ipynb`
  - `uv run jupyter notebook weeks/06/Assignment_01_Model_Repair.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of each notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`. CPU is enough. No external dataset download is required.

Optional: `ipywidgets` for the interactive repair lab in the teaching notebook. The static path through that notebook does not depend on widgets. The assignment notebook does not use widgets.

## Learning Path

1. **Quick recap** - train/validation signals for broken models.
2. **Shared setup** - small nonlinear binary classification task.
3. **Diagnosis dashboard** - underfitting, overfitting, and instability.
4. **Capacity** - small, medium, and large MLPs.
5. **Coding block 1** - diagnose capacity and label failure modes.
6. **Stability fixes** - initialization, activation choice, and gradient clipping.
7. **Regularization fixes** - dropout, batch normalization, and early stopping.
8. **Interactive repair lab** - optional widget panel for toggling repair tools.
9. **Coding block 2** - repair a deliberately broken model.
10. **Assignment-style repair** - points to the controlled assignment notebook.
11. **Extensions** - weight decay, repair grids, early stopping sensitivity.

## Assignment 1

Use **Assignment_01_Model_Repair.ipynb** for the graded model-repair submission.

The teaching notebook is exploratory. The assignment notebook fixes the dataset, baseline, seed, metrics, and required evidence so submissions are comparable.

## Interactivity

**Teaching notebook**

- TODOs in Sections 4 and 7 of the learning path above.
- Optional widgets after the regularization section.
- Optional extension cells at the end.

**Assignment notebook**

- Starter `TODO` comments in the repair experiment cells (replace with your settings and runs).

**Both**

- Train/validation curves are the main diagnostic artifact.
- The central pattern is: diagnose -> change one thing -> run -> observe -> explain.
