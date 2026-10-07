# Automobile Insurance Fraud Detection (MSc Dissertation)

## Question
Fraud is rare, so models trained on raw data tend to miss it. **Do resampling methods actually help a strong gradient boosting model detect fraudulent insurance claims?**

## Data
- 15,420 car insurance claims, 33 columns, only **6% fraud**
- Source: *Vehicle Insurance Claim Fraud Detection* dataset (`fraud_oracle.csv`), available on Kaggle
- Place the file at `data/fraud_oracle.csv`

## Method
1. Cleaned the data: dropped the ID column, fixed 320 impossible ages (Age = 0), removed one invalid record
2. Encoded 24 categorical features with ordinal encoding
3. Split into train/test **before** resampling to avoid data leakage
4. Trained the **same LightGBM model** on: original data, class weights, SMOTE, ADASYN, and SMOTE-Tomek
5. Compared with an unsupervised **Isolation Forest**
6. Evaluated with precision, recall, F1, PR-AUC and ROC-AUC (metrics suited to rare events)

## Key results
| Model | Precision | Recall | F1 | PR-AUC |
|-------|-----------|--------|----|--------|
| Baseline (no resampling) | 0.208 | 0.502 | 0.294 | 0.252 |
| Class weights | 0.226 | 0.429 | 0.296 | 0.227 |
| SMOTE | 0.230 | 0.437 | 0.301 | 0.240 |
| ADASYN | 0.203 | 0.511 | 0.291 | 0.235 |
| SMOTE-Tomek | 0.233 | 0.468 | **0.311** | 0.243 |
| Isolation Forest | 0.064 | 0.710 | 0.117 | 0.068 |

- Resampling gave only **small gains** over a well-tuned baseline
- Supervised models **clearly outperformed** the unsupervised Isolation Forest, which produced too many false alarms

## Files
- `fraud_detection.ipynb` – full analysis
- `dissertation_report.pdf` – dissertation report

## Run it
```bash
pip install pandas numpy scikit-learn matplotlib lightgbm imbalanced-learn
```
