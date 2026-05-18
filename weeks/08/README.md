# Week 8: Sequence Representations and Attention

## Contents

- **Week_08_Sequence_Representations_Attention.ipynb** - Canonical teaching notebook for this week.
- **Assignment_03_Sequence_Representations_Attention.ipynb** - Controlled graded assignment notebook.

## Running

- **Local (uv):** From repo root run `uv sync`, then open either notebook, for example:
  - `uv run jupyter notebook weeks/08/Week_08_Sequence_Representations_Attention.ipynb`
  - `uv run jupyter notebook weeks/08/Assignment_03_Sequence_Representations_Attention.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of each notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`, and `scikit-learn`. CPU is enough for the full notebook.

This week uses tiny inline datasets. There are no dataset downloads.

## Learning Path

1. **Recap from CNNs** - spatial representations become a bridge to sequence representations.
2. **Why order matters** - compare sequences with the same tokens in different orders.
3. **Character sequence modeling** - train a tiny RNN on names.
4. **Hidden-state inspection** - visualize evolving memory and prefix predictions.
5. **Coding block 1** - change sequence-model knobs and inspect what changes.
6. **Word embeddings** - train a tiny sentence classifier and inspect learned vectors.
7. **Attention intuition** - visualize which words receive high attention.
8. **Coding block 2** - compare nearest neighbors and attention heatmaps.
9. **Assignment-style framing** - connect the notebook to Assignment 3.

Attention note: Week 8 uses single-head attention pooling, not full transformer self-attention. The heatmaps show which tokens this tiny model emphasized, but they should be read as debugging clues rather than guaranteed human explanations.

## Assignment 3

Use **Assignment_03_Sequence_Representations_Attention.ipynb** for the graded sequence representation submission.

Students train and analyze small sequence models. The assignment emphasizes controlled comparison, visualization, and explanation rather than final accuracy alone.

## External Resources

### Sequence and RNN Intuition

- Understanding LSTM Networks: https://colah.github.io/posts/2015-08-Understanding-LSTMs/
- The Unreasonable Effectiveness of RNNs: https://karpathy.github.io/2015/05/21/rnn-effectiveness/
- PyTorch character-level RNN tutorial: https://docs.pytorch.org/tutorials/intermediate/char_rnn_classification_tutorial.html

Quick framing: `RNN = simple recurrent memory`; `LSTM = recurrent memory with learned gates`. The notebook uses a plain RNN because it is easiest to inspect, while the LSTM resource explains why gated memory helps on longer or harder sequences.

### Embeddings

- 3Blue1Brown word embeddings video: https://www.youtube.com/watch?v=wjZofJX0v4M&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=6&t=747s
- TensorFlow Embedding Projector: https://projector.tensorflow.org/
- How to Use t-SNE Effectively: https://distill.pub/2016/misread-tsne/

### Attention

- Visualizing seq2seq attention: https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/
- The Illustrated Transformer: https://jalammar.github.io/illustrated-transformer/
- Attention Is All You Need: https://arxiv.org/abs/1706.03762

## Interactivity

**Teaching notebook**

- TODOs in the character-RNN block and attention/embedding block.
- Static hidden-state, embedding, and attention plots are the reliable core path.
- Optional extensions are grouped at the end.

**Colab pointers**

- RNN section: run cells in order and inspect `CharRNNClassifier`; `embedding` maps characters to vectors, `rnn` updates the hidden memory, and `classifier` predicts from the final memory.
- Embedding section: inspect `mean_model.embedding.weight`; use the PCA plot and `nearest_words(...)` as intuition aids, and keep custom sentences close to the tiny vocabulary.

**Assignment notebook**

- Starter `TODO` comments in the experiment and reflection cells.

**Both**

- The central pattern is: inspect representation -> change one thing -> run -> observe -> explain.
