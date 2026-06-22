# Week 11: Choosing Representations and Building Responsible Systems

## Contents

- **Week_11_Choosing_Representations_Responsible_Systems.ipynb** - Final integration and course-wrap notebook.

There is no new graded assignment. Assignment 5 remains the final practical submission.

## Running

- **Local (uv):** From repo root run `uv sync`, then:
  - `uv run jupyter notebook weeks/11/Week_11_Choosing_Representations_Responsible_Systems.ipynb`
- **Colab:** Use the "Open in Colab" badge at the top of the notebook.

## Dependencies

`torch`, `numpy`, `matplotlib`, and `scikit-learn`. CPU is enough. The notebook uses the built-in digits dataset and requires no downloads.

## Learning Path

1. **Architecture decision map** - connect data structure to MLPs, CNNs, RNNs, transformers, and pretrained representations.
2. **Shared case study** - compare an MLP and CNN on the same digits task.
3. **Representation geometry** - inspect PCA projections of learned features.
4. **Coding block 1** - make and defend an architecture decision using validation accuracy, size, time, and representation evidence.
5. **Failure audit** - inspect per-class performance, confusion matrices, and confident errors.
6. **Distribution shift** - compare clean and synthetically shifted inputs.
7. **Coding block 2** - audit subgroups, confidence, abstention, or shift severity.
8. **System thinking** - connect data, training, artifacts, deployment, monitoring, and rollback.
9. **Model/system card** - document intended use, limitations, evidence, risks, and operational fallback.
10. **Current directions** - PEFT/LoRA, multimodality, retrieval, efficient inference, and system evaluation.

The notebook uses validation evidence for model choice and reserves test evidence for final auditing. Its example digit subgroup demonstrates slice analysis, not demographic fairness.

## External Resources

| Topic | Resource | Why it helps |
|---|---|---|
| Parameter-efficient adaptation | [Hugging Face PEFT quicktour](https://huggingface.co/docs/peft/quicktour) | Shows how adapters update a small fraction of a pretrained model. |
| LoRA | [Hugging Face LoRA reference](https://huggingface.co/docs/peft/package_reference/lora) | Concrete description of low-rank adaptation. |
| Model documentation | [Hugging Face Model Cards](https://huggingface.co/docs/hub/model-cards) | Practical structure for intended use, evaluation, limitations, and sharing. |
| Responsible AI systems | [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) | Connects model work to governance, measurement, and risk management. |
| API deployment | [FastAPI deployment concepts](https://fastapi.tiangolo.com/deployment/concepts/) | Shows that serving a model is one part of operating it. |

## Colab Pointers

- Run cells in order; the audit sections reuse the trained `mlp` and `cnn`.
- `mlp_eval` and `cnn_eval` contain probabilities, predictions, and learned representations.
- The synthetic shift is deterministic and can be made milder or stronger.
- If state becomes confusing, restart the Colab session and run all.

## Central Pattern

`problem -> data structure -> representation -> architecture -> evidence -> system -> monitoring`
