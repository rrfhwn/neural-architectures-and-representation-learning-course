# Week 7: CNNs and Visual Representations

## Contents

- **Week_07_CNNs_Visual_Representations.ipynb** - Canonical teaching notebook for this week.
- **Assignment_02_CNN_Representations.ipynb** - Controlled graded assignment notebook.

## Running

- **Local (uv):** From repo root run `uv sync`, then open either notebook, for example:
  - `uv run jupyter notebook weeks/07/Week_07_CNNs_Visual_Representations.ipynb`
  - `uv run jupyter notebook weeks/07/Assignment_02_CNN_Representations.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of each notebook.

## Dependencies

`torch`, `torchvision`, `numpy`, and `matplotlib`. CPU is enough for the core path.

The MNIST section downloads MNIST. The color representation section downloads CIFAR-10 and may download pretrained ResNet18 weights. Pre-run the notebook before class so downloads are cached.

## Learning Path

1. **Kernel intuition** - use an external image-kernel demo to understand local filters.
2. **Tiny MNIST CNN** - build a small CNN and inspect tensor shapes.
3. **Full MNIST training** - train the CNN and plot loss/accuracy.
4. **Feature inspection** - visualize learned filters and feature maps.
5. **Coding block 1** - change CNN architecture knobs and observe effects.
6. **External CNN visualizers** - connect our code to richer CNN visual explanations.
7. **Color representation task** - compute hue/saturation disk targets for color images.
8. **Pretrained features** - freeze a CNN backbone and train a small regression head.
9. **Coding block 2** - experiment with representation-head settings.
10. **Assignment-style framing** - connect the notebook to Assignment 2.

## Assignment 2

Use **Assignment_02_CNN_Representations.ipynb** for the graded CNN representation submission.

Students use a frozen CNN representation and train small heads to predict hue/saturation disk coordinates from CIFAR-10 images. The assignment emphasizes comparison, visualization, and explanation rather than leaderboard-style accuracy.

## External Visualizers

- Setosa image kernels: https://setosa.io/ev/image-kernels/
- Adam Harley MNIST CNN visualizer: https://adamharley.com/nn_vis/cnn/2d.html
- MNIST/CNN visualization page: https://www.brilliantwavetech.com/cnn-visualization.html
- CNN Explainer: https://poloclub.github.io/cnn-explainer/

## Interactivity

**Teaching notebook**

- TODOs in the MNIST architecture block and representation-head block.
- Optional hover visualization scaffold at the end.
- Static plots are the reliable core path.

**Assignment notebook**

- Starter `TODO` comments in the experiment and final-model cells.

**Both**

- The central pattern is: inspect representation -> change one thing -> run -> observe -> explain.
