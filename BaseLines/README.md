# BaseLines

Baseline models used for comparison with H²GNN.

## 📁 Folder Structure

```
BaseLines/
├── GAT_MLP.ipynb                           # Graph Attention Network (excluded due to instability)
├── GCN-singlelayer_MLP_Morgan512.ipynb     # Single-layer GCN (failed to converge on CPU)
├── GCN-towlayer_MLP_Morgan512.ipynb        # Two-layer GCN + MLP Decoder
├── GraphSAGE_singlelayerMLP_Morgan512.ipynb # Single-layer GraphSAGE (failed to converge on CPU)
├── GraphSAGE-towlayer_MLP_Morgan512.ipynb  # Two-layer GraphSAGE + MLP Decoder
├── RandomForest.ipynb                      # Random Forest + Morgan Fingerprints
├── XGBoost.ipynb                           # XGBoost + Morgan Fingerprints
└── README.md                              
```

---

## 📊 Binary Classification Results (Chemical Network)

| Model | Accuracy | F1 | ROC-AUC | PR-AUC |
|-------|:--------:|:--:|:-------:|:------:|
| Random Forest + Morgan FP | 79% | 80% | 88% | 88% |
| GCN + Morgan FP | 88% | 88% | 95% | 95% |
| **H²GNN (Ours)** | **93%** | **93%** | **98%** | **98%** |

---

## 📊 Multi-class Classification Results (Metabolic Network)

| Model | Top-1 Acc | Top-3 Acc | ROC-AUC | PR-AUC | Macro F1 | Weighted F1 |
|-------|:---------:|:---------:|:-------:|:------:|:--------:|:-----------:|
| GCN + Morgan FP | 45.9% | 80.7% | 97.89% | 56.77% | 42% | 48% |
| XGBoost + Morgan FP | 69.9% | 92.4% | 98.46% | 70.92% | 64% | 69% |
| GraphSAGE + Morgan FP | 80.9% | 96.8% | 99.41% | 76.76% | 59% | 81% |
| **H²GNN (Ours)** | **85.7%** | **98.1%** | **99.44%** | **87.24%** | **81%** | **86%** |

---

## ⏱️ Training Time Comparison (Metabolic Network)

| Model | Training Time | Hardware |
|-------|:-------------:|:--------:|
| **H²GNN (Ours)** | **18.6 min** | CPU (2-core) |
| GCN (2-layer) | 75.56 min | GPU (T4) |
| GraphSAGE (2-layer) | 148.52 min | GPU (T4) |
| XGBoost | 225.55 min | CPU |

---

## 📝 Notes

- **Single-layer GCN/GraphSAGE**: Failed to converge on CPU (validation error >100). Required 2-layer architecture + GPU.
- **GAT**: Excluded due to training instability with class imbalance.
- **All baselines** received Morgan Fingerprints as input features — an advantage H²GNN does not require.
- **H²GNN** achieves **4-12× faster** training while outperforming all baselines.

---

## 📂 Data Usage

| Baseline Task | Uses Data From |
|---------------|----------------|
| Binary Classification (Random Forest, GCN) | [chemical/DataSet-Partitions/](../chemical/DataSet-Partitions/) |
| Multi-class Classification (GCN, GraphSAGE, XGBoost) | [metabolic/DataSet-Partitions/](../metabolic/DataSet-Partitions/) |

---

## ⚠️ Important Note

Some file paths in the notebooks may contain **`MLHYGNN`** — this was the original model name before it was renamed to **H²GNN**. Both names refer to the same project.
