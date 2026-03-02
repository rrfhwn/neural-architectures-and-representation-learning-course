# Week 2: Perceptron, Backpropagation, and the Training Loop

## Contents

- **Week_02_Perceptron_Backprop_TrainingLoop.ipynb** — Main notebook for this week.

## Running

- **Local (uv):** From repo root run `uv sync`, then `uv run jupyter notebook weeks/02/Week_02_Perceptron_Backprop_TrainingLoop.ipynb`.
- **Colab:** Use the "Open in Colab" badge at the top of the notebook; it links to the notebook on the [public course repo](https://github.com/rrfhwn/neural-architectures-and-representation-learning-course).

## Dependencies

Only: `torch`, `torchvision`, `matplotlib`, `numpy`. CPU is enough; CUDA is optional for the MNIST section.

## Learning path

1. **Foundations:** Single neuron (w^T x + b, activation), perceptron definition and update rule, step vs differentiable loss, training loop pseudocode (batch / epoch / forward / backward / step).
2. **Perceptron from scratch:** 2D separable toy data (two Gaussian clusters), plot decision boundary; then add a third cluster to one class and continue training to see the boundary shift.
3. **XOR:** Visualise XOR failure of a linear classifier; train a tiny MLP to solve XOR and plot its decision boundary.
4. **MNIST:** Minimal training loop (1–2 epochs) to practise the full pipeline.

## Interactivity

- At least 6 TODOs for hands-on changes (e.g. change `n_per_class`, centroid, activation, batch size, add accuracy).
- Pause & Reflect blocks after key concepts and experiments.
- Three debate prompts at the end for discussion.
