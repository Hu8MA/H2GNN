# DataSet-Partitions

## Overview

| Item | Value |
|------|-------|
| Total Interactions | 191,877 |
| Unique Drugs | 1,709 |
| Split Ratio | 80% / 10% / 10% |
| Seeds | 32, 42, 46 |

## Split Sizes

| Split | Count |
|-------|:-----:|
| Train | 153,501 |
| Validation | 19,187 |
| Test | 19,189 |

## Per-Seed Summary

| Seed | Drugs in Train | Drugs in Val | Drugs in Test | Status |
|:----:|:--------------:|:------------:|:-------------:|:------:|
| 32 | 1,709 | 1,534 | 1,517 | ✅ |
| 42 | 1,709 | 1,536 | 1,540 | ✅ |
| 46 | 1,709 | 1,508 | 1,534 | ✅ |

## Data Leakage Verification

| Check | Result |
|-------|:------:|
| Positive Overlap (Train/Val/Test) | ✅ None |
| Negative Overlap (Train/Val/Test) | ✅ None |
| Internal Conflicts | ✅ None |
| Global Conflicts | ✅ None |

## Final Verdict

✅ **No data leakage detected**  
✅ **No cold-start issue** — all 1,709 drugs appear in training  
✅ **All seeds meet target split sizes**
