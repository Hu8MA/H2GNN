# Chemical Network

Binary classification of drug-drug interactions using K-mer representations of SMILES strings.

## 📁 Folder Structure

```
chemical/
│
├── Best-Experiment-1/                  # 🥇 Top performing experiment
│   ├── Chemical-Model2.ipynb           # Google Colab notebook
│   ├── Best-Experiment-1_README.md     # Detailed results
│   └── OutPut/                         # Model outputs and saved files
│
├── Best-Experiment-2/                  # 🥈 Second best experiment
│   ├── Chemical-Model1.ipynb           # Google Colab notebook
│   ├── Best-Experiment-2_README.md     # Detailed results
│   └── OutPut/                         # Model outputs and saved files
│
├── DataSet/                            # Raw datasets
│   ├── Code/                           # Data processing scripts
│   ├── Data_analysis_of_1709_drugs.csv
│   ├── DDI_unique_interactions.csv
│   ├── DeepDDI-DrunkBunk_Original.csv
│   ├── Drugbank_vocabulary_from_original_Dru...csv
│   ├── Drugs_With_SMILES.csv
│   ├── Final_table_of_drug_information.csv
│   └── TDC-DrungBank-Original-WithLables.csv
│
├── DataSet-Partitions/                 # Train/Validation/Test splits
│                                       # Seeds: 32, 42, 46
│
├── Hypergraph_Chemical/                # Hypergraph structure files
│   ├── Code/                           # Hypergraph construction scripts
│   ├── hyG_drug_drugbank_kmer_3.pt
│   ├── hyG_drug_drugbank_kmer_3_metadata.pt
│   ├── hyG_drug_drugbank_kmer_6.pt
│   ├── hyG_drug_drugbank_kmer_6_metadata.pt
│   ├── hyG_drug_drugbank_kmer_9.pt
│   ├── hyG_drug_drugbank_kmer_9_metadata.pt
│   ├── hyG_drug_drugbank_kmer_12.pt
│   └── hyG_drug_drugbank_kmer_12_metadata.pt
│
├── K-mer/                              # K-mer feature files
│   ├── Code/                           # K-mer extraction scripts
│   ├── drugbank_kmers_k3.csv
│   ├── drugbank_kmers_k6.csv
│   ├── drugbank_kmers_k9.csv
│   ├── drugbank_kmers_k12.csv
│   └── drugbank_kmers_k15.csv
│
└── README.md                          
```

---

## 🧪 Experimental Summary

| Setting                  | Values                                               |
| ------------------------ | ---------------------------------------------------- |
| **Task**                 | Binary Classification (Interaction / No Interaction) |
| **K-mer Lengths**        | 3, 6, 9, 12                                          |
| **Dataset Seeds**        | 32, 42, 46                                           |
| **Model Configurations** | 3                                                    |
| **Total Experiments**    | **36**                                               |

---

## 🏆 Top 3 Results

| Rank | Accuracy | Precision | Recall | F1-Score |  ROC-AUC   |   PR-AUC   |
| :--: | :------: | :-------: | :----: | :------: | :--------: | :--------: |
|  🥇  |  93.20%  |  92.36%   | 94.49% |  93.41%  | **98.46%** | **98.47%** |
|  🥈  |  93.13%  |  91.96%   | 94.69% |  93.30%  |   98.42%   |   98.41%   |
|  🥉  |  93.01%  |  92.05%   | 94.58% |  93.30%  |   98.41%   |   98.40%   |

---

## 📊 All Experimental Results

### Seed 32

|   Model    |   K    |  Accuracy  | Precision  |   Recall   |     F1     |  ROC-AUC   |   PR-AUC   |
| :--------: | :----: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
|   Model1   |   3    |   0.8660   |   0.8375   |   0.9131   |   0.8737   |   0.9413   |   0.9349   |
|   Model2   |   3    |   0.8426   |   0.8271   |   0.8743   |   0.8500   |   0.9226   |   0.9211   |
|   Model3   |   3    |   0.8501   |   0.8320   |   0.8790   |   0.8548   |   0.9286   |   0.9274   |
|   Model1   |   6    |   0.9195   |   0.9018   |   0.9423   |   0.9216   |   0.9775   |   0.9767   |
|   Model2   |   6    |   0.9070   |   0.8872   |   0.9342   |   0.9101   |   0.9700   |   0.9687   |
|   Model3   |   6    |   0.9187   |   0.8981   |   0.9438   |   0.9204   |   0.9754   |   0.9736   |
| **Model1** | **9**  | **0.9301** | **0.9205** | **0.9458** | **0.9330** | **0.9841** | **0.9840** |
|   Model2   |   9    |   0.9118   |   0.8941   |   0.9367   |   0.9149   |   0.9730   |   0.9723   |
|   Model3   |   9    |   0.9250   |   0.9074   |   0.9456   |   0.9261   |   0.9795   |   0.9782   |
| **Model1** | **12** | **0.9313** | **0.9196** | **0.9469** | **0.9330** | **0.9842** | **0.9841** |
|   Model2   |   12   |   0.9073   |   0.8885   |   0.9319   |   0.9097   |   0.9709   |   0.9700   |
|   Model3   |   12   |   0.9249   |   0.9101   |   0.9450   |   0.9272   |   0.9808   |   0.9802   |

### Seed 42

|   Model    |   K    |  Accuracy  | Precision  |   Recall   |     F1     |  ROC-AUC   |   PR-AUC   |
| :--------: | :----: | :--------: | :--------: | :--------: | :--------: | :--------: | :--------: |
|   Model1   |   3    |   0.8870   |   0.8742   |   0.9090   |   0.8913   |   0.9565   |   0.9558   |
|   Model2   |   3    |   0.8448   |   0.8234   |   0.8799   |   0.8507   |   0.9240   |   0.9226   |
|   Model3   |   3    |   0.8486   |   0.8316   |   0.8789   |   0.8546   |   0.9278   |   0.9263   |
| **Model1** | **6**  | **0.9288** | **0.9138** | **0.9491** | **0.9312** | **0.9824** | **0.9821** |
|   Model2   |   6    |   0.8903   |   0.8778   |   0.9096   |   0.8934   |   0.9595   |   0.9595   |
|   Model3   |   6    |   0.9212   |   0.9048   |   0.9440   |   0.9240   |   0.9772   |   0.9754   |
| **Model1** | **9**  | **0.9320** | **0.9236** | **0.9449** | **0.9341** | **0.9846** | **0.9847** |
|   Model2   |   9    |   0.9064   |   0.8948   |   0.9242   |   0.9093   |   0.9698   |   0.9687   |
|   Model3   |   9    |   0.9228   |   0.9183   |   0.9356   |   0.9269   |   0.9804   |   0.9800   |
| **Model1** | **12** | **0.9290** | **0.9253** | **0.9376** | **0.9314** | **0.9834** | **0.9832** |
|   Model2   |   12   |   0.9032   |   0.8850   |   0.9290   |   0.9065   |   0.9695   |   0.9692   |
|   Model3   |   12   |   0.9228   |   0.9183   |   0.9356   |   0.9269   |   0.9804   |   0.9800   |

### Seed 46

| Model  |  K  | Accuracy | Precision | Recall |   F1   | ROC-AUC | PR-AUC |
| :----: | :-: | :------: | :-------: | :----: | :----: | :-----: | :----: |
| Model1 |  3  |  0.8729  |  0.8613   | 0.8970 | 0.8788 | 0.9486  | 0.9474 |
| Model2 |  3  |  0.8487  |  0.8322   | 0.8785 | 0.8547 | 0.9275  | 0.9260 |
| Model3 |  3  |  0.8498  |  0.8329   | 0.8811 | 0.8563 | 0.9301  | 0.9285 |
| Model1 |  6  |  0.9243  |  0.9180   | 0.9393 | 0.9285 | 0.9803  | 0.9790 |
| Model2 |  6  |  0.8954  |  0.8793   | 0.9190 | 0.8987 | 0.9616  | 0.9615 |
| Model3 |  6  |  0.9150  |  0.9001   | 0.9360 | 0.9177 | 0.9738  | 0.9723 |
| Model1 |  9  |  0.9279  |  0.9226   | 0.9385 | 0.9305 | 0.9829  | 0.9828 |
| Model2 |  9  |  0.9051  |  0.8841   | 0.9314 | 0.9071 | 0.9678  | 0.9665 |
| Model3 |  9  |  0.9224  |  0.9053   | 0.9450 | 0.9247 | 0.9784  | 0.9768 |
| Model1 | 12  |  0.9279  |  0.9248   | 0.9370 | 0.9309 | 0.9828  | 0.9830 |
| Model2 | 12  |  0.9054  |  0.8910   | 0.9264 | 0.9084 | 0.9710  | 0.9710 |
| Model3 | 12  |  0.9222  |  0.9056   | 0.9439 | 0.9243 | 0.9787  | 0.9775 |

---

## 📈 Key Findings

- **Best K-mer Length**: K=9 and K=12 consistently produced the best results
- **Best Seed**: Seed 42 achieved the highest overall performance
- **K=3 Limitation**: Shorter K-mer sequences plateau around 84-88% accuracy
- **Model Consistency**: Model1 dominated all top positions

---

## 🔗 Embeddings Generated

The top 2 models generate embeddings used by the [Metabolic Network](../metabolic/):

| Embedding | Source Model         | Used In           |
| --------- | -------------------- | ----------------- |
| **E-1**   | 🥇 Best-Experiment-1 | Metabolic Network |
| **E-2**   | 🥈 Best-Experiment-2 | Metabolic Network |
