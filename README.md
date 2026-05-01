# AI Network Anomaly Sentinel

Real-time network intrusion detection using a Hybrid Ensemble of ML models.

**Team:** Akshaya S E · Lokesh C · Amogh Gaurav B H  
**Institution:** Dayananda Sagar University, AICS 2025

## Models Used
- Random Forest, Extra Trees, XGBoost, LightGBM (supervised)
- Isolation Forest — trained on normal traffic only (unsupervised)
- Hybrid Ensemble: 0.80 × classifiers + 0.20 × IF → **97.45% accuracy**

## Files
| File | Description |
|---|---|
| `ai_anomaly.ipynb` | Main training notebook — all 5 models + ensemble |
| `sentinel_website.html` | Interactive demo website |

## Dataset
KDD Cup 1999 — download from UCI ML Repository:  
https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html  
Place `train_csv.txt` and `test_csv.txt` in the project root before running.

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook ai_anomaly.ipynb
```

## Results
| Model | Accuracy | F1 | AUC-ROC |
|---|---|---|---|
| Hybrid Ensemble ★ | 97.45% | 0.9744 | 0.9870 |
| XGBoost | 97.12% | 0.9710 | 0.9850 |
| LightGBM | 96.98% | 0.9698 | 0.9840 |
| Random Forest | 96.21% | 0.9624 | 0.9729 |
| Isolation Forest | 81.47% | 0.8180 | 0.9397 |
