# Dataset Analysis Results
During preprocessing, 406 drug–drug interaction pairs were annotated with multiple interaction categories. To enable single-label supervised learning, only one label was retained for each pair and all additional labels were removed. Among these multi-label cases, 38 (9.36%) appeared in the stratified test split, allowing assessment of the model's ability to recover excluded interaction types. Remarkably, the model reproduced 94.74% of the omitted labels within its top-3 predictions, despite never encountering them during training or validation. This result suggests that the hypergraph architecture captures underlying multi-mechanistic pharmacological relationships and can infer secondary interaction mechanisms beyond the primary label used during training.
## Summary Statistics

The dataset underwent processing to identify and remove pairs with multiple reaction types.

| Metric | Value |
|--------|-------|
| Original dataset | 192,283 rows |
| Processed dataset | 191,877 rows |
| Total removed | 406 rows |
| Pairs with multiple types | 406 |
| Excluded reactions | 406 |

## Validation Results


### Distribution of Excluded Labels

| Position | Count |
|----------|-------|
| Top 1 | 9 |
| Top 2 | 22 |
| Top 3 | 5 |
| Not Found | 2 |

### Breakdown by Position

| Category | Count | Percentage |
|----------|-------|------------|
| Found in Top 1 (Primary) | 9 | 23.68% |
| Found in Top 2 (Secondary) | 22 | 57.89% |
| Found in Top 3 (Tertiary) | 5 | 13.16% |

### Summary

| Result | Count | Percentage |
|--------|-------|------------|
| Total Found in Top 3 | 36 | 94.74% |
| Not Found in Top 3 | 2 | 5.26% |

The validation demonstrates that 94.74% of excluded labels were successfully identified within the top 3 predictions, indicating strong model performance in capturing alternative reaction types.
