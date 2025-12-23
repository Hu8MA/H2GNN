# Metabolic Network

Multi-class classification of drug-drug interaction types (86 classes) using embeddings from the Chemical Network.

## 📁 Folder Structure

```
metabolic/
│
├── Best-Experiment-1/                       # 🥇 Top performing experiment
│   ├── Model2_metabolic.ipynb               # Google Colab notebook
│   ├──metabolic_Best-Experiment-1_README.md # Detailed results
│   └── OutPut/                              # Model outputs
│
├── Best-Experiment-2/                        # 🥈 Second best experiment
│   ├── Model1_metabolic.ipynb                # Google Colab notebook
│   ├── metabolic_Best-Experiment-2_README.md # Detailed results
│   └── OutPut/                               # Model outputs
│
├── Best-Embedding/                          # Embeddings from Chemical Network
│   ├── Model1-S42-K9-Experiment-1/          # E-1 (from chemical 🥇)
│   └── Model1-S32-K12-Experiment-2/         # E-2 (from chemical 🥈)
│
├── DataSet-Partitions/                      # Train/Validation/Test splits
│   ├── Metabolic-Seed32/
│   ├── Metabolic-Seed42/
│   ├── ddi_DrugBank_label_map.csv
│   └── Summary-typer-inter.xlsx
│
├── Metabolic-Hypergraph/                    # Hypergraph structure files
│   ├── Code/                                # Hypergraph construction scripts
│   ├── Drugs_interaction-types.csv
│   ├── metabolic_hypergraph.pt
│   └── metabolic_hypergraph_metadata.pt
│
└── README.md                               
```

---

## 🧪 Experimental Summary

| Setting | Values |
|---------|--------|
| **Task** | Multi-class Classification (86 Interaction Types) |
| **Dataset Seeds** | 32, 42 |
| **Chemical Embeddings** | E-1, E-2 |
| **Model Configurations** | 3 |
| **Total Experiments** | **12** |

---

## 🏆 Top 3 Results

| Rank | ROC-AUC | PR-AUC | Top-1 Acc | Top-3 Acc | Weighted F1 |
|:----:|:-------:|:------:|:---------:|:---------:|:-----------:|
| 🥇 | **99.44%** | 87.24% | 85.73% | **98.11%** | **86%** |
| 🥈 | **99.44%** | 87.24% | 85.73% | **98.11%** | **86%** |
| 🥉 | 99.44% | 86.76% | 85.33% | 97.93% | 85% |

*Note: Ranks 1 and 2 have identical metrics. Final ranking determined by validation loss (0.4900 vs 0.5440).*

---

## 📊 All Experimental Results

### Seed 32

| Embedding | Model | ROC-AUC | PR-AUC | Top-1 Acc | Top-3 Acc | Macro F1 | Weighted F1 |
|:---------:|:-----:|:-------:|:------:|:---------:|:---------:|:--------:|:-----------:|
| E-1 | M1 | 0.9942 | 0.8660 | 0.8521 | 0.9784 | 0.80 | 0.85 |
| **E-1** | **M2** | **0.9944** | **0.8676** | **0.8533** | **0.9793** | **0.81** | **0.85** |
| E-1 | M3 | 0.9803 | 0.5816 | 0.7601 | 0.9470 | 0.43 | 0.75 |
| E-2 | M1 | 0.9958 | 0.8640 | 0.8554 | 0.9807 | 0.79 | 0.85 |
| **E-2** | **M2** | **0.9944** | **0.8620** | **0.8510** | **0.9793** | **0.80** | **0.85** |
| E-2 | M3 | 0.9765 | 0.5693 | 0.7625 | 0.9408 | 0.40 | 0.85 |

### Seed 42

| Embedding | Model | ROC-AUC | PR-AUC | Top-1 Acc | Top-3 Acc | Macro F1 | Weighted F1 |
|:---------:|:-----:|:-------:|:------:|:---------:|:---------:|:--------:|:-----------:|
| **E-1** | **M1** | **0.9944** | **0.8724** | **0.8573** | **0.9811** | **0.81** | **0.86** |
| **E-1** | **M2** | **0.9944** | **0.8724** | **0.8573** | **0.9811** | **0.81** | **0.86** |
| E-1 | M3 | 0.9818 | 0.5530 | 0.7601 | 0.9447 | 0.43 | 0.75 |
| E-2 | M1 | 0.9926 | 0.8764 | 0.8518 | 0.9801 | 0.79 | 0.85 |
| E-2 | M2 | 0.9926 | 0.8811 | 0.8524 | 0.9799 | 0.79 | 0.85 |
| E-2 | M3 | 0.9838 | 0.5674 | 0.7614 | 0.9442 | 0.41 | 0.75 |

---

## 📈 Key Findings

- **E-1 Embedding** (from Chemical Best-Experiment-1) achieved all top rankings
- **Alpha = 0.3** (Model 2) slightly outperformed Alpha = 0.5 (Model 1)
- **Alpha = 0.7** (Model 3) performed poorly due to class imbalance sensitivity
- **Seed 42** consistently produced the best results

---

## 🔗 Input Embeddings

Embeddings are transferred from the [Chemical Network](https://github.com/Hu8MA/H2GNN/tree/main/chemical):

| Embedding | Source | Description |
|-----------|--------|-------------|
| **E-1** | Chemical Best-Experiment-1 | Model1-S42-K9 (🥇 98.46% ROC-AUC) |
| **E-2** | Chemical Best-Experiment-2 | Model1-S32-K12 (🥈 98.42% ROC-AUC) |
