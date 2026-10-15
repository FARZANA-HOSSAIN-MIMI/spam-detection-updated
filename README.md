# SMS Spam Classification (SVM → Improved SVM + Model Comparison)

Classifies SMS messages as **spam** or **ham** using TF-IDF features and linear models.

## Dataset
[SMS Spam Collection – Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset).
Download `spam.csv` and upload it when the notebook asks (or place it next to the notebook).

## Run it
Open `SMS_Spam_SVM_Improved.ipynb` in Google Colab → Runtime → Run all → upload `spam.csv` when prompted.

## What changed vs. the original notebook
- Digits, prices and URLs are kept as tokens instead of being deleted
- Word + character n-gram TF-IDF features
- Class-weight balancing and F1-based tuning
- Cross-validation on the training set only; test set used once
- 7 models compared; soft-voting ensemble (SVM + Logistic Regression + Naive Bayes) as final model

## Results (held-out test set)
| | Original SVM | Final model |
|---|---|---|
| Accuracy | 0.984 | 0.991 |
| Spam recall | 0.886 | 0.947 |
| F1 (spam) | 0.932 | 0.965 |
| Spam messages missed | 15 | 7 |

## Files
- `SMS_Spam_SVM_Improved.ipynb` – full analysis with outputs
- AUthor **FH Mimi**
