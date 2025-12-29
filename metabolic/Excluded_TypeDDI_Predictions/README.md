# Dataset Analysis Results

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

A validation was performed to determine where excluded labels appeared in the model's predictions. Out of the excluded pairs, 38 were matched for analysis.

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
