# Week 9: Transformers and Contextual Representations

## Contents

- **Week_09_Transformers_Contextual_Representations.ipynb** - Canonical teaching notebook for this week.
- **Assignment_04_Transformer_Representation_Analysis.ipynb** - Controlled graded assignment notebook.

## Running

- **Local (uv):** From repo root run `uv sync`, then open either notebook, for example:
  - `uv run jupyter notebook weeks/09/Week_09_Transformers_Contextual_Representations.ipynb`
  - `uv run jupyter notebook weeks/09/Assignment_04_Transformer_Representation_Analysis.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of each notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`, and `scikit-learn`. CPU is enough for the full notebook.

This week uses tiny inline datasets. There are no dataset downloads and no Hugging Face dependency in the core path.

## Learning Path

1. **Recap from Week 8** - attention pooling vs self-attention.
2. **Self-attention intuition** - queries, keys, values as roles.
3. **Ambiguous-word dataset** - classify `bank` in finance vs river contexts.
4. **Tiny transformer block** - token embeddings, positional embeddings, self-attention, residuals, feed-forward refinement.
5. **Coding block 1** - change transformer settings and inspect attention.
6. **Contextual representations** - compare static and contextual `bank` vectors.
7. **Attention-head inspection** - visualize per-head attention maps.
8. **Coding block 2** - try custom sentences and interpret representation behavior.
9. **Assignment-style framing** - connect the notebook to Assignment 4.

## Assignment 4

Use **Assignment_04_Transformer_Representation_Analysis.ipynb** for the graded transformer representation submission.

Students train and analyze a tiny transformer on an ambiguous-word task. The assignment emphasizes controlled comparison, attention visualization, contextual representation analysis, and explanation.

## External Resources

These are optional references, not required dependencies. Use them as visual anchors before or after class.

| Chapter | Resource | Why it helps |
|---|---|---|
| Self-attention intuition | [3Blue1Brown: Attention in transformers, visually explained](https://www.youtube.com/watch?v=eMlx5fFNoYc) | Best first visual explanation of attention as moving information between token vectors. |
| Transformer walkthrough | [Transformer Explainer](https://poloclub.github.io/transformer-explainer/) | Interactive GPT-2 view of tokenization, embeddings, attention, MLP blocks, and output probabilities. |
| Architecture overview | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | Clear visual bridge from attention to the full transformer block. |
| Contextual embeddings | [The Illustrated BERT](https://jalammar.github.io/illustrated-bert/) | Shows why contextual token representations matter for pretrained models. |
| Code reference | [The Annotated Transformer](http://nlp.seas.harvard.edu/annotated-transformer/) | Optional code-oriented reference for students who want implementation detail. |
| Attention inspection | [BertViz](https://github.com/jessevig/bertviz) | Optional tool for visualizing attention heads in pretrained transformer models. |
| Deep coding extension | [Andrej Karpathy: Let's build GPT from scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY) | Long optional coding deep dive; useful only after the core notebook feels comfortable. |
| Cautionary reading | [Attention is not Explanation](https://arxiv.org/abs/1902.10186) | Reminder that attention maps are useful evidence, not guaranteed human explanations. |
| Original paper | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Historical reference; optional and math-heavy. |

## Colab Pointers

- Run cells in order; the inspection cells reuse the trained `transformer_model`.
- The main object to inspect is `TinyTransformerClassifier`.
- `token_embedding` gives static token vectors.
- `pos_embedding` gives position information.
- `block.attn` performs self-attention.
- `classifier` predicts from the `[CLS]` contextual representation.
- If Colab state gets confusing after edits, use Runtime -> Restart session and run all.

## Interactivity

**Teaching notebook**

- TODOs in the transformer configuration block and custom-sentence analysis block.
- Static attention and contextual embedding plots are the reliable core path.
- Optional extensions are grouped at the end.

**Assignment notebook**

- Starter `TODO` comments in the experiment and reflection cells.

**Both**

- The central pattern is: inspect representation -> change one thing -> run -> observe -> explain.
