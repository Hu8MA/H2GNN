# Best-Experiment-2 (🥈 Second Best)

## Model Configuration

| Parameter | Value |
|-----------|-------|
| Model Name | Model_metabolic_network_1 |
| Learning Rate | 0.005 |
| Hidden Units | 128 |
| Dropout | 0.5 |
| Weight Decay | 0.0 |
| Alpha | 0.5 |
| Training Seed | 42 |

## Results

| Metric | Value |
|--------|:-----:|
| **ROC-AUC (macro)** | 99.44% |
| **PR-AUC (macro)** | 87.24% |
| **Top-1 Accuracy** | 85.73% |
| **Top-3 Accuracy** | 98.11% |
| **Precision (macro)** | 84.99% |
| **Recall (macro)** | 80.10% |
| **F1-Score (macro)** | 81.08% |
| **Precision (weighted)** | 86% |
| **Recall (weighted)** | 86% |
| **F1-Score (weighted)** | 86% |

## Training Details

| Metric | Value |
|--------|:-----:|
| Best Epoch | 499 |
| Best Validation Loss | 0.5535 |
| Total Training Time | 17.28 minutes |
| RAM Used | 0.29 GB |

## Files in This Folder

```
Best-Experiment-2/
├── Model1_metabolic.ipynb    # Google Colab notebook with full code
├── info-Model-1.docx         # Detailed configuration and results
├── README.md                 # This file
└── OutPut/                   # Saved model weights and outputs
```

## Input Embedding

This model uses **E-1** embedding from [Chemical Network Best-Experiment-1](https://github.com/Hu8MA/H2GNN/tree/main/chemical/Best-experience-1).

## Note

This model achieved identical metrics to Best-Experiment-1, but ranked 2nd due to higher validation loss (0.5535 vs 0.4900).
