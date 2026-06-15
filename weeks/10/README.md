# Week 10: Practical Deep Learning Systems

## Contents

- **Week_10_Practical_Deep_Learning_Systems.ipynb** - Canonical teaching notebook for this week.
- **Assignment_05_Experiment_Tracking_Tuning.ipynb** - Controlled graded assignment notebook.

## Running

- **Local (uv):** From repo root run `uv sync`, then open either notebook, for example:
  - `uv run jupyter notebook weeks/10/Week_10_Practical_Deep_Learning_Systems.ipynb`
  - `uv run jupyter notebook weeks/10/Assignment_05_Experiment_Tracking_Tuning.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of each notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`, and `scikit-learn`. CPU is enough for the full notebook.

The core path does not require MLflow, Weights & Biases, Trackio, Optuna, Hugging Face, or model downloads. Those tools are discussed as production references, while the notebook builds the workflow ideas with small in-memory utilities.

## Learning Path

1. **Recap from Week 9** - representation quality needs evidence across runs.
2. **Practical task** - train a small representation MLP on the digits dataset.
3. **Run tracker** - log config, metrics, history, and small artifacts.
4. **Baseline run** - establish a reference point.
5. **Controlled experiments** - compare changes without relying on memory.
6. **Coding block 1** - add two tracked student runs.
7. **Hyperparameter tuning intuition** - run a tiny random search as an Optuna-shaped workflow.
8. **Optional Optuna API block** - read or run the same search idea with real Optuna syntax.
9. **Fine-tuning workflow** - compare scratch, frozen representation, and fine-tuning strategies.
10. **Assignment-style framing** - connect the notebook to Assignment 5.

## Search Strategy Note

Small models can sometimes support a full grid search because every combination is cheap enough to run. As models get larger, exhaustive grids become wasteful quickly; use random/Optuna search for broader sampling, or a controlled ladder where you change one parameter at a time and keep the best stable setting before moving to the next parameter.

## Assignment 5

Use **Assignment_05_Experiment_Tracking_Tuning.ipynb** for the graded practical workflow submission.

Students run and compare tracked experiments on a small representation model. The assignment emphasizes configuration logging, validation/test comparison, hyperparameter search interpretation, final model selection, and a freeze-vs-fine-tune decision.

## External Resources

These are optional references, not required dependencies.

| Chapter | Resource | Why it helps |
|---|---|---|
| Experiment tracking | [MLflow Tracking docs](https://mlflow.org/docs/latest/ml/tracking/) | Standard vocabulary: experiments, runs, parameters, metrics, and artifacts. |
| Experiment dashboards | [Weights & Biases docs](https://docs.wandb.ai/) | Shows the production version of the run-comparison workflow built manually in the notebook. |
| Local-first tracking | [Hugging Face Trackio docs](https://huggingface.co/docs/trackio/index) | Lightweight local dashboard, W&B-style API, and optional Hugging Face Spaces sharing. |
| Hyperparameter tuning | [Optuna docs](https://optuna.readthedocs.io/) | Official reference for define-by-run hyperparameter optimization. |
| Fine-tuning workflow | [Hugging Face fine-tuning guide](https://huggingface.co/docs/transformers/en/training) | Practical bridge from this tiny notebook to pretrained-model workflows. |
| MLOps heuristics | [Google: Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml) | Engineering heuristics for avoiding premature workflow complexity. |

## Colab Pointers

- Run cells in order; tracked runs accumulate in `RunTracker` objects.
- `tracker.table()` gives the main comparison table.
- `plot_histories(...)` compares validation curves.
- `plot_final_metrics(...)` or `plot_final_bars(...)` compares validation and test results.
- If Colab state gets confusing after edits, use Runtime -> Restart session and run all.

## Interactivity

**Teaching notebook**

- TODOs in the tracked-run configuration block.
- The random search is intentionally small and CPU-safe.
- Search strategy is discussed explicitly: full grid for tiny spaces, random/Optuna for medium spaces, and controlled ladders for expensive runs.
- The Optuna cell is optional and skipped by default unless `optuna` is installed.
- Fine-tuning is simulated on a small even-vs-odd transfer task.

**Assignment notebook**

- Starter `TODO` comments in the controlled experiment, search, final decision, and reflection sections.

**Both**

- The central pattern is: configure -> run -> track -> compare -> decide -> explain.
